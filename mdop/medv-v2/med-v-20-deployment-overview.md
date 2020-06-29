---
title: Обзор развертывания MED-V 2.0
description: Обзор развертывания MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826109"
---
# <span data-ttu-id="4bd6e-103">Обзор развертывания MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="4bd6e-103">MED-V 2.0 Deployment Overview</span></span>


<span data-ttu-id="4bd6e-104">В этом разделе приводятся общие сведения и инструкции по установке и развертыванию Microsoft Enterprise Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-104">This section provides general information and instructions about how to install and deploy Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="4bd6e-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="4bd6e-105">Overview</span></span>


<span data-ttu-id="4bd6e-106">MED-V 2,0 основывается на модели приложения, в которой те же методы, которые используются для развертывания приложений, можно использовать для развертывания и управления MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-106">MED-V 2.0 is based on an application model, where the same methods that you use to deploy applications can be used to deploy and manage MED-V.</span></span> <span data-ttu-id="4bd6e-107">Развернутое решение для MED-V включает два компонента: агент узла MED-V и гостевой агент.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-107">A deployed MED-V solution includes two components: the MED-V Host Agent and Guest Agent.</span></span> <span data-ttu-id="4bd6e-108">Агент узла MED-V установлен на рабочем столе Windows 7, а Гостевой агент MED-V установлен в Windows XP в рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-108">The MED-V Host Agent is installed on the Windows 7 desktop and the MED-V Guest Agent is installed on Windows XP inside the MED-V workspace.</span></span> <span data-ttu-id="4bd6e-109">MED-V также включает в себя диспетчер рабочих областей MED-V, который предоставляет сведения и инструменты, необходимые для создания и настройки рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-109">MED-V also includes a MED-V Workspace Packager that provides the information and tools necessary for creating and configuring MED-V workspaces.</span></span>

**<span data-ttu-id="4bd6e-110">Важно.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-110">Important</span></span>**  
<span data-ttu-id="4bd6e-111">В целях MED-V для всех пользователей поддерживается только установка диспетчера рабочих областей MED-V, агента хоста MED-v и рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-111">MED-V only supports the installation of the MED-V Workspace Packager, the MED-V Host Agent, and the MED-V workspace for all users.</span></span> <span data-ttu-id="4bd6e-112">Установка MED-V для текущего пользователя только путем выбора параметра **ALLUSERS = ""** приводит к сбоям при установке компонентов и настройке рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-112">Installing MED-V for the current user only by selecting **ALLUSERS=””** causes failures in the installation of the components and in the setup of the MED-V workspace.</span></span>



### <span data-ttu-id="4bd6e-113">Файлы установки для MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-113">The MED-V Installation Files</span></span>

<span data-ttu-id="4bd6e-114">MED-V включает следующие установочные файлы, необходимые для работы с MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-114">MED-V includes the following installation files, required for running MED-V:</span></span>

**<span data-ttu-id="4bd6e-115">Установочный файл агента узла MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-115">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="4bd6e-116">Установочный файл агента узла имеет имя MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-116">The Host Agent installation file is named MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="4bd6e-117">Этот файл распространяется на все подходящие компьютеры конечных пользователей в рамках развертывания MED-V на уровне предприятия.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-117">This file is distributed and installed on each relevant end-user computer as part of your enterprise-wide deployment of MED-V.</span></span>

**<span data-ttu-id="4bd6e-118">Установочный файл упаковщика рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-118">The MED-V Workspace Packager Installation File</span></span>**

