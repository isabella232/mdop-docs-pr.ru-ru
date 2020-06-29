---
title: Установка сервера потоковой передачи Application Virtualization Streaming Server
description: Установка сервера потоковой передачи Application Virtualization Streaming Server
author: dansimp
ms.assetid: a3065257-fb5a-4d92-98f8-7ef996c61db9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4e4f8421ef1c0e60a7df92d41be98a5d2bc0132
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817329"
---
# <span data-ttu-id="1f0e8-103">Установка сервера потоковой передачи Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="1f0e8-103">How to Install the Application Virtualization Streaming Server</span></span>


<span data-ttu-id="1f0e8-104">Сервер потоковой передачи Application Virtualization публикует приложения для клиентов.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-104">The Application Virtualization Streaming Server publishes its applications to clients.</span></span> <span data-ttu-id="1f0e8-105">В среде с балансировкой нагрузки, которая является типичной для больших развертываний, все серверы в группе серверов должны передавать в поток одинаковые приложения.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-105">In a load-balanced environment, which is typical of large deployments, all servers in a server group should stream the same applications.</span></span> <span data-ttu-id="1f0e8-106">Если серверы потоков виртуализации приложений должны передавать различные приложения, назначьте серверы разным группам серверов.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-106">If Application Virtualization Streaming Servers are to stream different applications, assign the servers to different server groups.</span></span> <span data-ttu-id="1f0e8-107">В этом случае вам также может потребоваться уменьшить емкость группы сервера.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-107">In this case, you might also have to increase a server group's capacity.</span></span>

<span data-ttu-id="1f0e8-108">Если вы выбрали конечный компьютер в сети с учетной записью, обладающей локальными правами администратора, вы можете выполнить описанные ниже действия, чтобы установить потоковый сервер Application Virtualization и назначить его соответствующей группе сервера.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-108">If you have designated a target computer on the network, with a logon account having local administrative privileges, you can use the following procedure to install the Application Virtualization Streaming Server and assign it to the appropriate server group.</span></span>

<span data-ttu-id="1f0e8-109">**Примечание**  Мастер установки может создать запись группы серверов, если она не существует, и запись о членстве сервера в потоке виртуализации приложений в этой группе.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-109">**Note** The Installation Wizard can create a server group record, if one does not exist, and a record of the Application Virtualization Streaming Server membership in this group.</span></span>

 

<span data-ttu-id="1f0e8-110">После завершения процесса установки перезагрузите сервер.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-110">After you complete the installation process, restart the server.</span></span>

**<span data-ttu-id="1f0e8-111">Установка потокового сервера Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="1f0e8-111">To install an Application Virtualization Streaming Server</span></span>**

1.  <span data-ttu-id="1f0e8-112">Убедитесь, что на целевом компьютере не установлены более ранние версии сервера потоковой передачи Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-112">Verify that no earlier versions of the Application Virtualization Streaming Server are installed on your target computer.</span></span>

    <span data-ttu-id="1f0e8-113">**Важно!**  Убедитесь, что на компьютере не установлен сервер управления App-V.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-113">**Important** Make sure that the App-V Management Server is not installed on this computer.</span></span> <span data-ttu-id="1f0e8-114">Эти два продукта невозможно установить на одном и том же компьютере.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-114">The two products cannot be installed on the same computer.</span></span>

     

2.  <span data-ttu-id="1f0e8-115">Перейдите в папку программы установки системы Application Virtualization в сети или запустите ее из сети или скопируйте ее каталог на конечный компьютер, а затем дважды щелкните файл **Setup.exe** .</span><span class="sxs-lookup"><span data-stu-id="1f0e8-115">Navigate to the location of the Application Virtualization System Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the **Setup.exe** file.</span></span>

