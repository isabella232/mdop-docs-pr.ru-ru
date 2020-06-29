---
title: Установка сервера управления на отдельном компьютере и подключение его к базе данных
description: Установка сервера управления на отдельном компьютере и подключение его к базе данных
author: dansimp
ms.assetid: 95281287-cb56-4117-befd-854268ea147c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86f384e88b85101855287bb428e75376f7974219
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814029"
---
# <span data-ttu-id="df91d-103">Установка сервера управления на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="df91d-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="df91d-104">Чтобы установить сервер управления на отдельном компьютере и подключить его к базе данных, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="df91d-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="df91d-105">Установка сервера управления на отдельном компьютере и его подключение к базе данных</span><span class="sxs-lookup"><span data-stu-id="df91d-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="df91d-106">Скопируйте файлы установки сервера App-V 5,0 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="df91d-106">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="df91d-107">Чтобы запустить установку App-V 5,0 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="df91d-107">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="df91d-108">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="df91d-108">Click **Install**.</span></span>

2.  <span data-ttu-id="df91d-109">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="df91d-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="df91d-110">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="df91d-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="df91d-111">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="df91d-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="df91d-112">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="df91d-112">Click **Next**.</span></span>

4.  <span data-ttu-id="df91d-113">На странице **Выбор компонентов** установите флажок **сервер управления** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="df91d-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="df91d-114">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="df91d-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="df91d-115">На странице **Настройка существующей базы данных управления** выберите **использовать удаленный SQL Server**и введите имя компьютера, на котором работает Microsoft SQL SQL, например **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="df91d-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="df91d-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="df91d-116">Note</span></span>**  
    <span data-ttu-id="df91d-117">Если Microsoft SQL Server развернут на том же сервере, выберите параметр **использовать локальный SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="df91d-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="df91d-118">На странице **Настройка конфигурации сервера управления** укажите группу или учетную запись, которая будет подключаться к консоли управления в целях администрирования, например **MyDomain\\MyUser** или **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="df91d-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="df91d-119">Указанная учетная запись или группа рекламы будут включены для управления сервером с помощью консоли управления.</span><span class="sxs-lookup"><span data-stu-id="df91d-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="df91d-120">Вы можете добавить дополнительных пользователей или группы, используя консоль управления после установки.</span><span class="sxs-lookup"><span data-stu-id="df91d-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="df91d-121">Укажите **имя веб-сайта** , который вы хотите использовать для службы управления.</span><span class="sxs-lookup"><span data-stu-id="df91d-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="df91d-122">Если у вас нет настраиваемого имени, подтвердите действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="df91d-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="df91d-123">Для **привязки порта**укажите уникальный номер порта, который вы хотите использовать, например **12345**.</span><span class="sxs-lookup"><span data-stu-id="df91d-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="df91d-124">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="df91d-124">Click **Install**.</span></span>

9. <span data-ttu-id="df91d-125">Чтобы убедиться в успешном завершении установки, откройте веб-браузер и введите следующий URL-адрес: http://managementserver:portnumber/Console.html Если установка прошла успешно, вы увидите, что **консоль управления Silverlight** отображается без сообщений об ошибках и предупреждений.</span><span class="sxs-lookup"><span data-stu-id="df91d-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.html if the installation was successful you should see the **Silverlight Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="df91d-126">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="df91d-126">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="df91d-127">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="df91d-127">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="df91d-128">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="df91d-128">Got an App-V issue?</span></span>** <span data-ttu-id="df91d-129">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="df91d-129">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="df91d-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="df91d-130">Related topics</span></span>


[<span data-ttu-id="df91d-131">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="df91d-131">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









