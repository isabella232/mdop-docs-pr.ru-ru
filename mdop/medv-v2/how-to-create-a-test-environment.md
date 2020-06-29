---
title: Создание тестовой среды
description: Создание тестовой среды
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827289"
---
# <span data-ttu-id="a0d73-103">Создание тестовой среды</span><span class="sxs-lookup"><span data-stu-id="a0d73-103">How to Create a Test Environment</span></span>


<span data-ttu-id="a0d73-104">Ниже приведены инструкции и инструкции, которые помогут вам создать тестовую среду, которую можно использовать для проверки локального пакета рабочей области для MED-V перед ее развертыванием во всей Организации.</span><span class="sxs-lookup"><span data-stu-id="a0d73-104">The following are some steps and instructions to help you create a test environment that you can use to test your MED-V workspace package locally before deploying it throughout your enterprise.</span></span> <span data-ttu-id="a0d73-105">В этом разделе приведены рекомендации о том, как создать тестовую среду: вручную или с помощью электронной системы рассылки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="a0d73-105">This section provides guidance about how to create a test environment, either manually or by using an electronic software distribution system.</span></span>

**<span data-ttu-id="a0d73-106">Создание тестовой среды с помощью ESD</span><span class="sxs-lookup"><span data-stu-id="a0d73-106">To create a test environment by using an ESD</span></span>**