<span data-ttu-id="4bd6e-119">Установочный файл упаковщика рабочей области MED-V имеет имя MED-V\_WorkspacePackager\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-119">The MED-V Workspace Packager installation file is named MED-V\_WorkspacePackager\_Setup.exe.</span></span> <span data-ttu-id="4bd6e-120">Используйте этот файл, чтобы установить диспетчер рабочих областей MED-V на компьютер, на котором у вас есть права и разрешения администратора.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-120">Use this file to install the MED-V Workspace Packager on a computer where you have administrator rights and permissions.</span></span> <span data-ttu-id="4bd6e-121">Администратор на рабочем столе использует диспетчер рабочих областей MED-V для создания рабочих областей MED-V и управления ими.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-121">The desktop administrator uses the MED-V Workspace Packager to create and manage MED-V workspaces.</span></span>

**<span data-ttu-id="4bd6e-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-122">Note</span></span>**  
<span data-ttu-id="4bd6e-123">Гостевой агент MED-V устанавливается автоматически при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-123">The MED-V Guest Agent is installed automatically during first time setup.</span></span>



### <span data-ttu-id="4bd6e-124">Процесс развертывания MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-124">The MED-V Deployment Process</span></span>

<span data-ttu-id="4bd6e-125">Ниже приведен общий обзор процесса установки и развертывания для MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-125">The following is a high-level overview of the MED-V installation and deployment process:</span></span>

1.  <span data-ttu-id="4bd6e-126">Установите диспетчер рабочих областей MED-V на компьютере, на котором у вас есть учетные данные администратора, и что вы будете использовать для создания пакетов рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-126">Install the MED-V Workspace Packager on the computer where you have administrative credentials and that you will be using to build the MED-V workspace packages.</span></span> <span data-ttu-id="4bd6e-127">Дополнительные сведения можно найти [в разделе Установка диспетчера рабочих областей MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-127">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

2.  <span data-ttu-id="4bd6e-128">Подготовьте образ MED-V и создайте пакеты рабочей области для MED-v с помощью диспетчера рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-128">Prepare your MED-V image and create your MED-V workspace packages by using the MED-V Workspace Packager.</span></span> <span data-ttu-id="4bd6e-129">Дополнительные сведения можно найти в разделе [операции для MED-V](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-129">For more information, see [Operations for MED-V](operations-for-med-v.md).</span></span>

3.  <span data-ttu-id="4bd6e-130">Развертывайте необходимые компоненты MED-V во всей Организации.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-130">Deploy the required MED-V components throughout your enterprise.</span></span> <span data-ttu-id="4bd6e-131">В качестве обязательных компонентов MED-V используются виртуальные компьютеры Windows, агент хоста MED-V и Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-131">The required components of MED-V are Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span>

**<span data-ttu-id="4bd6e-132">Важно.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-132">Important</span></span>**  
<span data-ttu-id="4bd6e-133">Установка компонентов MED-V требует учетных данных администратора.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-133">Installation of the MED-V components requires administrative credentials.</span></span> <span data-ttu-id="4bd6e-134">Если конечный пользователь устанавливает MED-V, ему будет предложено ввести учетные данные администратора.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-134">If an end user is installing MED-V, they are prompted to enter administrative credentials.</span></span> <span data-ttu-id="4bd6e-135">Кроме того, учетные данные администратора могут быть предоставлены в контексте, если установка выполняется с помощью электронной системы программного обеспечения (ESD).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-135">Alternately, administrative credentials can be provided in context if you are installing by using an electronic software distribution (ESD) system.</span></span>



### <span data-ttu-id="4bd6e-136">Компоненты MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-136">The MED-V Components</span></span>

<span data-ttu-id="4bd6e-137">Компоненты MED-V, развертываемые в рамках всего предприятия, состоят из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="4bd6e-137">The MED-V components that you deploy throughout your enterprise consist of the following:</span></span>

**<span data-ttu-id="4bd6e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4bd6e-138">Windows Virtual PC</span></span>**

<span data-ttu-id="4bd6e-139">Функции MED-V в изображениях виртуальных ПК на основе Windows для решения совместимости.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-139">MED-V functions inside Windows Virtual PC images for its compatibility solution.</span></span> <span data-ttu-id="4bd6e-140">Windows Virtual PC и обновление для Windows 7 (KB977206) являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-140">Windows Virtual PC and the update for Windows 7 (KB977206) are required.</span></span> <span data-ttu-id="4bd6e-141">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-141">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

