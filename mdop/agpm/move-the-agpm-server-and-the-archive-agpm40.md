---
title: Перемещение сервера и архива AGPM
description: Перемещение сервера и архива AGPM
author: dansimp
ms.assetid: 9ec48d3a-c293-45f0-8939-32ccdc062303
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 61ad2eb6e0ea46eef89379894a99469254e0fd5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822532"
---
# <span data-ttu-id="86303-103">Перемещение сервера и архива AGPM</span><span class="sxs-lookup"><span data-stu-id="86303-103">Move the AGPM Server and the Archive</span></span>


<span data-ttu-id="86303-104">Если вы заменяете сервер РАСШИРЕНного обслуживания и сервер, на котором размещается Архив, необходимо переместить службу РАСШИРЕНного выбора и архив.</span><span class="sxs-lookup"><span data-stu-id="86303-104">If you are replacing the AGPM Server and the server on which the archive is hosted, you must move the AGPM Service and the archive.</span></span> <span data-ttu-id="86303-105">Если вы предпочитаете, вы можете переместить службу РАСШИРЕНного и архивов отдельно.</span><span class="sxs-lookup"><span data-stu-id="86303-105">If you prefer, you can move the AGPM Service and the archive separately.</span></span>

**<span data-ttu-id="86303-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="86303-106">Note</span></span>**  
-   <span data-ttu-id="86303-107">Сервер расширенного управления групповыми политиками — это компьютер, на котором размещается служба, и на компьютере, на котором установлен компонент Advanced Group Policy Management (Майкрософт) — сервер.</span><span class="sxs-lookup"><span data-stu-id="86303-107">The AGPM Server is the computer that hosts the AGPM Service and the computer on which Microsoft Advanced Group Policy Management – Server is installed.</span></span>

-   <span data-ttu-id="86303-108">По умолчанию архив размещается на сервере расширенного управления групповыми политиками, но вы можете указать путь к архиву, чтобы разместить его на другом сервере.</span><span class="sxs-lookup"><span data-stu-id="86303-108">By default, the archive is hosted on the AGPM Server, but you can specify an archive path to host it on another server instead.</span></span>

 

<span data-ttu-id="86303-109">Для выполнения этой процедуры требуется пользовательская учетная запись, которая входит в группу администраторов домена и имеет доступ к предыдущему и новым серверам РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="86303-109">A user account that is a member of the Domain Admins group and has access to the previous and new AGPM Servers is required to complete this procedure.</span></span> <span data-ttu-id="86303-110">Кроме того, чтобы выполнить эту процедуру, необходимо предоставить учетные данные учетной записи службы РАСШИРЕНного доступа для использования новым сервером РАСШИРЕНного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="86303-110">Additionally, you must provide credentials for the AGPM Service Account to be used by the new AGPM Server to complete this procedure.</span></span>

**<span data-ttu-id="86303-111">Перемещение службы РАСШИРЕНного и архивного сервера на другой сервер или серверы</span><span class="sxs-lookup"><span data-stu-id="86303-111">To move the AGPM Service and the archive to a different server or servers</span></span>**