1.  <span data-ttu-id="a0d73-107">Используйте метод развертывания программного обеспечения компании для развертывания на тестовом компьютере следующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="a0d73-107">Use your company’s method of deploying software throughout the enterprise to deploy the following necessary components to a test computer.</span></span> <span data-ttu-id="a0d73-108">Установите их в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="a0d73-108">Install them in the following order:</span></span>

    -   <span data-ttu-id="a0d73-109">**Windows Virtual PC** — если она еще не установлена.</span><span class="sxs-lookup"><span data-stu-id="a0d73-109">**Windows Virtual PC** – if not already installed.</span></span> <span data-ttu-id="a0d73-110">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="a0d73-110">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="a0d73-111">Добавлены **и обновленные виртуальные компьютеры Windows**— если они еще не установлены.</span><span class="sxs-lookup"><span data-stu-id="a0d73-111">**Windows Virtual PC Additions and Updates**– if not already installed.</span></span> <span data-ttu-id="a0d73-112">Дополнительные сведения можно найти в разделе [Настройка предварительных требований для установки](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="a0d73-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    -   <span data-ttu-id="a0d73-113">**Установочный файл агента узла MED-v** — Установка агента узла (MED-V \ _HostAgent \ _setup установочный файл).</span><span class="sxs-lookup"><span data-stu-id="a0d73-113">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="a0d73-114">Дополнительные сведения [можно найти в разделе Установка агента узла MED-V вручную](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="a0d73-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    -   <span data-ttu-id="a0d73-115">**Программа установки рабочей области MED-v, VHD и исполняемый файл Setup** создаются в **упаковщике рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="a0d73-115">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="a0d73-116">Дополнительные сведения можно найти [в разделе Создание пакета рабочей области для MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="a0d73-116">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        <span data-ttu-id="a0d73-117">**Важно!**  Исполняемая программа установки VHD и Setup должна находиться в той же папке, что и в установщике рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="a0d73-117">**Important** The VHD and Setup executable program must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="a0d73-118">Затем установите установщик рабочей области MED-V, запустив setup.exe.</span><span class="sxs-lookup"><span data-stu-id="a0d73-118">Then, install the MED-V workspace installer by running setup.exe.</span></span>

         

2.  <span data-ttu-id="a0d73-119">После того как все компоненты будут установлены на тестовом компьютере, запустите агент узла MED-V, чтобы начать установку в первый раз.</span><span class="sxs-lookup"><span data-stu-id="a0d73-119">After all of the components are installed on the test computer, run the MED-V Host Agent to start first time setup.</span></span>

    <span data-ttu-id="a0d73-120">Нажмите кнопку **Пуск**, выберите **все программы**, нажмите кнопку **Microsoft Enterprise Virtualization**и выберите пункт **Агент хоста MED-V**.</span><span class="sxs-lookup"><span data-stu-id="a0d73-120">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

    <span data-ttu-id="a0d73-121">**Примечание**  Если вы не можете физически запускать агент хоста MED-V на тестовом компьютере, программа установки запускается автоматически при следующем запуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="a0d73-121">**Note** If you cannot physically run the MED-V Host Agent on the test computer, first time setup starts automatically the next time that the computer restarts.</span></span>

     

<span data-ttu-id="a0d73-122">При первом запуске программы установки может потребоваться десять минут и больше.</span><span class="sxs-lookup"><span data-stu-id="a0d73-122">First time setup starts and can take ten minutes or more to finish.</span></span>

<span data-ttu-id="a0d73-123">Сведения о проверке параметров конфигурации при первом запуске программы установки приведены [в разделе Проверка параметров](how-to-verify-first-time-setup-settings.md)настройки при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="a0d73-123">For information about testing your configuration settings when first time setup is running, see [How to Verify First Time Setup Settings](how-to-verify-first-time-setup-settings.md).</span></span>

**<span data-ttu-id="a0d73-124">Создание тестовой среды вручную</span><span class="sxs-lookup"><span data-stu-id="a0d73-124">To create a test environment manually</span></span>**

1.  <span data-ttu-id="a0d73-125">Установка агента узла MED-V в локальной тестовой среде, включающей предварительные требования для MED-V, например Virtual PC для Windows и дополнений и обновлений.</span><span class="sxs-lookup"><span data-stu-id="a0d73-125">Install the MED-V Host Agent in a local test environment that includes MED-V prerequisites, such as Windows Virtual PC with additions and updates.</span></span> <span data-ttu-id="a0d73-126">Дополнительные сведения можно найти [в разделе Установка агента узла MED-V вручную](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="a0d73-126">For information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

2.  <span data-ttu-id="a0d73-127">Скопируйте файлы рабочей области для MED-V в тестовую среду.</span><span class="sxs-lookup"><span data-stu-id="a0d73-127">Copy the MED-V workspace files to your test environment.</span></span> <span data-ttu-id="a0d73-128">Файлы рабочих областей MED-V находятся в конечной папке, указанной в **упаковщике рабочих областей med-v**.</span><span class="sxs-lookup"><span data-stu-id="a0d73-128">The MED-V workspace files are located in the destination folder that you specified in the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="a0d73-129">**Важно!**  Исполняемая программа установки VHD и Setup должна находиться в той же папке тестовой среды, что и программа установки рабочей области MED-V.</span><span class="sxs-lookup"><span data-stu-id="a0d73-129">**Important** The VHD and Setup executable program must be in the same folder on your test environment as the MED-V workspace installer.</span></span>

     

3.  <span data-ttu-id="a0d73-130">Установите рабочую область MED-V, запустив setup.exe.</span><span class="sxs-lookup"><span data-stu-id="a0d73-130">Install the MED-V workspace by running setup.exe.</span></span>

4.  <span data-ttu-id="a0d73-131">Начните настройку с первого раза с помощью агента узла MED-V.</span><span class="sxs-lookup"><span data-stu-id="a0d73-131">Start first time setup by running the MED-V Host Agent.</span></span>

    <span data-ttu-id="a0d73-132">Нажмите кнопку **Пуск**, выберите **все программы**, нажмите кнопку **Microsoft Enterprise Virtualization**и выберите пункт **Агент хоста MED-V**.</span><span class="sxs-lookup"><span data-stu-id="a0d73-132">Click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Host Agent**.</span></span>

<span data-ttu-id="a0d73-133">При первом запуске программы установки может потребоваться несколько минут, в зависимости от размера указанного виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="a0d73-133">First time setup starts and might take several minutes to complete, depending on the size of the VHD specified.</span></span>

<span data-ttu-id="a0d73-134">Теперь вы можете протестировать различные параметры конфигурации, публикации приложений и перенаправления URL-адресов, которые вы указали для вашей рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="a0d73-134">You are now ready to test the different settings for configuration, application publishing, and URL redirection that you specified for your MED-V workspace.</span></span>

<span data-ttu-id="a0d73-135">**Примечание**  По умолчанию MED-V переопределяет политику блокировки экрана в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="a0d73-135">**Note** By default, MED-V overrides the screen lock policy in the guest.</span></span> <span data-ttu-id="a0d73-136">Однако это не представляет проблемы с безопасностью, так как главный компьютер по-прежнему учитывает политику блокировки экрана.</span><span class="sxs-lookup"><span data-stu-id="a0d73-136">However, this does not pose a security problem because the host computer still honors the screen lock policy.</span></span>

 

## <span data-ttu-id="a0d73-137">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a0d73-137">Related topics</span></span>


[<span data-ttu-id="a0d73-138">Проверка параметров первой установки</span><span class="sxs-lookup"><span data-stu-id="a0d73-138">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="a0d73-139">Проверка публикации приложений</span><span class="sxs-lookup"><span data-stu-id="a0d73-139">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="a0d73-140">Проверка перенаправления URL-адресов</span><span class="sxs-lookup"><span data-stu-id="a0d73-140">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

 

 





