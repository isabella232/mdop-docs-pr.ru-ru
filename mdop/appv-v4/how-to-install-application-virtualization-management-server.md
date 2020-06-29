---
title: Установка сервера Application Virtualization Management Server
description: Установка сервера Application Virtualization Management Server
author: dansimp
ms.assetid: 8184be79-8c27-4328-a3c1-183791b5556c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfd06ee1d2448990d5a740f3d59b0e5e4b45be4d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817362"
---
# <span data-ttu-id="4d1a4-103">Установка сервера Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="4d1a4-103">How to Install Application Virtualization Management Server</span></span>


<span data-ttu-id="4d1a4-104">Сервер управления виртуализацией приложений публикует свои приложения для клиентов.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-104">The Application Virtualization Management Server publishes its applications to clients.</span></span> <span data-ttu-id="4d1a4-105">В среде с балансировкой нагрузки, которая является типичной для больших развертываний, все серверы в группе серверов должны передавать в поток одинаковые приложения.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="4d1a4-106">Если серверы управления виртуализацией приложений должны публиковать различные приложения, назначьте серверы разным группам серверов.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-106">If Application Virtualization Management Servers are to publish different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="4d1a4-107">В этом случае вам также может потребоваться уменьшить емкость группы сервера.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-107">In this case, you also might need to increase a server group's capacity.</span></span>

<span data-ttu-id="4d1a4-108">Если вы выбрали конечный компьютер в сети, а учетная запись имеет права локального администратора, вы можете использовать описанную ниже процедуру, чтобы установить сервер управления виртуализацией приложений и назначить его соответствующей группе серверов.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-108">If you have designated a target computer on the network, with a login account having local Administrator privileges, you can use the following procedure to install the Application Virtualization Management Server and assign it to the appropriate server group.</span></span>

**<span data-ttu-id="4d1a4-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-109">Note</span></span>**  
<span data-ttu-id="4d1a4-110">Мастер установки может создать запись группы серверов, если она не существует, а также запись о членстве сервера управления виртуализацией приложений в этой группе.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-110">The Installation Wizard can create a server group record, if one does not exist, as well as a record of the Application Virtualization Management Server's membership in this group.</span></span>



<span data-ttu-id="4d1a4-111">После завершения процесса установки перезагрузите сервер.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-111">After you complete the installation process, reboot the server.</span></span>

**<span data-ttu-id="4d1a4-112">Установка сервера управления виртуализацией приложений</span><span class="sxs-lookup"><span data-stu-id="4d1a4-112">To install an Application Virtualization Management Server</span></span>**

1.  <span data-ttu-id="4d1a4-113">Проверьте и, при необходимости, удалите предыдущие версии сервера управления виртуализации приложений, установленных на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-113">Verify and, if necessary, uninstall previous versions of the Application Virtualization Management Server that are installed on the target computer.</span></span>

2.  <span data-ttu-id="4d1a4-114">Чтобы открыть мастер **установки сервера управления виртуализацией приложений (Майкрософт** ), перейдите в папку, в которой находится программа **setup.exe** Application Virtualization в сети, либо запустите ее из сети, либо скопируйте ее каталог на конечный компьютер, а затем дважды щелкните файл **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="4d1a4-114">To open the **Microsoft Application Virtualization Management Server installation** wizard, navigate to the location of the Application Virtualization System **setup.exe** program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="4d1a4-115">На странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-115">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="4d1a4-116">На странице **лицензионное соглашение ознакомьтесь** с лицензионным соглашением и, чтобы принимаю лицензионное соглашение, выберите **я принимаю условия лицензионного**соглашения.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-116">On the **License Agreement** page, read the license agreement and, to accept the license agreement, select **I accept the license terms and conditions**.</span></span> <span data-ttu-id="4d1a4-117">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-117">Click **Next**.</span></span>

5.  <span data-ttu-id="4d1a4-118">На странице **зарегистрировать сведения** необходимо ввести имя пользователя и **организацию**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-118">On the **Registering Information** page, you must enter the user name and the **Organization**.</span></span> <span data-ttu-id="4d1a4-119">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-119">Click **Next**.</span></span>