**<span data-ttu-id="4bd6e-142">Установочный файл агента узла MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-142">The MED-V Host Agent Installation File</span></span>**

<span data-ttu-id="4bd6e-143">MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-143">MED-V\_HostAgent\_Setup.exe.</span></span>

**<span data-ttu-id="4bd6e-144">Установочные файлы рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-144">The MED-V Workspace Installation Files</span></span>**

<span data-ttu-id="4bd6e-145">Установочные файлы рабочей области MED-V создаются при создании пакета рабочей области MED-V, который включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="4bd6e-145">The MED-V workspace installation files are created when you build your MED-V workspace package that consists of the following:</span></span>

<span data-ttu-id="4bd6e-146">Исполняемая программа setup.exe, выполняющая установку рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-146">A setup.exe executable program that executes the MED-V workspace installation</span></span>

<span data-ttu-id="4bd6e-147">&lt;Установщик MED-V \ _workspace \ _name &gt; . msi</span><span class="sxs-lookup"><span data-stu-id="4bd6e-147">A &lt;MED-V\_workspace\_name&gt;.msi installer</span></span>

<span data-ttu-id="4bd6e-148">&lt;Файл VHD: _filename &gt; . MEDV, который является сжатым виртуальным жестким диском</span><span class="sxs-lookup"><span data-stu-id="4bd6e-148">A &lt;VHD\_filename&gt;.medv file, which is the compressed virtual hard disk</span></span>

<span data-ttu-id="4bd6e-149">Файлы параметров конфигурации ( &lt; Рабочая область \ _name &gt; . reg и &lt; Workspace \ _name &gt; . ps1)</span><span class="sxs-lookup"><span data-stu-id="4bd6e-149">The files for configuration settings (&lt;workspace\_name&gt;.reg and &lt;workspace\_name&gt;.ps1)</span></span>

<span data-ttu-id="4bd6e-150">Чтобы развернуть MED-V, скопируйте все необходимые файлы установки на узел компьютера или в общий доступ, доступ к которому может получить узел компьютера.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-150">To deploy MED-V, copy all the required installation files to the host computer or to a share that can be accessed by the host computer.</span></span> <span data-ttu-id="4bd6e-151">Запустите файлы установки компонента для Windows Virtual PC, агента хостов MED-V и рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-151">Run the component installation files for Windows Virtual PC, the MED-V Host Agent, and the MED-V workspace.</span></span> <span data-ttu-id="4bd6e-152">Затем запустите агент узла MED-V, чтобы выполнить первый раз при установке MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-152">Then start the MED-V Host Agent to complete the first time setup of MED-V.</span></span>

