---
title: Развертывание компонентов MED-V с помощью системы электронного распространения программного обеспечения
description: Развертывание компонентов MED-V с помощью системы электронного распространения программного обеспечения
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824852"
---
# <span data-ttu-id="210b9-103">Развертывание компонентов MED-V с помощью системы электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="210b9-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="210b9-104">Электронная система распространения программного обеспечения поможет вам быстро переместить программное обеспечение на многие компьютеры через медленные или быстрые сетевые подключения.</span><span class="sxs-lookup"><span data-stu-id="210b9-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="210b9-105">В следующем разделе содержатся сведения и инструкции, которые помогут вам развернуть компоненты 2,0 для Microsoft Enterprise Virtualization (MED-V) в рамках своей организации с помощью системы распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="210b9-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="210b9-106">Примечание.</span><span class="sxs-lookup"><span data-stu-id="210b9-106">Note</span></span>**  
<span data-ttu-id="210b9-107">Независимо от того, какое решение используется для распространения программного обеспечения, вам должны быть знакомы требования, предъявляемые с конкретным решением.</span><span class="sxs-lookup"><span data-stu-id="210b9-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="210b9-108">Если вы используете System Center Configuration Manager 2007 R2 или более поздней версии, ознакомьтесь с [библиотекой документации Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) в технической библиотеке Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="210b9-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="210b9-109">Важно.</span><span class="sxs-lookup"><span data-stu-id="210b9-109">Important</span></span>**  
<span data-ttu-id="210b9-110">Если вы используете System Center Configuration Manager 2007 с пакетом обновления 2 (SP2), а ваши рабочие области MED-V настроены для работы в режиме **NAT** , виртуальные машины классифицируются как Интернет-клиенты и не могут найти ближайшие точки распространения для загрузки содержимого.</span><span class="sxs-lookup"><span data-stu-id="210b9-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="210b9-111">[Исправление для улучшения функциональности виртуальных машин, управляемых с помощью MED-](https://go.microsoft.com/fwlink/?LinkId=201088) v ( https://go.microsoft.com/fwlink/?LinkId=201088) добавляются новые возможности на виртуальные машины, управляемые med-v и настроенные для работы в режиме **NAT** .</span><span class="sxs-lookup"><span data-stu-id="210b9-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="210b9-112">Новая функция позволяет виртуальным машинам получить доступ к ближайшим точкам распространения.</span><span class="sxs-lookup"><span data-stu-id="210b9-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="210b9-113">Таким образом, администратор может управлять виртуальной машиной и ведущим компьютером точно так же.</span><span class="sxs-lookup"><span data-stu-id="210b9-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="210b9-114">Сначала необходимо установить это исправление на сервере сайта, а затем на клиенте.</span><span class="sxs-lookup"><span data-stu-id="210b9-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="210b9-115">Обновление доступно для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="210b9-115">The update is publicly available.</span></span> <span data-ttu-id="210b9-116">Тем не менее, вам может быть предложено принимать условия соглашения для служб Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="210b9-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="210b9-117">Следуйте указаниям на последовательных страницах, чтобы получить это исправление.</span><span class="sxs-lookup"><span data-stu-id="210b9-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="210b9-118">Примечание.</span><span class="sxs-lookup"><span data-stu-id="210b9-118">Note</span></span>**  
<span data-ttu-id="210b9-119">Прежде чем развертывать компоненты MED-V с помощью системы распространения программного обеспечения, необходимо установить диспетчер рабочих областей MED-V и выполнить сборку рабочих областей med-v.</span><span class="sxs-lookup"><span data-stu-id="210b9-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="210b9-120">Дополнительные сведения о том, как подготовить образ и выполнить построение рабочих областей MED-V, приведены в статье [операции для MED-v](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="210b9-121">Развертывание компонентов MED-V с помощью системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="210b9-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="210b9-122">Определите группу компьютеров и пользователей в системе электронной рассылки программного обеспечения как целевые наборы компьютеров и пользователей.</span><span class="sxs-lookup"><span data-stu-id="210b9-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="210b9-123">Создайте пакеты для каждого установочного файла Microsoft, который нужно распространить.</span><span class="sxs-lookup"><span data-stu-id="210b9-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="210b9-124">Ниже указаны необходимые файлы и порядок их установки.</span><span class="sxs-lookup"><span data-stu-id="210b9-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="210b9-125">**Операционная система Windows Virtual PC** — если она еще не установлена (требуется перезагрузка компьютера).</span><span class="sxs-lookup"><span data-stu-id="210b9-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="210b9-126">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="210b9-127">Добавлены **и обновленные виртуальные компьютеры Windows** — если они еще не установлены.</span><span class="sxs-lookup"><span data-stu-id="210b9-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="210b9-128">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="210b9-129">**Установочный файл агента узла MED-v** — Установка агента узла (MED-V \ _HostAgent \ _setup установочный файл).</span><span class="sxs-lookup"><span data-stu-id="210b9-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="210b9-130">Дополнительные сведения [можно найти в разделе Установка агента узла MED-V вручную](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="210b9-131">Warning</span><span class="sxs-lookup"><span data-stu-id="210b9-131">Warning</span></span>**  
        <span data-ttu-id="210b9-132">Перед установкой агента узла MED-V закройте Internet Explorer, в противном случае конфликты могут возникать позже с перенаправлением URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="210b9-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="210b9-133">Вы также можете сделать это, указав компьютер во время распространения.</span><span class="sxs-lookup"><span data-stu-id="210b9-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="210b9-134">**Программа установки рабочей области MED-v, VHD и исполняемый файл Setup** создаются в **упаковщике рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="210b9-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="210b9-135">Дополнительные сведения можно найти [в разделе Создание пакета рабочей области для MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="210b9-136">Важно.</span><span class="sxs-lookup"><span data-stu-id="210b9-136">Important</span></span>**  
        <span data-ttu-id="210b9-137">Сжатый файл виртуального жесткого диска (. MEDV) и исполняемая программа установки (setup.exe) должны находиться в той же папке, что и в установщике рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="210b9-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="210b9-138">Затем установите установщик рабочей области MED-V, запустив setup.exe.</span><span class="sxs-lookup"><span data-stu-id="210b9-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="210b9-139">Совет</span><span class="sxs-lookup"><span data-stu-id="210b9-139">Tip</span></span>**  
        <span data-ttu-id="210b9-140">Из-за проблем, которые могут возникнуть при установке MED-V из сетевого расположения, рекомендуется скопировать файлы настройки рабочей области для MED-V на локальном компьютере, а затем запустить setup.exe.</span><span class="sxs-lookup"><span data-stu-id="210b9-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="210b9-141">Настройте пакеты для работы в режиме молчания (вмешательство пользователя не требуется).</span><span class="sxs-lookup"><span data-stu-id="210b9-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="210b9-142">При запуске в автоматическом режиме удаляется запрос на закрытие Internet Explorer, если он запущен, и запрос на запуск агента хоста MED-V.</span><span class="sxs-lookup"><span data-stu-id="210b9-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="210b9-143">Оба действия выполняются при перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="210b9-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="210b9-144">Примечание.</span><span class="sxs-lookup"><span data-stu-id="210b9-144">Note</span></span>**  
    <span data-ttu-id="210b9-145">Для установки Virtual PC для Windows требуется перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="210b9-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="210b9-146">Вы можете создать один процесс установки и установить все компоненты одновременно, если отключить его и игнорировать предварительные требования, необходимые для установки MED-V.</span><span class="sxs-lookup"><span data-stu-id="210b9-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="210b9-147">Это также можно сделать с помощью аргументов командной строки.</span><span class="sxs-lookup"><span data-stu-id="210b9-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="210b9-148">Пример этих аргументов можно найти [в разделе Установка компонентов MED-V с помощью пакетного файла](#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="210b9-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="210b9-149">MED-V автоматически запускается при перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="210b9-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="210b9-150">Перед установкой Windows Virtual PC установите MED-V и ее компоненты.</span><span class="sxs-lookup"><span data-stu-id="210b9-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="210b9-151">Пример пакетного файла приведен ниже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="210b9-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="210b9-152">Важно.</span><span class="sxs-lookup"><span data-stu-id="210b9-152">Important</span></span>**  
    <span data-ttu-id="210b9-153">Выберите параметр **игнорировать \ _PREREQUISITES** , как показано в пакетном файле примера, чтобы можно было установить компоненты MED-V до необходимых компонентов VPC.</span><span class="sxs-lookup"><span data-stu-id="210b9-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="210b9-154">Установите компоненты MED-V в соответствии с этим заказом, чтобы обеспечить единую перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="210b9-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="210b9-155">Определите другие требования, необходимые для установки, и для системы распространения программного обеспечения, например целевых платформ и свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="210b9-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="210b9-156">Назначьте пакеты целевому набору компьютеров и пользователей.</span><span class="sxs-lookup"><span data-stu-id="210b9-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="210b9-157">По мере выполнения компьютеров клиент системы распространения программного обеспечения распознает, что новые пакеты доступны, и начнет устанавливать пакеты в соответствии с определением и требованиями.</span><span class="sxs-lookup"><span data-stu-id="210b9-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="210b9-158">Установка должна выполняться последовательно в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="210b9-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="210b9-159">Мы рекомендуем выполнять эти действия как один процесс, который не требует перезапуска, пока не будут установлены все пакеты.</span><span class="sxs-lookup"><span data-stu-id="210b9-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="210b9-160">После завершения установки перезагрузите обновленные компьютеры.</span><span class="sxs-lookup"><span data-stu-id="210b9-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="210b9-161">В зависимости от системы распространения программного обеспечения вы можете запланировать перезагрузку компьютера, или конечные пользователи смогут вручную перезапустить компьютеры во время их обычной работы.</span><span class="sxs-lookup"><span data-stu-id="210b9-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="210b9-162">После перезапуска компьютера MED-V автоматически запускается после входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="210b9-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="210b9-163">В первый раз при первом запуске MED-V запускается первая Настройка.</span><span class="sxs-lookup"><span data-stu-id="210b9-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="210b9-164">При первом запуске программы установки может потребоваться несколько минут, в зависимости от размера указанного виртуального жесткого диска и количества политик, примененных к рабочей области MED-V при запуске.</span><span class="sxs-lookup"><span data-stu-id="210b9-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="210b9-165">Конечный пользователь может отслеживать ход выполнения, проследите за помощью значка MED-V в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="210b9-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="210b9-166">Дополнительные сведения о первой настройке можно найти в статье [Обзор развертывания для MED-V 2,0](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="210b9-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="210b9-167">Установка компонентов MED-V с помощью пакетного файла</span><span class="sxs-lookup"><span data-stu-id="210b9-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="210b9-168">Запустите установку из командной строки с учетными данными администратора.</span><span class="sxs-lookup"><span data-stu-id="210b9-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="210b9-169">Разместите каждый компонент в одном каталоге.</span><span class="sxs-lookup"><span data-stu-id="210b9-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="210b9-170">При запуске из общей сетевой папке требуется более длительное время для распаковки файла. MEDV.</span><span class="sxs-lookup"><span data-stu-id="210b9-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="210b9-171">Рекомендуется указывать, что Virtual PC и Windows Virtual PC Hotfix устанавливаются после агента узла MED-V и файлов пакета MED-V Workspace.</span><span class="sxs-lookup"><span data-stu-id="210b9-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="210b9-172">Это означает, что при установке центра обновления Windows не будет вмешательство в процесс установки, если требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="210b9-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="210b9-173">Перезагрузите компьютер после завершения выполнения пакетного файла.</span><span class="sxs-lookup"><span data-stu-id="210b9-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="210b9-174">После перезагрузки пользователю будет предложено запустить программу установки в первый раз и завершить настройку MED-V.</span><span class="sxs-lookup"><span data-stu-id="210b9-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="210b9-175">В приведенном ниже примере с заданными параметрами показано, как установить 64-разрядные компоненты MED-V в одном процессе.</span><span class="sxs-lookup"><span data-stu-id="210b9-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="210b9-176">Аргумент</span><span class="sxs-lookup"><span data-stu-id="210b9-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="210b9-177">Описание</span><span class="sxs-lookup"><span data-stu-id="210b9-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="210b9-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="210b9-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="210b9-179">Запрещает установку виртуальных ПК под управлением Windows и Windows Virtual PC Update из перезапуска главного компьютера.</span><span class="sxs-lookup"><span data-stu-id="210b9-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="210b9-180">параметрами</span><span class="sxs-lookup"><span data-stu-id="210b9-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="210b9-181">Установка компонентов MED-V в тихом режиме без взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="210b9-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="210b9-182">/Qn</span><span class="sxs-lookup"><span data-stu-id="210b9-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="210b9-183">Устанавливаются компоненты MED-V без пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="210b9-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="210b9-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="210b9-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="210b9-185">Установка без проверки на наличие Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="210b9-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="210b9-186">Примечание.</span><span class="sxs-lookup"><span data-stu-id="210b9-186">Note</span></span></strong><br/><p><span data-ttu-id="210b9-187">Указывайте этот аргумент только в том случае, если вы устанавливаете Windows Virtual PC в рамках этой установки.</span><span class="sxs-lookup"><span data-stu-id="210b9-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="210b9-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="210b9-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="210b9-189">Принудительно устанавливает рабочую область MED-V и предотвращает любые запросы, которые она может создать.</span><span class="sxs-lookup"><span data-stu-id="210b9-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="210b9-190">Пример</span><span class="sxs-lookup"><span data-stu-id="210b9-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="210b9-191">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="210b9-191">Related topics</span></span>


[<span data-ttu-id="210b9-192">Обзор развертывания MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="210b9-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="210b9-193">Развертывание компонентов MED-V</span><span class="sxs-lookup"><span data-stu-id="210b9-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)









