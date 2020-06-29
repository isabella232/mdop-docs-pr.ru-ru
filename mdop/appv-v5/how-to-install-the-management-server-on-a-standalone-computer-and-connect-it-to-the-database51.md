---
title: Установка сервера управления на отдельном компьютере и подключение его к базе данных
description: Установка сервера управления на отдельном компьютере и подключение его к базе данных
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814013"
---
# <span data-ttu-id="e5bec-103">Установка сервера управления на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="e5bec-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="e5bec-104">Чтобы установить сервер управления на отдельном компьютере и подключить его к базе данных, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e5bec-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="e5bec-105">Установка сервера управления на отдельном компьютере и его подключение к базе данных</span><span class="sxs-lookup"><span data-stu-id="e5bec-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="e5bec-106">Скопируйте файлы установки сервера App-V 5,1 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="e5bec-106">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="e5bec-107">Чтобы запустить установку App-V 5,1 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="e5bec-107">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="e5bec-108">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-108">Click **Install**.</span></span>

2.  <span data-ttu-id="e5bec-109">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="e5bec-110">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="e5bec-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="e5bec-111">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="e5bec-112">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-112">Click **Next**.</span></span>

4.  <span data-ttu-id="e5bec-113">На странице **Выбор компонентов** установите флажок **сервер управления** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="e5bec-114">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="e5bec-115">На странице **Настройка существующей базы данных управления** выберите **использовать удаленный SQL Server**и введите имя компьютера, на котором работает Microsoft SQL SQL, например **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="e5bec-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e5bec-116">Note</span></span>**  
    <span data-ttu-id="e5bec-117">Если Microsoft SQL Server развернут на том же сервере, выберите параметр **использовать локальный SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="e5bec-118">На странице **Настройка конфигурации сервера управления** укажите группу или учетную запись, которая будет подключаться к консоли управления в целях администрирования, например **MyDomain\\MyUser** или **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="e5bec-119">Указанная учетная запись или группа рекламы будут включены для управления сервером с помощью консоли управления.</span><span class="sxs-lookup"><span data-stu-id="e5bec-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="e5bec-120">Вы можете добавить дополнительных пользователей или группы, используя консоль управления после установки.</span><span class="sxs-lookup"><span data-stu-id="e5bec-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="e5bec-121">Укажите **имя веб-сайта** , который вы хотите использовать для службы управления.</span><span class="sxs-lookup"><span data-stu-id="e5bec-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="e5bec-122">Если у вас нет настраиваемого имени, подтвердите действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5bec-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="e5bec-123">Для **привязки порта**укажите уникальный номер порта, который вы хотите использовать, например **12345**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="e5bec-124">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="e5bec-124">Click **Install**.</span></span>

9. <span data-ttu-id="e5bec-125">Чтобы убедиться в успешном завершении установки, откройте веб-браузер и введите следующий URL-адрес: http://managementserver:portnumber/Console .</span><span class="sxs-lookup"><span data-stu-id="e5bec-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.</span></span> <span data-ttu-id="e5bec-126">Если установка прошла успешно, на экране появится **консоль управления** без сообщений об ошибках и предупреждений.</span><span class="sxs-lookup"><span data-stu-id="e5bec-126">If the installation was successful, you should see the **Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="e5bec-127">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="e5bec-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="e5bec-128">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="e5bec-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="e5bec-129">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="e5bec-129">Got an App-V issue?</span></span>** <span data-ttu-id="e5bec-130">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="e5bec-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="e5bec-131">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e5bec-131">Related topics</span></span>


[<span data-ttu-id="e5bec-132">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e5bec-132">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