<span data-ttu-id="4bd6e-153">Вы можете выполнить установку вручную.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-153">You can perform the installation manually.</span></span> <span data-ttu-id="4bd6e-154">Однако мы рекомендуем использовать электронный метод распространения программного обеспечения для автоматизации развертывания компонентов.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-154">However, we recommend that you use an electronic software distribution method to automate the deployment of the components.</span></span> <span data-ttu-id="4bd6e-155">Дополнительные сведения можно найти в разделе [Развертывание рабочей области MED-V с помощью электронной системы распространения программного обеспечения](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-155">For more information, see [How to Deploy a MED-V Workspace Through an Electronic Software Distribution System](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).</span></span>

**<span data-ttu-id="4bd6e-156">Примечание.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-156">Note</span></span>**  
<span data-ttu-id="4bd6e-157">Сведения о доступных аргументах командной строки для управления параметрами установки можно найти в разделе [Параметры командной строки для установочных файлов MED-V](command-line-options-for-med-v-installation-files.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-157">For information about available command-line arguments to control install options, see [Command-Line Options for MED-V Installation Files](command-line-options-for-med-v-installation-files.md).</span></span>



## <span data-ttu-id="4bd6e-158">Действия по развертыванию</span><span class="sxs-lookup"><span data-stu-id="4bd6e-158">Deployment Steps</span></span>


<span data-ttu-id="4bd6e-159">При развертывании MED-V по всему предприятию необходимо учитывать два основных аспекта: Установка и первая Настройка.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-159">When you deploy MED-V throughout your enterprise, there are two main considerations: installation and first time setup.</span></span>

### <span data-ttu-id="4bd6e-160">Установка</span><span class="sxs-lookup"><span data-stu-id="4bd6e-160">Installation</span></span>

1.  <span data-ttu-id="4bd6e-161">**Windows Virtual PC** – во время установки для Windows 7 (KB977206) на компьютере с операционной системой MED-V проверяются виртуальные компьютеры Windows и необходимые обновления.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-161">**Windows Virtual PC** - During installation, MED-V checks for Windows Virtual PC and its required update for Windows 7 (KB977206).</span></span> <span data-ttu-id="4bd6e-162">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-162">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    <span data-ttu-id="4bd6e-163">Вы можете установить эти компоненты в установках Windows 7 перед установкой MED-V или установить их в рамках дистрибутива MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-163">You can install these as part of the Windows 7 installations before you install MED-V, or you can install them as part of the MED-V distribution.</span></span> <span data-ttu-id="4bd6e-164">Однако MED-V не включает механизм для развертывания; они должны быть развернуты с помощью электронного распространения программного обеспечения или в составе образа Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-164">However, MED-V does not include a mechanism for their deployment; they must be deployed by using an electronic software distribution (ESD) system or as part of the Windows 7 image.</span></span>

    **<span data-ttu-id="4bd6e-165">Важно.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-165">Important</span></span>**  
    <span data-ttu-id="4bd6e-166">При установке компонентов MED-V с помощью пакетного файла рекомендуется указать, что Windows Virtual PC и Windows Virtual PC Hotfix устанавливаются после агента узла MED-V и файлов пакета MED-V Workspace.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-166">When you install the MED-V components by using a batch file, a best practice is to specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="4bd6e-167">Это означает, что при установке центра обновления Windows не будет вмешательство в процесс установки, если требуется перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-167">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. <span data-ttu-id="4bd6e-168">**Агент узла MED-v** — Установка агента узла MED-v на компьютере с Windows 7, на котором будет выполняться med-v.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-168">**MED-V Host Agent** – Install the MED-V Host Agent on the Windows 7 computer where MED-V will be run.</span></span> <span data-ttu-id="4bd6e-169">Этот параметр должен быть установлен перед установкой рабочей области MED-V и проверяет, установлен ли Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-169">This must be installed before installing the MED-V workspace and checks to make sure that Windows Virtual PC is installed.</span></span>

3. <span data-ttu-id="4bd6e-170">**Рабочая область MED-v** вы создаете файлы, необходимые в этой установке с помощью диспетчера рабочих областей med-v: setup.exe, MEDV и MSI-файлы.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-170">**MED-V workspace** – You create the files that are required in this installation by using the MED-V Workspace Packager: the setup.exe, .medv, and .msi files.</span></span> <span data-ttu-id="4bd6e-171">Чтобы установить рабочую область для MED-V, запустите setup.exe; При этом другие файлы перезапускаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-171">To install the MED-V workspace, run setup.exe; this triggers the other files as required.</span></span> <span data-ttu-id="4bd6e-172">В процессе установки в реестре под ключом запуска на локальном компьютере заносится запись, с помощью которой запускается агент хоста MED-v, который всегда запускает MED-V при запуске Windows.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-172">The installation places an entry in the registry under the local machine run key to start the MED-V Host Agent, which always runs MED-V when Windows is started.</span></span>

   **<span data-ttu-id="4bd6e-173">Важно.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-173">Important</span></span>**  
   <span data-ttu-id="4bd6e-174">Установка рабочей области MED-V может выполняться конечным пользователем или автоматически с помощью электронной системы распространения программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-174">The installation of the MED-V workspace can be run interactively by the end user or silently through an electronic software distribution system.</span></span> <span data-ttu-id="4bd6e-175">Для установки рабочей области MED-V требуются учетные данные администратора, поэтому конечные пользователи должны быть администраторами компьютеров для установки рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-175">Installation of the MED-V workspace requires administrative credentials, so end users must be administrators of their computers to install the MED-V workspace.</span></span> <span data-ttu-id="4bd6e-176">Кроме того, электронная система распространения программного обеспечения обычно работает в контексте системы и обладает достаточными разрешениями.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-176">Alternately, an electronic software distribution system typically runs in the system context and has sufficient permissions.</span></span>



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### <span data-ttu-id="4bd6e-177">Установка первого раза</span><span class="sxs-lookup"><span data-stu-id="4bd6e-177">First Time Setup</span></span>

<span data-ttu-id="4bd6e-178">После установки MED-V и обязательных компонентов необходимо настроить MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-178">After MED-V and its required components are installed, MED-V must be configured.</span></span> <span data-ttu-id="4bd6e-179">Настройка MED-V известна при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-179">The configuration of MED-V is known as first time setup.</span></span> <span data-ttu-id="4bd6e-180">С помощью **диспетчера рабочих областей MED-V**вы можете настроить первый запуск программы установки в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-180">By using the **MED-V Workspace Packager**, you can configure first time setup to run silently or interactively.</span></span> <span data-ttu-id="4bd6e-181">При первой настройке MED-V требуется, чтобы конечные пользователи могли ввести пароль для проверки подлинности в рабочей области MED-V, но в противном случае она может быть практически невидимой для пользователя.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-181">First time setup of MED-V requires end users to enter their password to authenticate to the MED-V workspace, but otherwise can be almost invisible to the user.</span></span> <span data-ttu-id="4bd6e-182">Уведомления отображаются в области уведомлений, например при первом завершении настройки и готовности приложений.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-182">Notifications are shown in the notification area, such as when first time setup is complete and applications are ready.</span></span> <span data-ttu-id="4bd6e-183">Ниже приведены действия, которые выполняются при первом запуске MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-183">The following are the actions that occur during first time setup of MED-V:</span></span>

1.  <span data-ttu-id="4bd6e-184">Необходимо настроить виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-184">The virtual hard disk must be configured.</span></span> <span data-ttu-id="4bd6e-185">Мини-установка запускается и разворачивает образ Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-185">Mini-Setup runs and expands the Windows XP image.</span></span> <span data-ttu-id="4bd6e-186">Обычно это происходит в скрытом окне, но MED-V можно настроить для отображения во время этой конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-186">Typically, this occurs in a hidden window, but MED-V can be configured to display during this configuration.</span></span>

2.  <span data-ttu-id="4bd6e-187">После завершения мини-установки вы можете выполнять команды, необходимые для дополнительной настройки, такие как установка программного обеспечения ESD или других приложений, или Настройка изображения.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-187">After Mini-Setup finishes, you can run commands that you must have for additional configuration, such as installing ESD software or other applications, or configuring the image.</span></span> <span data-ttu-id="4bd6e-188">Они могут быть вызваны в файле Sysprep. INF, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-188">These can be called in the Sysprep.inf file, but are not required there.</span></span> <span data-ttu-id="4bd6e-189">Дополнительные сведения можно найти [в разделе Настройка образа ВИРТУАЛЬНЫХ ПК Windows для MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-189">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

3.  <span data-ttu-id="4bd6e-190">Ftscompletion.exe выполняется на последнем этапе настройки.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-190">Ftscompletion.exe is run as the last step in configuration.</span></span> <span data-ttu-id="4bd6e-191">Этот процесс завершает настройку MED-V, добавляет пользователя в группу RDP для доступа к рабочей области MED-V, копирует журналы, сигналы MED-V, которые готовы к работе с рабочей областью MED-v, а затем перезапускает рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-191">This process completes the MED-V configuration, adds the user to the RDP group to let them access the MED-V workspace, copies logs, signals MED-V that the MED-V workspace is ready, and then restarts the MED-V workspace.</span></span> <span data-ttu-id="4bd6e-192">Этот процесс также может добавить пользователя в качестве администратора рабочей области MED-V, если он был настроен при создании рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-192">This process can also add the user as an administrator of the MED-V workspace if this was configured when the MED-V workspace was created.</span></span> <span data-ttu-id="4bd6e-193">Ftscompletion.exe обычно вызывается с помощью Sysprep, INF-файла, но также может выполняться с помощью другого метода, например сценария.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-193">Ftscompletion.exe is typically called through the Sysprep,inf file but can also be run through another method, such as a script.</span></span> <span data-ttu-id="4bd6e-194">Однако Ftscompletion.exe должны быть последними действиями, которые выполняются при настройке рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-194">However, Ftscompletion.exe must be the last action that is performed when the workstation is configured.</span></span> <span data-ttu-id="4bd6e-195">Дополнительные сведения можно найти [в разделе Настройка образа ВИРТУАЛЬНЫХ ПК Windows для MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="4bd6e-195">For more information, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

4.  <span data-ttu-id="4bd6e-196">После того, как Рабочая область MED-V перезапустится Ftscompletion.exe, конечный пользователь войдет в систему.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-196">After the MED-V workspace is restarted by Ftscompletion.exe, the end user is logged on.</span></span> <span data-ttu-id="4bd6e-197">Если вы не сохранили свой пароль в первый раз, вам будет предложено ввести его еще раз.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-197">If they did not save their password during first time setup, they are prompted for it again.</span></span> <span data-ttu-id="4bd6e-198">Затем Рабочая область MED-V запускается и конфигурируется для пользователя.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-198">The MED-V workspace is then started and configured for the user.</span></span> <span data-ttu-id="4bd6e-199">Конфигурация включает применение групповой политики.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-199">Configuration includes applying Group Policy.</span></span>

    <span data-ttu-id="4bd6e-200">Рекомендуется применять только те политики, которые имеют смысл в среде совместимости приложений для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-200">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="4bd6e-201">Например, политики персонализации рабочего стола обычно не нужно применять и должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-201">For example, desktop personalization policies do not typically need to be applied and should be disabled.</span></span> <span data-ttu-id="4bd6e-202">Дополнительные сведения о том, как разрешить только локальные профили, можно найти в разделе [Параметры групповой политики для перемещаемых профилей пользователей](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="4bd6e-202">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

<span data-ttu-id="4bd6e-203">После того как вы закончите настройку, конечные пользователи получат уведомление о том, что опубликованные приложения готовы.</span><span class="sxs-lookup"><span data-stu-id="4bd6e-203">After first time setup is complete, the end user is notified that the published applications are ready.</span></span> <span data-ttu-id="4bd6e-204">После этого они смогут получать доступ к приложениям, установленным в рабочей области MED-V, из меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="4bd6e-204">They are then able to access the applications installed in the MED-V workspace from their **Start** menu.</span></span>

## <span data-ttu-id="4bd6e-205">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4bd6e-205">Related topics</span></span>


[<span data-ttu-id="4bd6e-206">Подготовка среды развертывания для MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-206">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

[<span data-ttu-id="4bd6e-207">Развертывание MED-V</span><span class="sxs-lookup"><span data-stu-id="4bd6e-207">Deployment of MED-V</span></span>](deployment-of-med-v.md)









