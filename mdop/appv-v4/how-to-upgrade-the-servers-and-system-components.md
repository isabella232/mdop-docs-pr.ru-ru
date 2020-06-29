---
title: Обновление серверов и компонентов системы
description: Обновление серверов и компонентов системы
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816422"
---
# <span data-ttu-id="80b75-103">Обновление серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="80b75-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="80b75-104">Выполните описанные ниже действия, чтобы обновить программные компоненты, установленные на всех компьютерах системы виртуализации приложений.</span><span class="sxs-lookup"><span data-stu-id="80b75-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="80b75-105">Системные службы Application Virtualization будут автоматически перезапущены на каждом компьютере после того, как она будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="80b75-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="80b75-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80b75-106">Note</span></span>**  
-   <span data-ttu-id="80b75-107">Процесс обновления останавливает все системные службы виртуализации приложений, тем самым получая систему из обслуживания.</span><span class="sxs-lookup"><span data-stu-id="80b75-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="80b75-108">Сеансы пользователей должны быть закрыты, прежде чем начинать процесс обновления, и вы должны остановить все службы сервера Application Virtualization в своей среде.</span><span class="sxs-lookup"><span data-stu-id="80b75-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="80b75-109">Если у вас есть несколько серверов, которые имеют доступ к базе данных Application Virtualization, то во время обновления базы данных все эти серверы должны быть переведены в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="80b75-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="80b75-110">Вы должны следовать обычным бизнес-рекомендациям по обновлению базы данных, но настоятельно рекомендуется протестировать обновление базы данных с помощью резервной копии базы данных на тестовом сервере.</span><span class="sxs-lookup"><span data-stu-id="80b75-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="80b75-111">Затем необходимо выбрать один из серверов для первого обновления, который обновит схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="80b75-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="80b75-112">После успешного обновления рабочей базы данных вы можете обновить другие серверы.</span><span class="sxs-lookup"><span data-stu-id="80b75-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="80b75-113">Вы можете обновить приложение до Microsoft Application Virtualization (App-v) 4.5 только из Microsoft Application Virtualization (App-V) 4.1 или 4.1 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="80b75-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="80b75-114">Перед обновлением до версии 4.5 приложение App-V 4.0 или более ранней версии должно быть удалено или обновлено до версии 4.1 или 4.1 SP1.</span><span class="sxs-lookup"><span data-stu-id="80b75-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="80b75-115">Обновление компонентов программного обеспечения на компьютерах системы Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="80b75-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="80b75-116">Перейдите к папке программы установки в сети, запустите ее из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните Setup.exe файл.</span><span class="sxs-lookup"><span data-stu-id="80b75-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="80b75-117">На странице **приветствия** мастера установки нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="80b75-118">На странице Лицензионное **соглашение** прочитайте лицензионное соглашение, установите флажок **я принимаю условия лицензионного соглашения**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="80b75-119">Когда откроется страница **установленного программного обеспечения** со списком установленных компонентов системы Application Virtualization и версией каждого компонента, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="80b75-120">На странице **предупреждение об утере сеанса** прочтите отображаемое сообщение и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="80b75-121">На странице **Подключение к базе данных конфигурации** проверьте содержимое страницы и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="80b75-122">Если отображается страница " **требуется обновление базы данных** ", требуется обновление базы данных.</span><span class="sxs-lookup"><span data-stu-id="80b75-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="80b75-123">Введите учетные данные администратора базы данных и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="80b75-124">Если эта страница не отображается, перейдите к шагу 9.</span><span class="sxs-lookup"><span data-stu-id="80b75-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="80b75-125">На странице **резервная копия базы данных** установите соответствующие флажки, чтобы выполнить резервное копирование и экспортировать ее в существующее расположение, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="80b75-126">**Важно!**  Если вы хотите восстановить предыдущую версию в случае сбоя обновления, убедитесь в том, что вы установите флажок **выполнить резервное копирование базы данных конфигурации** , иначе данные конфигурации будут потеряны.</span><span class="sxs-lookup"><span data-stu-id="80b75-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="80b75-127">Если вы хотите восстановить базу данных с помощью VSS, необходимо сначала остановить службу App-V Server на сервере управления.</span><span class="sxs-lookup"><span data-stu-id="80b75-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="80b75-128">Это следует делать на каждом сервере управления, если к одной базе данных подключено более одного сервера.</span><span class="sxs-lookup"><span data-stu-id="80b75-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="80b75-129">На первой странице **проверки пакета** Прочтите содержимое и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="80b75-130">На странице вторая **Проверка пакета** вы сможете отобразить подробные сведения о проверке пакета в окне Блокнота.</span><span class="sxs-lookup"><span data-stu-id="80b75-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="80b75-131">Чтобы просмотреть подробные сведения, нажмите кнопку **сведения**; в противном случае нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="80b75-132">На странице **готовность к обновлению программы** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80b75-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="80b75-133">На странице " **Мастер установки завершен** " нажмите кнопку **"Готово"**.</span><span class="sxs-lookup"><span data-stu-id="80b75-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="80b75-134">Повторите действия 1 – 12 на всех компьютерах, на которых вы установили консоль управления Application Virtualization или серверный компонент Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="80b75-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="80b75-135">После обновления хранилища данных вы можете возобновить нормальную работу.</span><span class="sxs-lookup"><span data-stu-id="80b75-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="80b75-136">(Хранилище данных обновляется при обновлении любого сервера или веб-службы управления App-V.)</span><span class="sxs-lookup"><span data-stu-id="80b75-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="80b75-137">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="80b75-137">Related topics</span></span>


[<span data-ttu-id="80b75-138">Рекомендации перед развертыванием и обновлением Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="80b75-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





