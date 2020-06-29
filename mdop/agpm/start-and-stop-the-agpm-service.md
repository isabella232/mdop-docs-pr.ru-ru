---
title: Запуск и остановка службы AGPM
description: Запуск и остановка службы AGPM
author: dansimp
ms.assetid: 769aa0ce-224a-446f-9958-9518af4ad159
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 33e797182d49157da0fe8f36dce17b4b35cdd623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818322"
---
# <span data-ttu-id="754c9-103">Запуск и остановка службы AGPM</span><span class="sxs-lookup"><span data-stu-id="754c9-103">Start and Stop the AGPM Service</span></span>


<span data-ttu-id="754c9-104">Служба управления групповыми политиками — это служба Windows, которая выступает в качестве прокси-сервера, управляет доступом клиентов к объектам групповой политики (GPO) в архивной и рабочей среде.</span><span class="sxs-lookup"><span data-stu-id="754c9-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span>

<span data-ttu-id="754c9-105">**Важно!**  Остановка или отключение службы РАСШИРЕНного режима не позволит клиентам с РАСШИРЕНным управлением правами выполнять какие-либо операции (например, перечисление или изменение объектов групповой политики) с помощью сервера.</span><span class="sxs-lookup"><span data-stu-id="754c9-105">**Important** Stopping or disabling the AGPM Service will prevent AGPM clients from performing any operations (such as listing or editing GPOs) through the server.</span></span>

 

<span data-ttu-id="754c9-106">Для выполнения этой процедуры необходима учетная запись пользователя, на которой установлен доступ к серверу РАСШИРЕНного доступа к данным (на компьютере, на котором установлена служба РАСШИРЕНного доступа к данным).</span><span class="sxs-lookup"><span data-stu-id="754c9-106">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) is required to complete this procedure.</span></span>

**<span data-ttu-id="754c9-107">Запуск и остановка службы РАСШИРЕНного</span><span class="sxs-lookup"><span data-stu-id="754c9-107">To start or stop the AGPM Service</span></span>**

1.  <span data-ttu-id="754c9-108">На компьютере, на котором установлен сервер расширенного управления групповыми политиками (и, следовательно, служба РАСШИРЕНных вкладок), нажмите кнопку **Пуск**, выберите **Панель управления**, щелкните **Администрирование**и выберите пункт **службы**.</span><span class="sxs-lookup"><span data-stu-id="754c9-108">On the computer on which Microsoft Advanced Group Policy Management - Server (and therefore the AGPM Service) is installed, click **Start**, click **Control Panel**, click **Administrative Tools**, and then click **Services**.</span></span>

2.  <span data-ttu-id="754c9-109">В списке служб щелкните правой кнопкой мыши **службу расширенного** выбора элементов и выберите **Пуск**, **перезапустить**или **остановить**.</span><span class="sxs-lookup"><span data-stu-id="754c9-109">In the list of services, right-click **AGPM Service** and select **Start**, **Restart**, or **Stop**.</span></span>

    <span data-ttu-id="754c9-110">**Внимание!**  Не изменяйте параметры службы РАСШИРЕНного **управления правами с помощью средств администрирования** и **служб** в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="754c9-110">**Caution** Do not modify settings for the AGPM Service through **Administrative Tools** and **Services** in the operating system.</span></span> <span data-ttu-id="754c9-111">Это может привести к невозможности запуска службы РАСШИРЕНного настольных служб.</span><span class="sxs-lookup"><span data-stu-id="754c9-111">Doing so can prevent the AGPM Service from starting.</span></span> <span data-ttu-id="754c9-112">Чтобы изменить параметры службы, ознакомьтесь со сведениями о том, как [управлять службой управления групповыми политиками](managing-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="754c9-112">To modify settings for the service, see [Managing the AGPM Service](managing-the-agpm-service.md).</span></span>

     

### <span data-ttu-id="754c9-113">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="754c9-113">Additional references</span></span>

-   [<span data-ttu-id="754c9-114">Управление службой AGPM</span><span class="sxs-lookup"><span data-stu-id="754c9-114">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





