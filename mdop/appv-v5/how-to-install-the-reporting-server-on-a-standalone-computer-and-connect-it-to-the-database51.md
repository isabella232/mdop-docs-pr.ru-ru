---
title: Установка сервера отчетности на отдельном компьютере и подключение его к базе данных
description: Установка сервера отчетности на отдельном компьютере и подключение его к базе данных
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813973"
---
# <span data-ttu-id="ddb59-103">Установка сервера отчетности на отдельном компьютере и подключение его к базе данных</span><span class="sxs-lookup"><span data-stu-id="ddb59-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="ddb59-104">Чтобы установить сервер отчетов на отдельном компьютере и подключить его к базе данных, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ddb59-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="ddb59-105">**Важно!** Перед выполнением описанной ниже процедуры вы должны ознакомиться с [отчетами App-V 5,1](about-app-v-51-reporting.md)и ознакомиться с ними.</span><span class="sxs-lookup"><span data-stu-id="ddb59-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="ddb59-106">Установка сервера отчетов на отдельном компьютере и его подключение к базе данных</span><span class="sxs-lookup"><span data-stu-id="ddb59-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="ddb59-107">Скопируйте файлы установки сервера App-V 5,1 на компьютер, на котором вы хотите установить его.</span><span class="sxs-lookup"><span data-stu-id="ddb59-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="ddb59-108">Чтобы запустить установку App-V 5,1 Server, щелкните правой кнопкой мыши и запустите **appv\_server\_setup.exe** с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="ddb59-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="ddb59-109">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-109">Click **Install**.</span></span>

2. <span data-ttu-id="ddb59-110">На странице **Приступая к работе** проверьте и принимайте условия лицензии и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="ddb59-111">На странице **Использование центра обновления Майкрософт, чтобы обеспечить безопасность и актуальность** данных на компьютере, чтобы включить обновления Майкрософт, установите флажок **использовать Microsoft Update при проверке обновлений (рекомендуется).**</span><span class="sxs-lookup"><span data-stu-id="ddb59-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="ddb59-112">Чтобы отключить обновления Майкрософт, выберите **я не хочу использовать Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="ddb59-113">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-113">Click **Next**.</span></span>

4. <span data-ttu-id="ddb59-114">На странице **Выбор компонентов** установите флажок **сервер отчетов** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="ddb59-115">На странице **расположение для установки** подтвердите расположение по умолчанию и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="ddb59-116">На странице **Настройка существующей базы данных отчетов** выберите **использовать удаленный SQL Server**и введите имя компьютера, на котором работает Microsoft SQL Server, например **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ddb59-117">Если Microsoft SQL Server развернут на том же сервере, выберите параметр **использовать локальный SQL Server**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="ddb59-118">Для экземпляра SQL Server выберите **использовать экземпляр по умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="ddb59-119">Если вы используете настраиваемый экземпляр Microsoft SQL Server, необходимо выбрать **использовать настраиваемый экземпляр** и ввести имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ddb59-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="ddb59-120">Укажите **имя базы данных SQL Server** , которое будет использовать этот сервер отчетов (например, **AppvReporting**).</span><span class="sxs-lookup"><span data-stu-id="ddb59-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="ddb59-121">На странице **Настройка конфигурации сервера отчетов** .</span><span class="sxs-lookup"><span data-stu-id="ddb59-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="ddb59-122">Укажите имя веб-сайта, который вы хотите использовать для службы отчетов.</span><span class="sxs-lookup"><span data-stu-id="ddb59-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="ddb59-123">Оставьте значение по умолчанию без изменений, если у вас нет настраиваемого имени.</span><span class="sxs-lookup"><span data-stu-id="ddb59-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="ddb59-124">Для **привязки порта**укажите уникальный номер порта, который будет использоваться приложением-V 5,1, например **55555**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="ddb59-125">Кроме того, необходимо убедиться, что указанный порт не используется другим веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="ddb59-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="ddb59-126">Нажмите кнопку **Установить**.</span><span class="sxs-lookup"><span data-stu-id="ddb59-126">Click **Install**.</span></span>

**<span data-ttu-id="ddb59-127">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="ddb59-127">Got an App-V issue?</span></span>** <span data-ttu-id="ddb59-128">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ddb59-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ddb59-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ddb59-129">Related topics</span></span>

[<span data-ttu-id="ddb59-130">Сведения об отчетности в App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ddb59-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="ddb59-131">Развертывание App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="ddb59-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="ddb59-132">Порядок включения отчетов в клиенте App-V 5.1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="ddb59-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