6.  <span data-ttu-id="4d1a4-120">На странице **Настройка типа** выберите пункт **Настраиваемая**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-120">On the **Setup Type** page, select **Custom**.</span></span> <span data-ttu-id="4d1a4-121">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-121">Click **Next**.</span></span> <span data-ttu-id="4d1a4-122">На странице **Выборочная настройка** отмените выбор всех компонентов системы Application Virtualization, кроме **сервера Application Virtualization**, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-122">On the **Custom Setup** page, deselect all Application Virtualization System components except **Application Virtualization Server**, and then click **Next**.</span></span>

    **<span data-ttu-id="4d1a4-123">Осторожны</span><span class="sxs-lookup"><span data-stu-id="4d1a4-123">Caution</span></span>**  
    <span data-ttu-id="4d1a4-124">Если компонент уже установлен на компьютере, то при отмене выбора его в окне **Выборочная настройка** компонент автоматически удаляется.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-124">If a component is already installed on the computer, when you deselect it in the **Custom Setup** window, the component is automatically uninstalled.</span></span>



7.  <span data-ttu-id="4d1a4-125">На странице **база данных конфигурации** выберите сервер базы данных из списка доступных серверов или добавьте сервер, выбрав команду **использовать следующее имя узла** и указав **имя сервера** и данные о **номере порта** .</span><span class="sxs-lookup"><span data-stu-id="4d1a4-125">On the **Configuration Database** page, select a database server from the list of available servers or add a server by selecting **Use the following host name** and specifying the **Server Name** and **Port Number** data.</span></span> <span data-ttu-id="4d1a4-126">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-126">Click **Next**.</span></span>

    **<span data-ttu-id="4d1a4-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-127">Note</span></span>**  
    <span data-ttu-id="4d1a4-128">Сервер управления виртуализацией приложений не поддерживает SQL с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-128">The Application Virtualization Management Server does not support case sensitive SQL.</span></span>



~~~
If a database is available, click the radio button, select the database from the list, and then click **Next**. Setup will upgrade it to this newer version. If the name does not appear in the list, enter the name in the space provided.

**Note**  
When naming a server, do not use the backslash character (/) in the server name.

If you need to install a database, see [How to Install a Database](how-to-install-a-database.md). If you would like to create a new database for this version, select **Create a new database** and specify the name that will be assigned to the new database. You can also specify a new location for the database by selecting the check box and entering the path.
~~~



8. <span data-ttu-id="4d1a4-129">На странице **режим безопасности подключения** выберите нужный сертификат из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-129">On the **Connection Security Mode** page, select the desired certificate from the drop-down list.</span></span> <span data-ttu-id="4d1a4-130">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-130">Click **Next**.</span></span>

   **<span data-ttu-id="4d1a4-131">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-131">Note</span></span>**  
   <span data-ttu-id="4d1a4-132">Параметр **режим защищенного подключения** требует, чтобы сервер имел сертификат сервера, предоставленный из инфраструктуры открытых ключей.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-132">The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="4d1a4-133">Если сертификат сервера не установлен на сервере, этот параметр недоступен и не может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-133">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="4d1a4-134">Необходимо предоставить учетной записи Network Service доступ на чтение к используемому сертификату.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-134">You must grant the Network Service account read access to the certificate being used.</span></span>



9. <span data-ttu-id="4d1a4-135">На странице **Настройка порта TCP** , чтобы использовать порт по умолчанию (554), выберите **использовать порт по умолчанию (554)**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-135">On the **TCP Port Configuration** page, to use the default port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="4d1a4-136">Чтобы задать настраиваемый порт, выберите параметр **использовать настраиваемый порт** и укажите номер порта, который будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-136">To specify a custom port, select **Use custom port** and specify the port number that will be used.</span></span> <span data-ttu-id="4d1a4-137">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-137">Click **Next**.</span></span>

   **<span data-ttu-id="4d1a4-138">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-138">Note</span></span>**  
   <span data-ttu-id="4d1a4-139">При установке сервера в незащищенной среде вы можете использовать порт по умолчанию (554) или задать настраиваемый порт.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-139">When you install the server in a nonsecure environment, you can use the default port (554) or you can define a custom port.</span></span>