1.  <span data-ttu-id="86303-112">Создавайте резервные копии архива.</span><span class="sxs-lookup"><span data-stu-id="86303-112">Back up the archive.</span></span> <span data-ttu-id="86303-113">Дополнительные сведения можно найти [в разделе Резервное копирование архива](back-up-the-archive-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="86303-113">For more information, see [Back Up the Archive](back-up-the-archive-agpm40.md).</span></span>

2.  <span data-ttu-id="86303-114">Перемещение службы РАСШИРЕНного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="86303-114">Move the AGPM Service:</span></span>

    1.  <span data-ttu-id="86303-115">Остановите службу РАСШИРЕНного.</span><span class="sxs-lookup"><span data-stu-id="86303-115">Stop the AGPM Service.</span></span> <span data-ttu-id="86303-116">Дополнительные сведения можно найти в разделе [Запуск и остановка службы расширенного](start-and-stop-the-agpm-service-agpm40.md)просмотра.</span><span class="sxs-lookup"><span data-stu-id="86303-116">For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="86303-117">Установка расширенного управления групповыми политиками (Майкрософт) — сервер на новом сервере, на котором будет размещена служба с РАСШИРЕНным использованием.</span><span class="sxs-lookup"><span data-stu-id="86303-117">Install Microsoft Advanced Group Policy Management - Server on the new server that will host the AGPM Service.</span></span> <span data-ttu-id="86303-118">В ходе этого процесса вы можете указать новый путь к архиву, расположение архива относительно сервера РАСШИРЕНного анализа.</span><span class="sxs-lookup"><span data-stu-id="86303-118">During this process, you specify the new archive path, the location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="86303-119">Дополнительные сведения можно найти [в статье пошаговые инструкции для расширенного управления групповыми политиками microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) ( https://go.microsoft.com/fwlink/?LinkId=153505) и [руководство по планированию для расширенного управления групповыми политиками Microsoft](https://go.microsoft.com/fwlink/?LinkId=156883) ) ( https://go.microsoft.com/fwlink/?LinkId=156883) .</span><span class="sxs-lookup"><span data-stu-id="86303-119">For more information, see [Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505) and [Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883).</span></span>

    3.  <span data-ttu-id="86303-120">Администратор расширенного управления групповыми политиками (полный доступ) должен настроить подключение к серверу РАСШИРЕНного доступа для всех администраторов групповой политики, которые будут использовать новый сервер, и удалить подключение для старого сервера. Кроме того, каждый администратор групповой политики должен вручную настроить новое подключение к серверу расширенного управления правами и удалить старое подключение к серверу РАСШИРЕНного управления правами для оснастки управления ГРУППОВыми политиками на компьютере.</span><span class="sxs-lookup"><span data-stu-id="86303-120">Either an AGPM Administrator (Full Control) must configure the AGPM Server connection for all Group Policy administrators who will use the new AGPM Server and remove the connection for the old AGPM Server, or else each Group Policy administrator must manually configure the new AGPM Server connection and remove the old AGPM Server connection for the AGPM snap-in on their computer.</span></span> <span data-ttu-id="86303-121">Дополнительные сведения можно найти в разделе [Настройка подключений к серверам с расширенным](configure-agpm-server-connections-agpm40.md)протоколом.</span><span class="sxs-lookup"><span data-stu-id="86303-121">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm40.md).</span></span>

        <span data-ttu-id="86303-122">**Примечание**  Рекомендуется удалить расширенное управление групповыми политиками (Майкрософт) – сервер с предыдущего сервера РАСШИРЕНного управления правами.</span><span class="sxs-lookup"><span data-stu-id="86303-122">**Note** As a best practice, you should uninstall Microsoft Advanced Group Policy Management – Server from the previous AGPM Server.</span></span> <span data-ttu-id="86303-123">Это обеспечит непреднамеренное перезапуск службы РАСШИРЕНного работы на этом сервере и может привести к путанице в случае, если на нем осталось соединение с помощью РАСШИРЕНного сервера.</span><span class="sxs-lookup"><span data-stu-id="86303-123">This will ensure that the AGPM Service cannot be unintentionally restarted on that server and potentially cause confusion if any AGPM Server connections to it remain.</span></span>

         

3.  <span data-ttu-id="86303-124">Скопируйте архив из резервной копии на новый сервер, на котором будет размещен архив.</span><span class="sxs-lookup"><span data-stu-id="86303-124">Copy the archive from the backup to the new server that will host the archive.</span></span> <span data-ttu-id="86303-125">Дополнительные сведения можно найти в разделе [Восстановление архива из резервной копии](restore-the-archive-from-a-backup-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="86303-125">For more information, see [Restore the Archive from a Backup](restore-the-archive-from-a-backup-agpm40.md).</span></span>

    <span data-ttu-id="86303-126">**Важно!**  Если вы перешли в архив, не перемещая службу РАСШИРЕНного использования, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="86303-126">**Important** If you moved the archive without moving the AGPM Service at the same time:</span></span>

    1.  <span data-ttu-id="86303-127">Необходимо изменить путь к архиву, чтобы он указывал на новое расположение для архива относительно сервера РАСШИРЕНного поиска.</span><span class="sxs-lookup"><span data-stu-id="86303-127">You must change the archive path to point to the new location for the archive in relation to the AGPM Server.</span></span> <span data-ttu-id="86303-128">Дополнительные сведения можно найти в разделе [изменение службы расширенного редактирования](modify-the-agpm-service-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="86303-128">For more information, see [Modify the AGPM Service](modify-the-agpm-service-agpm40.md).</span></span>

    2.  <span data-ttu-id="86303-129">Вы должны повторно ввести пароль и подтвердить его на вкладке **доменное делегирование** . Дополнительные сведения можно найти в разделе [Настройка уведомлений по электронной почте](configure-e-mail-notification-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="86303-129">You must re-enter and confirm the password on the **Domain Delegation** tab. For more information, see [Configure E-Mail Notification](configure-e-mail-notification-agpm40.md).</span></span>

     

### <span data-ttu-id="86303-130">Дополнительные ссылки</span><span class="sxs-lookup"><span data-stu-id="86303-130">Additional references</span></span>

-   [<span data-ttu-id="86303-131">Резервное копирование архива</span><span class="sxs-lookup"><span data-stu-id="86303-131">Back Up the Archive</span></span>](back-up-the-archive-agpm40.md)

-   [<span data-ttu-id="86303-132">Восстановление архива из резервной копии</span><span class="sxs-lookup"><span data-stu-id="86303-132">Restore the Archive from a Backup</span></span>](restore-the-archive-from-a-backup-agpm40.md)

-   [<span data-ttu-id="86303-133">Настройка подключений к серверу AGPM</span><span class="sxs-lookup"><span data-stu-id="86303-133">Configure AGPM Server Connections</span></span>](configure-agpm-server-connections-agpm40.md)

-   [<span data-ttu-id="86303-134">Изменение службы AGPM</span><span class="sxs-lookup"><span data-stu-id="86303-134">Modify the AGPM Service</span></span>](modify-the-agpm-service-agpm40.md)

-   <span data-ttu-id="86303-135">Пошаговое [руководство для расширенного управления групповыми политиками Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span><span class="sxs-lookup"><span data-stu-id="86303-135">[Step-by-Step Guide for Microsoft Advanced Group Policy Management 4.0](https://go.microsoft.com/fwlink/?LinkId=153505) (https://go.microsoft.com/fwlink/?LinkId=153505)</span></span>

-   <span data-ttu-id="86303-136">[Руководство по планированию для расширенного управления групповыми политиками (Майкрософт](https://go.microsoft.com/fwlink/?LinkId=156883) ) (https://go.microsoft.com/fwlink/?LinkId=156883)</span><span class="sxs-lookup"><span data-stu-id="86303-136">[Planning Guide for Microsoft Advanced Group Policy Management](https://go.microsoft.com/fwlink/?LinkId=156883) (https://go.microsoft.com/fwlink/?LinkId=156883)</span></span>

-   [<span data-ttu-id="86303-137">Выполнение задач администратора AGPM</span><span class="sxs-lookup"><span data-stu-id="86303-137">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm40.md)

 

 





