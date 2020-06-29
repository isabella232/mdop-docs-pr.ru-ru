---
title: Установка сервера публикации на удаленном компьютере
description: Установка сервера публикации на удаленном компьютере
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813981"
---
# <span data-ttu-id="fff59-103">Установка сервера публикации на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="fff59-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="fff59-104">Чтобы установить сервер публикаций на отдельном компьютере, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="fff59-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="fff59-105">Перед выполнением описанной ниже процедуры убедитесь, что база данных и сервер управления доступны.</span><span class="sxs-lookup"><span data-stu-id="fff59-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="fff59-106">Установка сервера публикаций на отдельном компьютере</span><span class="sxs-lookup"><span data-stu-id="fff59-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="fff59-107">Скопируйте файлы установки сервера App-V 5,1 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="fff59-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="fff59-108">Чтобы запустить установку App-V 5,1 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="fff59-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="fff59-109">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="fff59-109">Click **Install**.</span></span>

2. <span data-ttu-id="fff59-110">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fff59-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="fff59-111">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="fff59-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="fff59-112">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="fff59-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="fff59-113">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fff59-113">Click **Next**.</span></span>

4. <span data-ttu-id="fff59-114">На странице **Выбор компонентов** установите флажок **сервер публикаций** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fff59-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="fff59-115">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="fff59-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="fff59-116">На странице **Настройка конфигурации сервера публикаций** укажите следующие элементы:</span><span class="sxs-lookup"><span data-stu-id="fff59-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="fff59-117">URL-адрес службы управления, к которой будет подключаться сервер публикации.</span><span class="sxs-lookup"><span data-stu-id="fff59-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="fff59-118">Например, **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="fff59-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="fff59-119">Укажите имя веб-сайта, который вы хотите использовать для службы публикации.</span><span class="sxs-lookup"><span data-stu-id="fff59-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="fff59-120">Если у вас нет настраиваемого имени, подтвердите действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fff59-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="fff59-121">Для **привязки порта**укажите уникальный номер порта, который будет использоваться приложением-V 5,1, например **54321**.</span><span class="sxs-lookup"><span data-stu-id="fff59-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.1, for example **54321**.</span></span>

7. <span data-ttu-id="fff59-122">На странице " **Готово для установки** " нажмите кнопку " **установить**".</span><span class="sxs-lookup"><span data-stu-id="fff59-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="fff59-123">После завершения установки сервер публикаций должен быть зарегистрирован на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="fff59-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="fff59-124">В консоли управления App-V 5,1 выполните указанные ниже действия, чтобы зарегистрировать сервер.</span><span class="sxs-lookup"><span data-stu-id="fff59-124">In the App-V 5.1 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="fff59-125">Откройте консоль сервера управления App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="fff59-125">Open the App-V 5.1 management server console.</span></span>

   2.  <span data-ttu-id="fff59-126">В левой области выберите пункт **серверы**, а затем — **зарегистрировать новый сервер**.</span><span class="sxs-lookup"><span data-stu-id="fff59-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="fff59-127">Введите имя сервера и его описание (если необходимо) и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="fff59-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="fff59-128">Чтобы проверить, правильно ли работает сервер публикаций, нужно импортировать пакет на сервер управления, протестировать его в группу Active Directory и опубликовать пакет.</span><span class="sxs-lookup"><span data-stu-id="fff59-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="fff59-129">С помощью браузера откройте следующий URL-адрес: <strong> http://publishingserver:pubport </strong> .</span><span class="sxs-lookup"><span data-stu-id="fff59-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="fff59-130">Если на сервере правильно выполняются такие сведения, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="fff59-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="fff59-131">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="fff59-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="fff59-132">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="fff59-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="fff59-133">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="fff59-133">Got an App-V issue?</span></span>** <span data-ttu-id="fff59-134">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="fff59-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="fff59-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="fff59-135">Related topics</span></span>


[<span data-ttu-id="fff59-136">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="fff59-136">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

 

 