3.  <span data-ttu-id="1f0e8-116">На странице **приветствия** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-116">On the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="1f0e8-117">На странице Лицензионное соглашение для получения условий лицензионного **соглашения** установите флажок **я принимаю условия лицензирования**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-117">On the **License Agreement** page, to accept the license terms, select **I accept the licensing terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="1f0e8-118">На странице **сведения о клиенте** укажите **имя пользователя** и организацию, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-118">On the **Customer Information** page, specify the **User name** and the organization, and then click **Next**.</span></span>

6.  <span data-ttu-id="1f0e8-119">На странице **путь установки** нажмите кнопку **Обзор**, укажите расположение, в которое вы хотите установить потоковый сервер, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-119">On the **Installation Path** page, click **Browse**, specify the location where you want to install the Streaming Server, and then click **Next**.</span></span>

7.  <span data-ttu-id="1f0e8-120">На странице **режим безопасности подключения** выберите нужный сертификат из раскрывающегося списка и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-120">On the **Connection Security Mode** page, select the desired certificate from the drop-down list, and then click **Next**.</span></span>

    <span data-ttu-id="1f0e8-121">**Примечание**  Параметр **режим защищенного подключения** требует, чтобы сервер имел сертификат сервера, предоставленный из инфраструктуры открытых ключей.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-121">**Note** The **Secure Connection Mode** setting requires the server to have a server certificate provisioned to it from a public key infrastructure.</span></span> <span data-ttu-id="1f0e8-122">Если сертификат сервера не установлен на сервере, этот параметр недоступен и не может быть выбран.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-122">If a server certificate is not installed on the server, this option is unavailable and cannot be selected.</span></span> <span data-ttu-id="1f0e8-123">Необходимо предоставить учетной записи Network Service доступ на чтение к используемому сертификату.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-123">You must grant the Network Service account read access to the certificate being used.</span></span>

     

8.  <span data-ttu-id="1f0e8-124">На странице **Настройка порта TCP** , чтобы использовать стандартный порт (554), выберите параметр **использовать порт по умолчанию (554)**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-124">On the **TCP Port Configuration** page, to use the standard port (554), select **Use default port (554)**.</span></span> <span data-ttu-id="1f0e8-125">Чтобы задать настраиваемый порт, выберите параметр **использовать настраиваемый порт**, укажите номер порта в указанном поле, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-125">To specify a custom port, select **Use custom port**, specify the port number in the field provided, and then click **Next**.</span></span>

    <span data-ttu-id="1f0e8-126">**Примечание**  При установке сервера в небезопасном сценарии вы можете использовать порт по умолчанию (554) или задать настраиваемый порт.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-126">**Note** When you install the server in a nonsecure scenario, you can use the default port (554), or you can define a custom port.</span></span>

     

9.  <span data-ttu-id="1f0e8-127">На странице **корень содержимого** укажите расположение на целевом компьютере, на котором будут сохранены SFT-файлы, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-127">On the **Content Root** page, specify the location on the target computer where SFT files will be saved, and then click **Next**.</span></span>

    <span data-ttu-id="1f0e8-128">**Примечание**  Если вы уже выделили порт HTTP или RTSP для сервера потоковой передачи виртуального приложения, вам будет предложено выбрать новый порт.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-128">**Note** If the HTTP or RTSP port for the Virtual Application Streaming Server is already allocated, you will be prompted to select a new port.</span></span> <span data-ttu-id="1f0e8-129">Укажите требуемый порт и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-129">Specify the desired port, and then click **Next**.</span></span>

     

