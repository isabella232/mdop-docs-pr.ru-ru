---
title: Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации
description: Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации
author: dansimp
ms.assetid: 23b2d03a-20ce-4973-99ee-748f3b682207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 034cf5255d75bbaf6a5e65357bd5b3d472344f03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814392"
---
# <span data-ttu-id="15733-103">Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации</span><span class="sxs-lookup"><span data-stu-id="15733-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="15733-104">Развертывание пакетов и групп соединений с помощью сервера публикаций App-V 5,1 является полезным, так как он поддерживает единую точку управления и высокую масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="15733-104">Deploying packages and connection groups using the App-V 5.1 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="15733-105">Чтобы настроить клиент App-V 5,1 для получения обновлений с сервера публикаций, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="15733-105">Use the following steps to configure the App-V 5.1 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="15733-106">**Примечание**  Для следующих процедур сервер управления установлен на компьютере с именем **MyMgmtSrv**, а сервер публикаций установлен на компьютере с именем **MyPubSrv**.</span><span class="sxs-lookup"><span data-stu-id="15733-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="15733-107">Настройка клиента App-V 5,1 для получения обновлений с сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="15733-107">To configure the App-V 5.1 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="15733-108">Разверните сервер управления App-V 5,1 и серверы публикации и добавьте необходимые пакеты и группы подключений.</span><span class="sxs-lookup"><span data-stu-id="15733-108">Deploy the App-V 5.1 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="15733-109">Дополнительные сведения о добавлении пакетов и групп подключений можно найти [в разделе Добавление и обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) и [Создание группы подключения](how-to-create-a-connection-group51.md).</span><span class="sxs-lookup"><span data-stu-id="15733-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group51.md).</span></span>

2.  <span data-ttu-id="15733-110">Чтобы открыть консоль управления, щелкните указанную ниже ссылку, откройте браузер и введите указанные ниже команды. http://MyMgmtSrv/AppvManagement/Console.html в веб-браузере, а также для импорта, публикации и обслуживания всех пакетов и групп подключений, которые будут необходимы для определенного набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="15733-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="15733-111">На компьютере, на котором запущен клиент App-V 5,1, откройте командную команду PowerShell с повышенными привилегиями, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="15733-111">On the computer running the App-V 5.1 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="15733-112">Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="15733-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="15733-113">Эта команда позволяет настроить указанный сервер публикаций.</span><span class="sxs-lookup"><span data-stu-id="15733-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="15733-114">Результат должен выглядеть примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="15733-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="15733-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="15733-115">Id : 1</span></span>

    <span data-ttu-id="15733-116">SetByGroupPolicy: false</span><span class="sxs-lookup"><span data-stu-id="15733-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="15733-117">Name (имя): ABC</span><span class="sxs-lookup"><span data-stu-id="15733-117">Name : ABC</span></span>

    <span data-ttu-id="15733-118">URL-адрес: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="15733-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="15733-119">GlobalRefreshEnabled: false</span><span class="sxs-lookup"><span data-stu-id="15733-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="15733-120">GlobalRefreshOnLogon: false</span><span class="sxs-lookup"><span data-stu-id="15733-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="15733-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="15733-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="15733-122">GlobalRefreshIntervalUnit: Day</span><span class="sxs-lookup"><span data-stu-id="15733-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="15733-123">UserRefreshEnabled: true</span><span class="sxs-lookup"><span data-stu-id="15733-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="15733-124">UserRefreshOnLogon: true</span><span class="sxs-lookup"><span data-stu-id="15733-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="15733-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="15733-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="15733-126">UserRefreshIntervalUnit: Day</span><span class="sxs-lookup"><span data-stu-id="15733-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="15733-127">Возвращенный идентификатор — в данном случае 1</span><span class="sxs-lookup"><span data-stu-id="15733-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="15733-128">На компьютере, на котором запущен клиент App-V 5,1, откройте командную строка PowerShell и введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="15733-128">On the computer running the App-V 5.1 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="15733-129">Sync-AppvPublishingServer-ServerId 1</span><span class="sxs-lookup"><span data-stu-id="15733-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="15733-130">Команда будет запрашивать сервер публикаций для пакетов и групп подключений, которые необходимо добавить или удалить для этого конкретного клиента на основании данных о разобслуживаниях пакетов и групп подключений, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="15733-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="15733-131">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="15733-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="15733-132">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="15733-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="15733-133">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="15733-133">Got an App-V issue?</span></span>** <span data-ttu-id="15733-134">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="15733-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="15733-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="15733-135">Related topics</span></span>


[<span data-ttu-id="15733-136">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="15733-136">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