10. <span data-ttu-id="4d1a4-140">На странице **Группа администраторов** укажите имя группы безопасности, авторизованной для управления этим сервером в **поле Имя группы**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-140">On the **Administrator Group** page, specify the name of the security group authorized to manage this server in **Group Name**.</span></span> <span data-ttu-id="4d1a4-141">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-141">Click **Next**.</span></span> <span data-ttu-id="4d1a4-142">Убедитесь в том, что группа указана, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-142">Confirm the group specified and click **Next**.</span></span>

11. <span data-ttu-id="4d1a4-143">На странице " **Группа поставщика по умолчанию** " укажите имя группы поставщика по умолчанию, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-143">On the **Default Provider Group** page, specify the name of the default provider group, and then click **Next**.</span></span>

12. <span data-ttu-id="4d1a4-144">На странице **путь к содержимому** укажите расположение на целевом компьютере, на котором будут сохранены SFT-файлы, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-144">On the **Content Path** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

   **<span data-ttu-id="4d1a4-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-145">Note</span></span>**  
   <span data-ttu-id="4d1a4-146">Если вы уже выделили порт HTTP или RTSP для сервера управления, вам будет предложено выбрать новый порт.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-146">If the HTTP or RTSP port for the Management Server is already allocated, you will be prompted to choose a new port.</span></span> <span data-ttu-id="4d1a4-147">Выберите нужный порт и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-147">Select the desired port, and then click **Next**.</span></span>



13. <span data-ttu-id="4d1a4-148">На странице **готовности к установке программы** установите сервер управления виртуализацией приложений и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-148">On the **Ready to Install the Program** page, to install the Application Virtualization Management Server, click **Install**.</span></span>

   **<span data-ttu-id="4d1a4-149">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-149">Note</span></span>**  
   <span data-ttu-id="4d1a4-150">Если при попытке выполнить это действие появляется сообщение об ошибке 25120, необходимо включить **сценарии и средства управления**IIS.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-150">If error 25120 is displayed when you try to complete this step, you need to enable IIS **Management Scripts and Tools**.</span></span> <span data-ttu-id="4d1a4-151">Чтобы включить эту функцию Windows, откройте панель управления " **программы и компоненты** ", выберите пункт **Включение или отключение компонентов Windows**и перейдите к **службам IIS.**</span><span class="sxs-lookup"><span data-stu-id="4d1a4-151">To enable this Windows feature, open the **Programs and Features** control panel, select **Turn Windows features on or off**, and navigate to **Internet Information Services.**</span></span>

   <span data-ttu-id="4d1a4-152">В разделе **средства управления веб-сайтами**включите **сценарии и инструменты управления IIS**.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-152">Under **Web Management Tools**, enable **IIS Management Scripts and Tools**.</span></span>



14. <span data-ttu-id="4d1a4-153">После завершения работы мастера **установки** нажмите кнопку **Готово**, чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-153">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

   **<span data-ttu-id="4d1a4-154">Важно.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-154">Important</span></span>**  
   <span data-ttu-id="4d1a4-155">Для завершения установки может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-155">The installation can take a few minutes to finish.</span></span> <span data-ttu-id="4d1a4-156">Сообщение о состоянии будет мигать над областью уведомлений на рабочем столе Windows, указывающей на то, что установка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-156">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

   <span data-ttu-id="4d1a4-157">При появлении соответствующего запроса вам не нужно перезагружать компьютер.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-157">It is not necessary to reboot the computer when prompted.</span></span> <span data-ttu-id="4d1a4-158">Однако для оптимизации производительности системы рекомендуется выполнить перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="4d1a4-158">However, to optimize system performance, a reboot is recommended.</span></span>



## <span data-ttu-id="4d1a4-159">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4d1a4-159">Related topics</span></span>


[<span data-ttu-id="4d1a4-160">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="4d1a4-160">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)









