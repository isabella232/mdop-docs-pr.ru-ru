---
title: Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации
description: Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814389"
---
# <span data-ttu-id="399d0-103">Настройка клиента для получения обновлений пакетов и групп соединений с сервера публикации</span><span class="sxs-lookup"><span data-stu-id="399d0-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="399d0-104">Развертывание пакетов и групп соединений с помощью сервера публикаций App-V 5,0 является полезным, так как он поддерживает единую точку управления и высокую масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="399d0-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="399d0-105">Чтобы настроить клиент App-V 5,0 для получения обновлений с сервера публикаций, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="399d0-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="399d0-106">**Примечание**  Для следующих процедур сервер управления установлен на компьютере с именем **MyMgmtSrv**, а сервер публикаций установлен на компьютере с именем **MyPubSrv**.</span><span class="sxs-lookup"><span data-stu-id="399d0-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="399d0-107">Настройка клиента App-V 5,0 для получения обновлений с сервера публикаций</span><span class="sxs-lookup"><span data-stu-id="399d0-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="399d0-108">Разверните сервер управления App-V 5,0 и серверы публикации и добавьте необходимые пакеты и группы подключений.</span><span class="sxs-lookup"><span data-stu-id="399d0-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="399d0-109">Дополнительные сведения о добавлении пакетов и групп подключений можно найти [в разделе Добавление и обновление пакетов с помощью консоли управления](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) и [Создание группы подключения](how-to-create-a-connection-group.md).</span><span class="sxs-lookup"><span data-stu-id="399d0-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="399d0-110">Чтобы открыть консоль управления, щелкните указанную ниже ссылку, откройте браузер и введите указанные ниже команды. http://MyMgmtSrv/AppvManagement/Console.html в веб-браузере, а также для импорта, публикации и обслуживания всех пакетов и групп подключений, которые будут необходимы для определенного набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="399d0-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="399d0-111">На компьютере, на котором запущен клиент App-V 5,0, откройте командную команду PowerShell с повышенными привилегиями, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="399d0-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="399d0-112">Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="399d0-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="399d0-113">Эта команда позволяет настроить указанный сервер публикаций.</span><span class="sxs-lookup"><span data-stu-id="399d0-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="399d0-114">Результат должен выглядеть примерно следующим образом:</span><span class="sxs-lookup"><span data-stu-id="399d0-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="399d0-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="399d0-115">Id : 1</span></span>

    <span data-ttu-id="399d0-116">SetByGroupPolicy: false</span><span class="sxs-lookup"><span data-stu-id="399d0-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="399d0-117">Name (имя): ABC</span><span class="sxs-lookup"><span data-stu-id="399d0-117">Name : ABC</span></span>

    <span data-ttu-id="399d0-118">URL-адрес: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="399d0-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="399d0-119">GlobalRefreshEnabled: false</span><span class="sxs-lookup"><span data-stu-id="399d0-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="399d0-120">GlobalRefreshOnLogon: false</span><span class="sxs-lookup"><span data-stu-id="399d0-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="399d0-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="399d0-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="399d0-122">GlobalRefreshIntervalUnit: Day</span><span class="sxs-lookup"><span data-stu-id="399d0-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="399d0-123">UserRefreshEnabled: true</span><span class="sxs-lookup"><span data-stu-id="399d0-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="399d0-124">UserRefreshOnLogon: true</span><span class="sxs-lookup"><span data-stu-id="399d0-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="399d0-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="399d0-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="399d0-126">UserRefreshIntervalUnit: Day</span><span class="sxs-lookup"><span data-stu-id="399d0-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="399d0-127">Возвращенный идентификатор — в данном случае 1</span><span class="sxs-lookup"><span data-stu-id="399d0-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="399d0-128">На компьютере, на котором запущен клиент App-V 5,0, откройте командную строка PowerShell и введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="399d0-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="399d0-129">Sync-AppvPublishingServer-ServerId 1</span><span class="sxs-lookup"><span data-stu-id="399d0-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="399d0-130">Команда будет запрашивать сервер публикаций для пакетов и групп подключений, которые необходимо добавить или удалить для этого конкретного клиента на основании данных о разобслуживаниях пакетов и групп подключений, настроенных на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="399d0-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="399d0-131">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="399d0-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="399d0-132">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="399d0-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="399d0-133">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="399d0-133">Got an App-V issue?</span></span>** <span data-ttu-id="399d0-134">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="399d0-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="399d0-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="399d0-135">Related topics</span></span>


[<span data-ttu-id="399d0-136">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="399d0-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





