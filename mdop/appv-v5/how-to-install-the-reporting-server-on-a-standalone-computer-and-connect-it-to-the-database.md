---
title: Установка сервера отчетности на отдельном компьютере и подключение его к базе данных
description: Установка сервера отчетности на отдельном компьютере и подключение его к базе данных
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813984"
---
# <span data-ttu-id="4f837-103">Установка сервера отчетности на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="4f837-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="4f837-104">Чтобы установить сервер отчетов на отдельном компьютере и подключить его к базе данных, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="4f837-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="4f837-105">Важно.</span><span class="sxs-lookup"><span data-stu-id="4f837-105">Important</span></span>**  
<span data-ttu-id="4f837-106">Перед выполнением описанной ниже процедуры вы должны ознакомиться с [отчетами App-V 5,0](about-app-v-50-reporting.md)и ознакомиться с ними.</span><span class="sxs-lookup"><span data-stu-id="4f837-106">Before performing the following procedure you should read and understand [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>



**<span data-ttu-id="4f837-107">Установка сервера отчетов на отдельном компьютере и его подключение к базе данных</span><span class="sxs-lookup"><span data-stu-id="4f837-107">To install the reporting server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="4f837-108">Скопируйте файлы установки сервера App-V 5,0 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="4f837-108">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="4f837-109">Чтобы запустить установку App-V 5,0 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="4f837-109">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="4f837-110">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="4f837-110">Click **Install**.</span></span>

2.  <span data-ttu-id="4f837-111">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f837-111">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="4f837-112">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="4f837-112">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="4f837-113">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="4f837-113">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="4f837-114">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f837-114">Click **Next**.</span></span>

4.  <span data-ttu-id="4f837-115">На странице **Выбор компонентов** установите флажок **сервер отчетов** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f837-115">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="4f837-116">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4f837-116">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="4f837-117">На странице **Настройка существующей базы данных отчетов** выберите **использовать удаленный SQL Server**и введите имя компьютера, на котором работает Microsoft SQL Server, например **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="4f837-117">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="4f837-118">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4f837-118">Note</span></span>**  
    <span data-ttu-id="4f837-119">Если Microsoft SQL Server развернут на том же сервере, выберите параметр **использовать локальный SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="4f837-119">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. <span data-ttu-id="4f837-120">На странице **Настройка конфигурации сервера отчетов** .</span><span class="sxs-lookup"><span data-stu-id="4f837-120">On the **Configure Reporting Server Configuration** page.</span></span>

   -   <span data-ttu-id="4f837-121">Укажите имя веб-сайта, который вы хотите использовать для службы отчетов.</span><span class="sxs-lookup"><span data-stu-id="4f837-121">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="4f837-122">Оставьте значение по умолчанию без изменений, если у вас нет настраиваемого имени.</span><span class="sxs-lookup"><span data-stu-id="4f837-122">Leave the default unchanged if you do not have a custom name.</span></span>

   -   <span data-ttu-id="4f837-123">Для **привязки порта**укажите уникальный номер порта, который будет использоваться приложением-V 5,0, например **55555**.</span><span class="sxs-lookup"><span data-stu-id="4f837-123">For the **Port binding**, specify a unique port number that will be used by App-V 5.0, for example **55555**.</span></span> <span data-ttu-id="4f837-124">Кроме того, необходимо убедиться, что указанный порт не используется другим веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="4f837-124">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="4f837-125">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="4f837-125">Click **Install**.</span></span>

   <span data-ttu-id="4f837-126">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="4f837-126">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="4f837-127">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="4f837-127">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="4f837-128">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="4f837-128">Got an App-V issue?</span></span>** <span data-ttu-id="4f837-129">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="4f837-129">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="4f837-130">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4f837-130">Related topics</span></span>


[<span data-ttu-id="4f837-131">Сведения об отчетности в App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="4f837-131">About App-V 5.0 Reporting</span></span>](about-app-v-50-reporting.md)

[<span data-ttu-id="4f837-132">Развертывание App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="4f837-132">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="4f837-133">Порядок включения отчетов в клиенте App-V 5.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="4f837-133">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