10. <span data-ttu-id="1f0e8-130">На экране **Дополнительные настройки** введите указанные ниже сведения.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-130">On the **Advanced Setting** screen, enter the following information:</span></span>

    1.  **<span data-ttu-id="1f0e8-131">Максимальное число клиентских подключений</span><span class="sxs-lookup"><span data-stu-id="1f0e8-131">Max client connections</span></span>**

    2.  **<span data-ttu-id="1f0e8-132">Время ожидания соединения (в секундах)</span><span class="sxs-lookup"><span data-stu-id="1f0e8-132">Connection timeout (sec)</span></span>**

    3.  **<span data-ttu-id="1f0e8-133">Размер пула потоков RTSP</span><span class="sxs-lookup"><span data-stu-id="1f0e8-133">RTSP thread pool size</span></span>**

    4.  **<span data-ttu-id="1f0e8-134">Время ожидания RTSP (сек)</span><span class="sxs-lookup"><span data-stu-id="1f0e8-134">RTSP timeout (sec)</span></span>**

    5.  **<span data-ttu-id="1f0e8-135">Количество основных процессов</span><span class="sxs-lookup"><span data-stu-id="1f0e8-135">Number of core processes</span></span>**

    6.  **<span data-ttu-id="1f0e8-136">Время ожидания ядра (в секундах)</span><span class="sxs-lookup"><span data-stu-id="1f0e8-136">Core timeout (sec)</span></span>**

    7.  **<span data-ttu-id="1f0e8-137">Включение проверки подлинности пользователей</span><span class="sxs-lookup"><span data-stu-id="1f0e8-137">Enable User authentication</span></span>**

    8.  **<span data-ttu-id="1f0e8-138">Включение авторизации пользователей</span><span class="sxs-lookup"><span data-stu-id="1f0e8-138">Enable User authorization</span></span>**

    9.  **<span data-ttu-id="1f0e8-139">Размер блока кэша (КБ)</span><span class="sxs-lookup"><span data-stu-id="1f0e8-139">Cache block size (KB)</span></span>**

    10. **<span data-ttu-id="1f0e8-140">Максимальный размер кэша (МБ)</span><span class="sxs-lookup"><span data-stu-id="1f0e8-140">Maximum cache size (MB)</span></span>**

    <span data-ttu-id="1f0e8-141">**Примечание**  Потоковый сервер App-V использует разрешения файловой системы NTFS для управления доступом к приложениям в рамках общего доступа к контенту.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-141">**Note** The App-V Streaming Server uses NTFS file system permissions to control access to the applications under the Content share.</span></span> <span data-ttu-id="1f0e8-142">**Включите проверку подлинности пользователей** и **включите авторизацию пользователя** , чтобы указать, должны ли сервер проверять и применять эти списки управления доступом (ACL).</span><span class="sxs-lookup"><span data-stu-id="1f0e8-142">Use **Enable User authentication** and **Enable User authorization** to control whether the server checks and enforces those access control lists (ACLs) or not.</span></span>

     

11. <span data-ttu-id="1f0e8-143">Чтобы начать установку, на странице **готовность к установке программы** нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-143">On the **Ready to Install the Program** page, to start the installation, click **Install**.</span></span>

12. <span data-ttu-id="1f0e8-144">После завершения работы мастера **установки** нажмите кнопку **Готово**, чтобы закрыть окно мастера.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-144">On the **Installation Wizard Completed** screen, to close the wizard, click **Finish**.</span></span>

    <span data-ttu-id="1f0e8-145">**Важно!**  Для завершения установки может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-145">**Important** The installation can take several minutes to finish.</span></span> <span data-ttu-id="1f0e8-146">Сообщение о состоянии будет мигать над областью уведомлений на рабочем столе Windows, указывающей на то, что установка выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-146">A status message will flash above the Windows desktop notification area, indicating that the installation succeeded.</span></span>

    <span data-ttu-id="1f0e8-147">При появлении соответствующего запроса перезагрузка компьютера не требуется.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-147">It is not required to restart the computer when you are prompted.</span></span> <span data-ttu-id="1f0e8-148">Однако для оптимизации производительности системы рекомендуется перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-148">However, to optimize system performance, we recommend a restart.</span></span>

     

13. <span data-ttu-id="1f0e8-149">Повторите действия 1 – 12 для каждого виртуального сервера приложений, который вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="1f0e8-149">Repeat Steps 1–12 for each Virtual Application Server that you have to install.</span></span>

## <span data-ttu-id="1f0e8-150">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1f0e8-150">Related topics</span></span>


[<span data-ttu-id="1f0e8-151">Установка серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="1f0e8-151">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





