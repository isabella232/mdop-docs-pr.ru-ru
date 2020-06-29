---
title: Удаление компонентов MED-V
description: Удаление компонентов MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813029"
---
# <span data-ttu-id="e8303-103">Удаление компонентов MED-V</span><span class="sxs-lookup"><span data-stu-id="e8303-103">How to Uninstall the MED-V Components</span></span>


<span data-ttu-id="e8303-104">В некоторых случаях вам может потребоваться удалить компоненты 2,0 (все или часть) Microsoft Enterprise Virtualization (MED-V) из вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e8303-104">Under certain circumstances, you might want to uninstall all or part of the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components from your enterprise.</span></span> <span data-ttu-id="e8303-105">Например, вы разрешили все проблемы с совместимостью операционной системы приложения или хотите развернуть другую рабочую область для MED-V на предприятии.</span><span class="sxs-lookup"><span data-stu-id="e8303-105">For example, you have resolved all application operating system compatibility issues, or you want to deploy a different MED-V workspace in your enterprise.</span></span>

<span data-ttu-id="e8303-106">Как правило, вы можете настроить систему электронной рассылки программного обеспечения (ESD) для удаления компонентов MED-V с помощью установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="e8303-106">Typically, you can configure your electronic software distribution (ESD) system to uninstall the MED-V components by using a Windows-based Installer.</span></span> <span data-ttu-id="e8303-107">Кроме того, вы можете удалить все или некоторые компоненты MED-V вручную.</span><span class="sxs-lookup"><span data-stu-id="e8303-107">Alternately, you can uninstall all or some MED-V components manually.</span></span>

<span data-ttu-id="e8303-108">**Важно!**  Прежде чем можно будет удалить агент узла MED-V, необходимо сначала удалить все установленные рабочие области MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-108">**Important** Before you can uninstall the MED-V Host Agent, you must first uninstall any installed MED-V workspace.</span></span>

 

<span data-ttu-id="e8303-109">Воспользуйтесь приведенными ниже инструкциями, чтобы удалить компоненты MED-V из Организации.</span><span class="sxs-lookup"><span data-stu-id="e8303-109">Use the following procedures to uninstall the MED-V components from your enterprise.</span></span>

**<span data-ttu-id="e8303-110">Удаление MED-V с помощью электронной системы распространения программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="e8303-110">To uninstall MED-V using an electronic software distribution System</span></span>**

1.  <span data-ttu-id="e8303-111">Используйте систему ESD для распространения сценария, который вызывает исполняемую программу uninstall.exe для каждой рабочей области MED-V, которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="e8303-111">Use your ESD system to distribute a script that invokes the uninstall.exe executable program for every MED-V workspace that you want to uninstall.</span></span> <span data-ttu-id="e8303-112">Файл расположен по адресу C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="e8303-112">The file is located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span> <span data-ttu-id="e8303-113">Вы можете установить флаг для автоматического запуска исполняемой программы удаления, чтобы конечные пользователи не могли удалить его.</span><span class="sxs-lookup"><span data-stu-id="e8303-113">You can set a flag to run the uninstall executable program silently so that end users are unaware of the uninstallation.</span></span>

2.  <span data-ttu-id="e8303-114">Создайте пакет для распространения установочного файла агента узла MED-V на каждый компьютер, на котором удалена Рабочая область MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-114">Create a package to distribute the MED-V Host Agent installation file to each computer on which a MED-V workspace was uninstalled.</span></span> <span data-ttu-id="e8303-115">Настройте пакет для выполнения удаления в автоматическом режиме.</span><span class="sxs-lookup"><span data-stu-id="e8303-115">Configure the package to run the uninstallation in silent mode.</span></span>

<span data-ttu-id="e8303-116">Клиент ESD определяет доступность новых пакетов и начинает удаление пакетов в соответствии с определением и требованиями.</span><span class="sxs-lookup"><span data-stu-id="e8303-116">The ESD client recognizes when the new packages are available and starts to uninstall the packages per the definition and requirements.</span></span>

**<span data-ttu-id="e8303-117">Удаление рабочей области MED-V вручную</span><span class="sxs-lookup"><span data-stu-id="e8303-117">To manually uninstall a MED-V workspace</span></span>**

1.  <span data-ttu-id="e8303-118">На главном компьютере нажмите кнопку **Пуск**и выберите пункт **Панель управления**, а затем — **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="e8303-118">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="e8303-119">В окне **программы и компоненты** выберите рабочую область MED-V, которую вы хотите удалить, и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e8303-119">In the **Programs and Features** window, select the MED-V workspace that you want to remove, and then click **Uninstall**.</span></span> <span data-ttu-id="e8303-120">(Рабочая область MED-V называется "MED-V Workspace &lt; ". *Рабочая область \ _name* &gt; ").</span><span class="sxs-lookup"><span data-stu-id="e8303-120">(The MED-V workspace is named "MED-V Workspace - &lt;*workspace\_name*&gt;").</span></span> <span data-ttu-id="e8303-121">&lt;Откроется мастер настройки *рабочей области \ _name* &gt; **Setup Wizard** .</span><span class="sxs-lookup"><span data-stu-id="e8303-121">The &lt;*workspace\_name*&gt; **Setup Wizard** opens.</span></span>

