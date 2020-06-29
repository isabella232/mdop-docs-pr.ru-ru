---
title: Ручное развертывание рабочей области MED-V
description: Ручное развертывание рабочей области MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827279"
---
# <span data-ttu-id="d18c7-103">Ручное развертывание рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="d18c7-103">How to Deploy a MED-V Workspace Manually</span></span>


<span data-ttu-id="d18c7-104">В некоторых случаях вам может потребоваться развернуть рабочую область MED-V вручную, например, если ваша компания не использует электронную систему распространения программного обеспечения для развертывания приложений.</span><span class="sxs-lookup"><span data-stu-id="d18c7-104">In some instances, you might want to deploy your MED-V workspace manually, for example, if your company does not use an electronic software distribution system to deploy applications.</span></span>

<span data-ttu-id="d18c7-105">В этом разделе приведены инструкции по развертыванию рабочей области MED-V вручную.</span><span class="sxs-lookup"><span data-stu-id="d18c7-105">This section provides instruction about how to manually deploy a MED-V workspace.</span></span>

**<span data-ttu-id="d18c7-106">Развертывание рабочей области для MED-V вручную</span><span class="sxs-lookup"><span data-stu-id="d18c7-106">To deploy a MED-V workspace manually</span></span>**

1.  <span data-ttu-id="d18c7-107">Скопируйте все необходимые приложения и файлы пакета рабочей области для MED-V на общий диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="d18c7-107">Copy all prerequisite applications and the MED-V workspace package files to a shared drive or to a DVD.</span></span> <span data-ttu-id="d18c7-108">Ниже приведен список необходимых приложений и файлов.</span><span class="sxs-lookup"><span data-stu-id="d18c7-108">The following is a list of the required applications and files.</span></span>

    -   <span data-ttu-id="d18c7-109">**Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="d18c7-109">**Windows Virtual PC**.</span></span> <span data-ttu-id="d18c7-110">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d18c7-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="d18c7-111">**Дополнения и обновления для ВИРТУАЛЬНЫХ ПК Windows**.</span><span class="sxs-lookup"><span data-stu-id="d18c7-111">**Windows Virtual PC Additions and Updates**.</span></span> <span data-ttu-id="d18c7-112">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="d18c7-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="d18c7-113">**Установочный файл агента узла MED-v** — Установка агента узла (MED-V \ _HostAgent \ _setup установочный файл).</span><span class="sxs-lookup"><span data-stu-id="d18c7-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span>

        **<span data-ttu-id="d18c7-114">Warning</span><span class="sxs-lookup"><span data-stu-id="d18c7-114">Warning</span></span>**  
        <span data-ttu-id="d18c7-115">Перед установкой агента узла MED-V закройте Internet Explorer, в противном случае конфликты могут возникать позже с перенаправлением URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="d18c7-115">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="d18c7-116">Вы также можете сделать это, указав компьютер во время распространения.</span><span class="sxs-lookup"><span data-stu-id="d18c7-116">You can also do this by specifying a computer restart during a distribution.</span></span>



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. <span data-ttu-id="d18c7-117">Установите указанные ниже действия в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="d18c7-117">Install the following in the order listed.</span></span> <span data-ttu-id="d18c7-118">Конечный пользователь может выполнить эту задачу вручную или создать сценарий, чтобы установить следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="d18c7-118">The end user can perform this task manually or you can create a script to install the following:</span></span>

   -   <span data-ttu-id="d18c7-119">Windows Virtual PC и Windows Virtual PC, дополненные и обновления.</span><span class="sxs-lookup"><span data-stu-id="d18c7-119">Windows Virtual PC and the Windows Virtual PC additions and updates.</span></span> <span data-ttu-id="d18c7-120">Требуется перезагрузка компьютера.</span><span class="sxs-lookup"><span data-stu-id="d18c7-120">A computer restart is required.</span></span>

   -   <span data-ttu-id="d18c7-121">Агент узла MED-V.</span><span class="sxs-lookup"><span data-stu-id="d18c7-121">The MED-V Host Agent.</span></span>

       **<span data-ttu-id="d18c7-122">Примечание.</span><span class="sxs-lookup"><span data-stu-id="d18c7-122">Note</span></span>**  
       <span data-ttu-id="d18c7-123">Если он запущен, необходимо перезапустить Internet Explorer, прежде чем можно будет завершить установку агента узла MED-V.</span><span class="sxs-lookup"><span data-stu-id="d18c7-123">If it is running, Internet Explorer must be restarted before the installation of the MED-V Host Agent can finish.</span></span>



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. <span data-ttu-id="d18c7-124">Закончите настройку первого раза.</span><span class="sxs-lookup"><span data-stu-id="d18c7-124">Complete first time setup.</span></span>

   <span data-ttu-id="d18c7-125">После установки рабочей области для MED-V вы сможете запустить MED-V.</span><span class="sxs-lookup"><span data-stu-id="d18c7-125">After the MED-V workspace is installed, you have the option of starting MED-V.</span></span> <span data-ttu-id="d18c7-126">Запустится агент хоста MED-V.</span><span class="sxs-lookup"><span data-stu-id="d18c7-126">This starts the MED-V Host Agent.</span></span> <span data-ttu-id="d18c7-127">В это время вы можете либо запустить MED-V, либо запустить агент хоста MED-V позже, чтобы завершить настройку первой последующей настройки.</span><span class="sxs-lookup"><span data-stu-id="d18c7-127">You can either start MED-V at that time, or start the MED-V Host Agent later to complete first time setup.</span></span>

   <span data-ttu-id="d18c7-128">Чтобы запустить агент узла MED-V, нажмите кнопку **Пуск**, выберите **все программы**, нажмите кнопку **Microsoft Enterprise Virtualization**и выберите пункт **Агент хоста MED-V**.</span><span class="sxs-lookup"><span data-stu-id="d18c7-128">To start the MED-V Host Agent, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

## <span data-ttu-id="d18c7-129">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d18c7-129">Related topics</span></span>


[<span data-ttu-id="d18c7-130">Развертывание рабочей области MED-V с помощью системы электронного распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="d18c7-130">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[<span data-ttu-id="d18c7-131">Развертывание рабочей области MED-V в образе Windows 7</span><span class="sxs-lookup"><span data-stu-id="d18c7-131">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[<span data-ttu-id="d18c7-132">Развертывание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="d18c7-132">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)