3.  <span data-ttu-id="e8303-122">В **мастере настройки**нажмите кнопку **Далее**, а затем — **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e8303-122">On the **Setup Wizard**, click **Next**, and then click **Remove**.</span></span>

4.  <span data-ttu-id="e8303-123">Если вы предпочитаете, установите флажок, чтобы удалить основной диск виртуального жесткого диска и разностные диски, созданные MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-123">If you prefer, select the check box to delete the master VHD disk and differencing disks created by MED-V.</span></span> <span data-ttu-id="e8303-124">Это не обязательно, но освобождает место на диске после завершения удаления.</span><span class="sxs-lookup"><span data-stu-id="e8303-124">This is not required, but frees disk space after the uninstallation finishes.</span></span>

5.  <span data-ttu-id="e8303-125">Нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e8303-125">Click **Remove**.</span></span>

    <span data-ttu-id="e8303-126">**Примечание**  Если в настоящее время запущены службы MED-V, появится диалоговое окно с запросом о том, нужно ли завершить работу.</span><span class="sxs-lookup"><span data-stu-id="e8303-126">**Note** If MED-V is currently running, a dialog box appears and prompts you whether you want to shut it down.</span></span> <span data-ttu-id="e8303-127">Нажмите кнопку **Да** , чтобы продолжить удаление.</span><span class="sxs-lookup"><span data-stu-id="e8303-127">Click **Yes** to continue with the uninstallation.</span></span> <span data-ttu-id="e8303-128">Нажмите кнопку **нет** , чтобы отменить удаление.</span><span class="sxs-lookup"><span data-stu-id="e8303-128">Click **No** to cancel the uninstallation.</span></span>

     

<span data-ttu-id="e8303-129">Кроме того, вы можете удалить рабочую область MED-V, запустив `uninstall.exe` файл, который, как правило, находится по адресу C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span><span class="sxs-lookup"><span data-stu-id="e8303-129">Alternately, you can remove a MED-V workspace by running the `uninstall.exe` file, typically located at C:\\ProgramData\\Microsoft\\Medv\\Workspace.</span></span>

**<span data-ttu-id="e8303-130">Удаление агента узла MED-V вручную</span><span class="sxs-lookup"><span data-stu-id="e8303-130">To manually uninstall the MED-V Host Agent</span></span>**

1.  <span data-ttu-id="e8303-131">На главном компьютере с Windows 7 нажмите кнопку **Пуск**, выберите **Панель управления**, а затем — **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="e8303-131">On the Windows 7 host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="e8303-132">В окне **программы и компоненты** выберите **Агент хоста MED-V**и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e8303-132">In the **Programs and Features** window, select **MED-V Host Agent**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="e8303-133">Установщик Windows удаляет агент узла MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-133">The Windows Installer removes the MED-V Host Agent.</span></span>

    <span data-ttu-id="e8303-134">**Примечание**  Если вы попытаетесь удалить агент узла MED-v перед удалением рабочей области MED-V, появится диалоговое окно, в котором говорится, что сначала необходимо удалить рабочую область MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-134">**Note** If you try to uninstall the MED-V Host Agent before you uninstall the MED-V workspace, a dialog box appears that states that you must first uninstall the MED-V workspace.</span></span> <span data-ttu-id="e8303-135">Чтобы продолжить, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e8303-135">Click **OK** to continue.</span></span>

     

**<span data-ttu-id="e8303-136">Удаление диспетчера рабочих областей MED-V вручную</span><span class="sxs-lookup"><span data-stu-id="e8303-136">To manually uninstall the MED-V Workspace Packager</span></span>**

1.  <span data-ttu-id="e8303-137">На главном компьютере нажмите кнопку **Пуск**и выберите пункт **Панель управления**, а затем — **программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="e8303-137">On the host computer, click **Start**, click **Control Panel**, and then click **Programs and Features**.</span></span>

2.  <span data-ttu-id="e8303-138">В окне **программы и компоненты** выберите **упаковщик рабочих областей MED-V**и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e8303-138">In the **Programs and Features** window, select **MED-V Workspace Packager**, and then click **Uninstall**.</span></span>

    <span data-ttu-id="e8303-139">Установщик Windows удаляет диспетчер рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-139">The Windows Installer removes the MED-V Workspace Packager.</span></span>

    <span data-ttu-id="e8303-140">**Примечание**  Вы можете удалить упаковщик рабочих областей MED-V в любое время, не затрагивая развернутых рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="e8303-140">**Note** You can uninstall the MED-V Workspace Packager at any time without affecting any deployed MED-V workspaces.</span></span>

     

## <span data-ttu-id="e8303-141">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e8303-141">Related topics</span></span>


[<span data-ttu-id="e8303-142">Развертывание компонентов MED-V</span><span class="sxs-lookup"><span data-stu-id="e8303-142">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)

 

 





