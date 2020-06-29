---
title: Создание образа для восстановления DaRT 10
description: Создание образа для восстановления DaRT 10
author: dansimp
ms.assetid: 173556de-2f20-4ea6-9e29-fc5ccc71ebd7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebb48ee140a6e3f70e05acd3f6affc6e3b71ff37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813208"
---
# <span data-ttu-id="5082c-103">Создание образа для восстановления DaRT 10</span><span class="sxs-lookup"><span data-stu-id="5082c-103">Creating the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="5082c-104">После установки набора средств диагностики и восстановления Microsoft (DaRT) 10 вы создадите изображение для восстановления DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="5082c-104">After installing Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you create a DaRT 10 recovery image.</span></span> <span data-ttu-id="5082c-105">Образ восстановления запускает Windows RE, из которого можно запускать инструменты DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-105">The recovery image starts Windows RE, from which you can then start the DaRT tools.</span></span> <span data-ttu-id="5082c-106">Вы можете создавать файлы международной организации по стандартизации (ISO) и изображения в формате Windows Imaging (WIM).</span><span class="sxs-lookup"><span data-stu-id="5082c-106">You can generate International Organization for Standardization (ISO) files and Windows Imaging Format (WIM) images.</span></span> <span data-ttu-id="5082c-107">Кроме того, вы можете использовать PowerShell для создания сценариев, использующих параметры, выбранные в мастере создания изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-107">In addition, you can use PowerShell to generate scripts that use the settings you select in the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="5082c-108">Вы можете использовать этот сценарий позже для повторной сборки образов восстановления с использованием одинаковых параметров.</span><span class="sxs-lookup"><span data-stu-id="5082c-108">You can use the script later to rebuild recovery images by using the same settings.</span></span> <span data-ttu-id="5082c-109">Образ восстановления предоставляет множество средств восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-109">The recovery image provides a variety of recovery tools.</span></span> <span data-ttu-id="5082c-110">Описание инструментов можно найти в статье [Обзор средств на DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="5082c-110">For a description of the tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

<span data-ttu-id="5082c-111">После загрузки компьютера на DaRT вы можете использовать различные инструменты DaRT для диагностики и восстановления компьютера.</span><span class="sxs-lookup"><span data-stu-id="5082c-111">After you boot the computer into DaRT, you can run the different DaRT tools to try to diagnose and repair the computer.</span></span> <span data-ttu-id="5082c-112">В этом разделе описывается процесс создания изображения для восстановления DaRT и вы можете выбрать инструменты и компоненты, которые нужно включить в состав изображения.</span><span class="sxs-lookup"><span data-stu-id="5082c-112">This section walks you through the process of creating the DaRT recovery image and lets you select the tools and features that you want to include as part of the image.</span></span>

<span data-ttu-id="5082c-113">Вы можете создать изображение для восстановления DaRT одним из двух способов:</span><span class="sxs-lookup"><span data-stu-id="5082c-113">You can create the DaRT recovery image by using either of two methods:</span></span>

-   <span data-ttu-id="5082c-114">Использование мастера создания изображений для восстановления с помощью DaRT, который работает в среде Windows.</span><span class="sxs-lookup"><span data-stu-id="5082c-114">Use the DaRT Recovery Image wizard, which runs in a Windows environment.</span></span>

-   <span data-ttu-id="5082c-115">Измените пример сценария PowerShell на нужные значения.</span><span class="sxs-lookup"><span data-stu-id="5082c-115">Modify an example PowerShell script with the values you want.</span></span> <span data-ttu-id="5082c-116">Дополнительные сведения можно найти в разделе [Использование сценария PowerShell для создания образа восстановления](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="5082c-116">For more information, see [How to Use a PowerShell Script to Create the Recovery Image](how-to-use-a-powershell-script-to-create-the-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="5082c-117">Вы можете записать ISO на записываемый компакт-диск или DVD-диски, сохранить его на USB-накопитель или сохранить в формате, который можно использовать для загрузки DaRT из удаленной секции или из раздела восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-117">You can write the ISO to a recordable CD or DVD, save it to a USB flash drive, or save it in a format that you can use to boot into DaRT from a remote partition or from a recovery partition.</span></span>

<span data-ttu-id="5082c-118">Создав ISO-образ, вы можете записать его на чистую дискету или DVD-диск (если на вашем компьютере есть компакт-или дисковод).</span><span class="sxs-lookup"><span data-stu-id="5082c-118">Once you have created the ISO image, you can burn it onto a blank CD or DVD (if your computer has a CD or DVD drive).</span></span> <span data-ttu-id="5082c-119">Если на вашем компьютере нет диска для этой цели, вы можете использовать большинство обычных программ, которые используются для записи компакт-дисков или DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="5082c-119">If your computer does not have a drive for this purpose, you can use most generic programs that are used to burn CDs or DVDs.</span></span>

## <span data-ttu-id="5082c-120">Выбор архитектуры изображения и указание пути</span><span class="sxs-lookup"><span data-stu-id="5082c-120">Select the image architecture and specify the path</span></span>


<span data-ttu-id="5082c-121">На странице Media в Windows 10 вы можете выбрать, нужно ли создавать изображение для восстановления с помощью 32 или 64-разрядной версии DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-121">On the Windows 10 Media page, you select whether to create a 32-bit or 64-bit DaRT recovery image.</span></span> <span data-ttu-id="5082c-122">Используйте 32-разрядную версию Windows для создания изображений для восстановления с 32-разрядной DaRT и 64-разрядная версия Windows для создания 64-разрядных изображений для восстановления с помощью DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-122">Use the 32-bit Windows to build 32-bit DaRT recovery images, and 64-bit Windows to build 64-bit DaRT recovery images.</span></span> <span data-ttu-id="5082c-123">Вы можете использовать один компьютер для создания изображений восстановления для обоих типов архитектуры, но вы не можете создать одно изображение, работающее как в 32-, так и в 64-разрядных архитектурах.</span><span class="sxs-lookup"><span data-stu-id="5082c-123">You can use a single computer to create recovery images for both architecture types, but you cannot create one image that works on both 32-bit and 64-bit architectures.</span></span> <span data-ttu-id="5082c-124">Вы также указываете путь к установочному носителю Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5082c-124">You also indicate the path of the Windows 10 installation media.</span></span> <span data-ttu-id="5082c-125">Выберите архитектуру, совпадающую с одним из создаваемого образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-125">Choose the architecture that matches the one of the recovery image that you are creating.</span></span>

**<span data-ttu-id="5082c-126">Выбор архитектуры изображения и указание пути</span><span class="sxs-lookup"><span data-stu-id="5082c-126">To select the image architecture and specify the path</span></span>**

1.  <span data-ttu-id="5082c-127">На странице **Windows 10 мультимедиа** выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="5082c-127">On the **Windows 10 Media** page, select one of the following:</span></span>

    -   <span data-ttu-id="5082c-128">Если вы создаете образ восстановления для компьютеров с 64, выберите команду **создать изображение DART для 64 64-разрядной версии**.</span><span class="sxs-lookup"><span data-stu-id="5082c-128">If you are creating a recovery image for 64-bit computers, select **Create x64 (64-bit) DaRT image**.</span></span>

    -   <span data-ttu-id="5082c-129">Если вы создаете образ для восстановления на компьютерах с 32-разрядными компьютерами, выберите команду **создать изображение DART для x86 (32-разр.)**.</span><span class="sxs-lookup"><span data-stu-id="5082c-129">If you are creating a recovery image for 32-bit computers, select **Create x86 (32-bit) DaRT image**.</span></span>

2.  <span data-ttu-id="5082c-130">В поле введите путь к корневому каталогу для установочного файла **Windows 10 &lt; (64 &gt; -разрядная версия) или 32-bit** (для Windows 10).</span><span class="sxs-lookup"><span data-stu-id="5082c-130">In the **Specify the root path of the Windows 10 &lt;64-bit or 32-bit&gt; install media** box, type the path of the Windows 10 installation files.</span></span> <span data-ttu-id="5082c-131">Используйте путь, соответствующий архитектуре создаваемого образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-131">Use a path that matches the architecture of the recovery image that you are creating.</span></span>

3.  <span data-ttu-id="5082c-132">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-132">Click **Next**.</span></span>

## <span data-ttu-id="5082c-133">Выбор средств для включения в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-133">Select the tools to include on the recovery image</span></span>


<span data-ttu-id="5082c-134">На странице "Инструменты" можно выбрать многочисленные инструменты, которые нужно включить в образ восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-134">On the Tools page, you can select numerous tools to include on the recovery image.</span></span> <span data-ttu-id="5082c-135">Эти средства будут доступны для конечных пользователей при загрузке изображения DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-135">These tools will be available to end users when they boot into the DaRT image.</span></span> <span data-ttu-id="5082c-136">Тем не менее, если при создании изображения DaRT вы подключаетесь к удаленному подключению, все эти средства будут доступны, когда сотрудник службы поддержки подключается к компьютеру конечного пользователя, независимо от того, какие инструменты вы выбрали для включения в изображение.</span><span class="sxs-lookup"><span data-stu-id="5082c-136">However, if you enable remote connectivity when creating the DaRT image, all of the tools will be available when a help desk worker connects to the end user’s computer, regardless of which tools you chose to include on the image.</span></span>

<span data-ttu-id="5082c-137">Чтобы ограничить доступ конечных пользователей к этим средствам, но по-прежнему сохранять полный доступ к средствам с помощью средства просмотра удаленных подключений, не выбирайте эти средства на странице инструменты.</span><span class="sxs-lookup"><span data-stu-id="5082c-137">To restrict end-user access to these tools, but still retain full access to the tools through the Remote Connection Viewer, do not select those tools on the Tools page.</span></span> <span data-ttu-id="5082c-138">Конечные пользователи смогут использовать только удаленное подключение и смогут просматривать, но не Access, любые инструменты, исключаемые из образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-138">End users will be able to use only Remote Connection and will be able to see, but not access, any tools that you exclude from the recovery image.</span></span>

**<span data-ttu-id="5082c-139">Выбор средств для включения в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-139">To select the tools to include on the recovery image</span></span>**

1.  <span data-ttu-id="5082c-140">На странице " **инструменты** " установите флажок рядом с каждым инструментом, который вы хотите включить в изображение.</span><span class="sxs-lookup"><span data-stu-id="5082c-140">On the **Tools** page, select the check box beside each tool that you want to include on the image.</span></span>

2.  <span data-ttu-id="5082c-141">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-141">Click **Next**.</span></span>

## <span data-ttu-id="5082c-142">Выберите, разрешено ли удаленное подключение через службу поддержки</span><span class="sxs-lookup"><span data-stu-id="5082c-142">Choose whether to allow remote connectivity by a help desk</span></span>


<span data-ttu-id="5082c-143">На странице Remote Connection (удаленное подключение) вы можете разрешить сотрудникам службы поддержки удаленно подключать и запускать инструменты DaRT на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5082c-143">On the Remote Connection page, you can choose to enable a help desk worker to remotely connect to and run the DaRT tools on an end user’s computer.</span></span> <span data-ttu-id="5082c-144">Параметр Remote Connectivity затем отображается как доступный параметр в окне инструментов Диагностика и восстановление.</span><span class="sxs-lookup"><span data-stu-id="5082c-144">The remote connectivity option is then shown as an available option in the Diagnostics and Recovery Toolset window.</span></span> <span data-ttu-id="5082c-145">После того как сотрудники службы поддержки смогут установить удаленное подключение, они могут запускать инструменты DaRT на компьютере конечного пользователя, находясь в удаленном расположении.</span><span class="sxs-lookup"><span data-stu-id="5082c-145">After help desk workers establish a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

**<span data-ttu-id="5082c-146">Разрешение удаленной связи между сотрудниками службы поддержки</span><span class="sxs-lookup"><span data-stu-id="5082c-146">To choose whether to allow remote connectivity by help desk workers</span></span>**

1.  <span data-ttu-id="5082c-147">На странице " **удаленное подключение** " установите флажок **Разрешить удаленные** соединения, чтобы разрешить удаленные подключения, или снимите этот флажок, чтобы запретить удаленные подключения.</span><span class="sxs-lookup"><span data-stu-id="5082c-147">On the **Remote Connection** page, select the **Allow remote connections** check box to allow remote connections, or clear the check box to prevent remote connections.</span></span>

2.  <span data-ttu-id="5082c-148">Если флажок **Разрешить удаленные подключения** снят, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-148">If you cleared the **Allow remote connections** check box, click **Next**.</span></span> <span data-ttu-id="5082c-149">В противном случае перейдите к следующему действию, чтобы продолжить настройку удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="5082c-149">Otherwise, go to the next step to continue configuring remote connectivity.</span></span>

3.  <span data-ttu-id="5082c-150">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="5082c-150">Select one of the following:</span></span>

    -   <span data-ttu-id="5082c-151">Позвольте Windows выбрать открытый номер порта.</span><span class="sxs-lookup"><span data-stu-id="5082c-151">Let Windows choose an open port number.</span></span>

    -   <span data-ttu-id="5082c-152">Укажите номер порта.</span><span class="sxs-lookup"><span data-stu-id="5082c-152">Specify the port number.</span></span> <span data-ttu-id="5082c-153">Если выбрать этот параметр, введите номер порта в диапазоне от 1 до 65535 в поле ниже параметра.</span><span class="sxs-lookup"><span data-stu-id="5082c-153">If you select this option, enter a port number between 1 and 65535 in the field beneath the option.</span></span> <span data-ttu-id="5082c-154">Этот номер порта будет использоваться при установке удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="5082c-154">This port number will be used when establishing a remote connection.</span></span> <span data-ttu-id="5082c-155">Чтобы свести к минимуму вероятность конфликта, мы рекомендуем использовать номер порта 1024 или выше.</span><span class="sxs-lookup"><span data-stu-id="5082c-155">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

4.  <span data-ttu-id="5082c-156">(Необязательно) в поле **приветственное сообщение удаленного подключения** создайте настраиваемое сообщение, которое конечные пользователи получат при установке удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="5082c-156">(Optional) in the **Remote connection welcome** message box, create a customized message that end users receive when they establish a remote connection.</span></span> <span data-ttu-id="5082c-157">Сообщение не может содержать более 2048 символов.</span><span class="sxs-lookup"><span data-stu-id="5082c-157">The message can be a maximum of 2048 characters.</span></span>

5.  <span data-ttu-id="5082c-158">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-158">Click **Next**.</span></span>

    <span data-ttu-id="5082c-159">Дополнительные сведения об удаленном запуске средств DaRT можно найти [в разделе Восстановление удаленных компьютеров с помощью DaRT для восстановления](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="5082c-159">For more information about running the DaRT tools remotely, see [How to Recover Remote Computers by Using the DaRT Recovery Image](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

## <span data-ttu-id="5082c-160">Добавление драйверов в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-160">Add drivers to the recovery image</span></span>


<span data-ttu-id="5082c-161">На вкладке "драйверы" на странице "Дополнительные параметры" можно добавить дополнительные драйверы устройств, которые могут потребоваться при восстановлении компьютера.</span><span class="sxs-lookup"><span data-stu-id="5082c-161">On the Drivers tab of the Advanced Options page, you can add additional device drivers that you may need when repairing a computer.</span></span> <span data-ttu-id="5082c-162">Сюда обычно относятся устройства хранения данных или сетевые контроллеры, которые не поддерживаются в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5082c-162">These may typically include storage or network controllers that Windows 10 does not provide.</span></span> <span data-ttu-id="5082c-163">Драйверы устанавливаются при создании образа.</span><span class="sxs-lookup"><span data-stu-id="5082c-163">Drivers are installed when the image is created.</span></span>

<span data-ttu-id="5082c-164">**Важно!**  Если вы выбрали драйвер для включения, имейте в виду, что в DaRT не поддерживается беспроводная связь (например, Bluetooth или 802.11 a/b/g/n).</span><span class="sxs-lookup"><span data-stu-id="5082c-164">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="5082c-165">Добавление драйверов в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-165">To add drivers to the recovery image</span></span>**

1.  <span data-ttu-id="5082c-166">На странице " **Дополнительные параметры** " откройте вкладку " **драйверы** ".</span><span class="sxs-lookup"><span data-stu-id="5082c-166">On the **Advanced Options** page, click the **Drivers** tab.</span></span>

2.  <span data-ttu-id="5082c-167">Щелкните **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="5082c-167">Click **Add**.</span></span>

3.  <span data-ttu-id="5082c-168">Перейдите к файлу, который нужно добавить для драйвера, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="5082c-168">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="5082c-169">**Примечание**  Файл драйвера предоставляется производителем устройства хранения или сетевого контроллера.</span><span class="sxs-lookup"><span data-stu-id="5082c-169">**Note** The driver file is provided by the manufacturer of the storage or network controller.</span></span>

     

4.  <span data-ttu-id="5082c-170">Повторите действия 2 и 3 для каждого драйвера, который вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="5082c-170">Repeat Steps 2 and 3 for every driver that you want to include.</span></span>

5.  <span data-ttu-id="5082c-171">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-171">Click **Next**.</span></span>

## <span data-ttu-id="5082c-172">Добавление дополнительных пакетов WinPE в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-172">Add WinPE optional packages to the recovery image</span></span>


<span data-ttu-id="5082c-173">На вкладке WinPE на странице "Дополнительные параметры" вы можете добавить дополнительные пакеты WinPE к изображению DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-173">On the WinPE tab of the Advanced Options page, you can add WinPE optional packages to the DaRT image.</span></span> <span data-ttu-id="5082c-174">Эти пакеты входят в состав Windows ADK, который является обязательным компонентом установки для мастера изображений для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-174">These packages are part of the Windows ADK, which is an installation prerequisite for the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="5082c-175">Все доступные для выбора инструменты необязательны.</span><span class="sxs-lookup"><span data-stu-id="5082c-175">The tools that you can select are all optional.</span></span> <span data-ttu-id="5082c-176">Все необходимые пакеты добавляются автоматически на основе средств, выбранных на странице инструменты.</span><span class="sxs-lookup"><span data-stu-id="5082c-176">Any required packages are added automatically, based on the tools you selected on the Tools page.</span></span>

<span data-ttu-id="5082c-177">Вы также можете указать размер рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5082c-177">You can also specify the size of the scratch space.</span></span> <span data-ttu-id="5082c-178">Рабочую область — это объем дискового пространства, выделяемого для использования DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-178">Scratch space is the amount of RAM disk space that is set aside for DaRT to run.</span></span> <span data-ttu-id="5082c-179">Рабочая область полезна в том случае, если жесткий диск конечного пользователя недоступен.</span><span class="sxs-lookup"><span data-stu-id="5082c-179">The scratch space is useful in case the end user’s hard disk is not available.</span></span> <span data-ttu-id="5082c-180">Если вы используете дополнительные инструменты и драйверы, вам может потребоваться расширить рабочую область.</span><span class="sxs-lookup"><span data-stu-id="5082c-180">If you are running additional tools and drivers, you may want to increase the scratch space.</span></span>

**<span data-ttu-id="5082c-181">Добавление дополнительных пакетов WinPE в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-181">To add WinPE optional packages to the recovery image</span></span>**

1.  <span data-ttu-id="5082c-182">На странице " **Дополнительные параметры** " откройте вкладку **WinPE** .</span><span class="sxs-lookup"><span data-stu-id="5082c-182">On the **Advanced Options** page, click the **WinPE** tab.</span></span>

2.  <span data-ttu-id="5082c-183">Установите флажки рядом с каждым пакетом, который вы хотите включить в изображение, или щелкните флажок **имя** , чтобы выбрать все пакеты.</span><span class="sxs-lookup"><span data-stu-id="5082c-183">Select the check box beside each package that you want to include on the image, or click the **Name** check box to select all of the packages.</span></span>

3.  <span data-ttu-id="5082c-184">В поле **Рабочая область** выберите объем дискового пространства, выделяемого для использования DART в случае недоступности жесткого диска конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5082c-184">In the **Scratch Space** field, select the amount of RAM disk space to allocate for running DaRT in case the end user’s hard disk is not available.</span></span>

4.  <span data-ttu-id="5082c-185">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-185">Click **Next**.</span></span>

## <span data-ttu-id="5082c-186">Добавление средств отладки для анализатора сбоев</span><span class="sxs-lookup"><span data-stu-id="5082c-186">Add the debugging tools for Crash Analyzer</span></span>


<span data-ttu-id="5082c-187">Если в образ ISO включено средство анализа сбоев, необходимо также включить средства отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="5082c-187">If you include the Crash Analyzer tool in the ISO image, you must also include the Debugging Tools for Windows.</span></span> <span data-ttu-id="5082c-188">На вкладке анализатора сбоев на странице "Дополнительные параметры" введите путь к средствам отладки Windows 10, которые анализатор аварийного анализа использует при анализе файлов дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="5082c-188">On the Crash Analyzer tab of the Advanced Options page, you enter the path of the Windows 10 Debugging Tools, which Crash Analyzer uses to analyze memory dump files.</span></span> <span data-ttu-id="5082c-189">Вы можете использовать инструменты, которые находятся на компьютере, на котором запущен мастер создания изображений для восстановления DaRT, или использовать инструменты, которые находятся на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="5082c-189">You can use the tools that are on the computer where you are running the DaRT Recovery Image wizard, or you can use the tools that are on the end-user computer.</span></span> <span data-ttu-id="5082c-190">Если вы решили использовать инструменты на компьютере конечного пользователя, помните, что на каждом компьютере, который вы хотите диагностировать, должны быть установлены средства отладки.</span><span class="sxs-lookup"><span data-stu-id="5082c-190">If you decide to use the tools on the end-user computer, remember that every computer that you diagnose must have the Debugging Tools installed.</span></span>

<span data-ttu-id="5082c-191">Если вы установили пакет средств разработки программного обеспечения для Microsoft Windows (SDK) или пакет средств разработки для Microsoft Windows (WDK), средства отладки Windows 10 добавляются в образ восстановления по умолчанию, и путь к средствам отладки автоматически заполняется.</span><span class="sxs-lookup"><span data-stu-id="5082c-191">If you installed the Microsoft Windows Software Development Kit (SDK) or the Microsoft Windows Development Kit (WDK), the Windows 10 Debugging Tools are added to the recovery image by default, and the path to the Debugging Tools is automatically filled in.</span></span> <span data-ttu-id="5082c-192">Вы можете изменить путь к средствам отладки Windows 10, если файлы находятся не там, где указан путь к файлу по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5082c-192">You can change the path of the Windows 10 Debugging Tools if the files are located somewhere other than the location indicated by the default file path.</span></span> <span data-ttu-id="5082c-193">Ссылка в мастере позволяет загрузить и установить инструменты отладки для Windows, если они еще не установлены.</span><span class="sxs-lookup"><span data-stu-id="5082c-193">A link in the wizard lets you download and install debugging tools for Windows if they are not already installed.</span></span>

<span data-ttu-id="5082c-194">Для загрузки средств отладки Windows ознакомьтесь со [средствами отладки для Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span><span class="sxs-lookup"><span data-stu-id="5082c-194">To download the Windows Debugging Tools, see [Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=266248).</span></span> <span data-ttu-id="5082c-195">Установка средств отладки в расположение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5082c-195">Install the Debugging Tools to the default location.</span></span>

<span data-ttu-id="5082c-196">**Примечание**  Мастер DaRT проверяет наличие средств в разделе `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` реестра.</span><span class="sxs-lookup"><span data-stu-id="5082c-196">**Note** The DaRT wizard checks for the tools in the `HKLM\Software\Microsoft\Windows Kits\Installed Roots\WindowsDebuggersRoot` registry key.</span></span> <span data-ttu-id="5082c-197">Если значение в реестре отсутствует, мастер выполняет поиск в одном из следующих расположений в зависимости от архитектуры системы:</span><span class="sxs-lookup"><span data-stu-id="5082c-197">If the registry value is not there, the wizard looks in one of the following locations, depending on your system architecture:</span></span>

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x64`

`%ProgramFilesX86%\Windows Kits\10.0\Debuggers\x86`

 

**<span data-ttu-id="5082c-198">Добавление средств отладки для анализатора сбоев</span><span class="sxs-lookup"><span data-stu-id="5082c-198">To add the debugging tools for Crash Analyzer</span></span>**

1.  <span data-ttu-id="5082c-199">На странице " **Дополнительные параметры** " откройте вкладку **анализатора сбоев** .</span><span class="sxs-lookup"><span data-stu-id="5082c-199">On the **Advanced Options** page, click the **Crash Analyzer** tab.</span></span>

2.  <span data-ttu-id="5082c-200">Необязательно Нажмите **загрузить инструменты отладки** , чтобы скачать инструменты отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="5082c-200">(Optional) Click **Download the Debugging Tools** to download the Debugging Tools for Windows.</span></span>

3.  <span data-ttu-id="5082c-201">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="5082c-201">Select one of the following options:</span></span>

    -   <span data-ttu-id="5082c-202">**Включите &lt; &gt; средства отладки Windows 10 64-bit или 32-bit**.</span><span class="sxs-lookup"><span data-stu-id="5082c-202">**Include the Windows 10 &lt;64-bit or 32-bit&gt; Debugging Tools**.</span></span> <span data-ttu-id="5082c-203">Если вы выберете этот параметр, найдите и выберите расположение инструментов, если путь еще не отображается.</span><span class="sxs-lookup"><span data-stu-id="5082c-203">If you select this option, browse to and select the location of the tools if the path is not already displaying.</span></span>

    -   <span data-ttu-id="5082c-204">**Используйте инструменты отладки из отлаживаемой системы**.</span><span class="sxs-lookup"><span data-stu-id="5082c-204">**Use the Debugging Tools from the system that is being debugged**.</span></span> <span data-ttu-id="5082c-205">Если вы выберете этот параметр, анализатор сбоев не будет работать, если средства отладки для Windows не будут найдены на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="5082c-205">If you select this option, the Crash Analyzer will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

4.  <span data-ttu-id="5082c-206">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-206">Click **Next**.</span></span>

## <span data-ttu-id="5082c-207">Выбор типов файлов образа восстановления для создания</span><span class="sxs-lookup"><span data-stu-id="5082c-207">Select the types of recovery image files to create</span></span>


<span data-ttu-id="5082c-208">На странице "Создание изображения" вы выбираете папку выходных данных для образа восстановления, введите имя изображения и выберите типы файлов изображений для восстановления DaRT, которые нужно создать.</span><span class="sxs-lookup"><span data-stu-id="5082c-208">On the Create Image page, you choose an output folder for the recovery image, enter an image name, and select the types of DaRT recovery image files to create.</span></span> <span data-ttu-id="5082c-209">В процессе создания образа восстановления исходные файлы Windows представляют собой распакованные файлы DaRT, и на нем копируется в форматы файлов, которые вы выбираете на этой странице.</span><span class="sxs-lookup"><span data-stu-id="5082c-209">During the recovery image creation process, Windows source files are unpacked, DaRT files are copied to it, and the image is then “re-packed” into the file formats that you select on this page.</span></span>

<span data-ttu-id="5082c-210">Доступные типы файлов изображений:</span><span class="sxs-lookup"><span data-stu-id="5082c-210">The available image file types are:</span></span>

-   <span data-ttu-id="5082c-211">**Файл образов Windows (WIM)** — используется для развертывания DART в среде предзагрузочной среды (PXE) или локальной секции).</span><span class="sxs-lookup"><span data-stu-id="5082c-211">**Windows Imaging File (WIM)** - used to deploy DaRT to a preboot execution environment (PXE) or local partition).</span></span>

-   <span data-ttu-id="5082c-212">**Международная организация по стандартизации (ISO)** — используется для развертывания на компакт-диск или DVD-диск или для использования на виртуальных машинах (ВМ) s).</span><span class="sxs-lookup"><span data-stu-id="5082c-212">**International Standards Organization (ISO)** – used to deploy to CD or DVD, or for use in virtual machines (VM)s).</span></span> <span data-ttu-id="5082c-213">Для мастера требуется, чтобы ISO-образ имел расширение ISO, так как в большинстве программ, которые занимают компакт – диски или DVD-диски требуют этого расширения.</span><span class="sxs-lookup"><span data-stu-id="5082c-213">The wizard requires that the ISO image have an .iso file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="5082c-214">Если вы не укажете другое расположение, на рабочем столе создается образ ISO с именем DaRT10. ISO.</span><span class="sxs-lookup"><span data-stu-id="5082c-214">If you do not specify a different location, the ISO image is created on your desktop with the name DaRT10.ISO.</span></span>

-   <span data-ttu-id="5082c-215">**Сценарий PowerShell** — создает изображение для восстановления DaRT с командами, которые предоставляют те же параметры, которые можно выбрать с помощью мастера создания изображений для восстановления DART.</span><span class="sxs-lookup"><span data-stu-id="5082c-215">**PowerShell script** – creates a DaRT recovery image with commands that provide essentially the same options that you can select by using the DaRT Recovery Image wizard.</span></span> <span data-ttu-id="5082c-216">Кроме того, сценарий позволяет добавлять или изменять файлы в образе для DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-216">The script also enables you to add or changes files in the DaRT recovery image.</span></span>

<span data-ttu-id="5082c-217">Если вы установите флажок Изменить изображение на этой странице, вы можете настроить его в процессе создания образа.</span><span class="sxs-lookup"><span data-stu-id="5082c-217">If you select the Edit Image check box on this page, you can customize the recovery image during the image creation process.</span></span> <span data-ttu-id="5082c-218">Например, вы можете изменить файл "winpeshl.ini", чтобы создать настраиваемый заказ на запуск или добавить сторонние инструменты.</span><span class="sxs-lookup"><span data-stu-id="5082c-218">For example, you can change the “winpeshl.ini” file to create a custom startup order or to add third-party tools.</span></span>

**<span data-ttu-id="5082c-219">Выбор типов создаваемых файлов образа для восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-219">To select the types of recovery image files to create</span></span>**

1.  <span data-ttu-id="5082c-220">На странице **Создание изображения** нажмите кнопку **Обзор** , чтобы выбрать папку вывода для файла изображения.</span><span class="sxs-lookup"><span data-stu-id="5082c-220">On the **Create Image** page, click **Browse** to choose the output folder for the image file.</span></span>

    <span data-ttu-id="5082c-221">**Примечание**  Размер изображения изменяется в зависимости от выбранных вами инструментов и файлов, которые вы добавляете в мастере.</span><span class="sxs-lookup"><span data-stu-id="5082c-221">**Note** The size of the image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

     

2.  <span data-ttu-id="5082c-222">В поле **имя изображения** введите имя для образа восстановления DaRT или подтвердите имя по умолчанию, которое является DaRT10.</span><span class="sxs-lookup"><span data-stu-id="5082c-222">In the **Image name** box, enter a name for the DaRT recovery image, or accept the default name, which is DaRT10.</span></span>

    <span data-ttu-id="5082c-223">Мастер создаст вложенную папку в пути вывода с этим именем.</span><span class="sxs-lookup"><span data-stu-id="5082c-223">The wizard creates a subfolder in the output path by this name.</span></span>

3.  <span data-ttu-id="5082c-224">Выберите типы файлов изображений, которые вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="5082c-224">Select the types of image files that you want to create.</span></span>

4.  <span data-ttu-id="5082c-225">Выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="5082c-225">Choose one of the following:</span></span>

    -   <span data-ttu-id="5082c-226">Чтобы изменить файлы в образе восстановления перед созданием файлов изображений, установите флажок **изменить изображение** и нажмите кнопку **подготовить**.</span><span class="sxs-lookup"><span data-stu-id="5082c-226">To change the files in the recovery image before you create the image files, select the **Edit Image** check box, and then click **Prepare**.</span></span>

    -   <span data-ttu-id="5082c-227">Чтобы создать образ восстановления, не изменяя файлы, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="5082c-227">To create the recovery image without changing the files, click **Create**.</span></span>

5.  

    <span data-ttu-id="5082c-228">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5082c-228">Click **Next**.</span></span>

## <span data-ttu-id="5082c-229">Изменение файлов образа для восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-229">Edit the recovery image files</span></span>


<span data-ttu-id="5082c-230">Изменить изображение восстановления можно только в том случае, если на странице "Создание изображения" установлен флажок "изменить изображение".</span><span class="sxs-lookup"><span data-stu-id="5082c-230">You can edit the recovery image only if you selected the Edit Image check box on the Create Image page.</span></span> <span data-ttu-id="5082c-231">После подготовки образа восстановления для редактирования вы можете добавить и изменить файлы образа для восстановления, прежде чем создавать загрузочный носитель.</span><span class="sxs-lookup"><span data-stu-id="5082c-231">After the recovery image has been prepared for editing, you can add and modify the recovery image files before creating the bootable media.</span></span> <span data-ttu-id="5082c-232">Например, вы можете создать настраиваемый заказ на запуск, добавить другие сторонние инструменты и другие.</span><span class="sxs-lookup"><span data-stu-id="5082c-232">For example, you can create a custom order for startup, add various third-party tools, and so on.</span></span>

**<span data-ttu-id="5082c-233">Редактирование файлов образа восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-233">To edit the recovery image files</span></span>**

1.  <span data-ttu-id="5082c-234">На странице **изменение изображения** нажмите кнопку **Открыть** в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="5082c-234">On the **Edit Image** page, click **Open** in Windows Explorer.</span></span>

2.  <span data-ttu-id="5082c-235">Создайте вложенную папку в папке, которая указана в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5082c-235">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="5082c-236">Скопируйте файлы, которые вы хотите добавить в новую вложенную папку, или удалите ненужные файлы.</span><span class="sxs-lookup"><span data-stu-id="5082c-236">Copy the files that you want to the new subfolder, or remove files that you don’t want.</span></span>

4.  <span data-ttu-id="5082c-237">Нажмите кнопку **создать** , чтобы начать создание образа восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-237">Click **Create** to start creating the recovery image.</span></span>

## <span data-ttu-id="5082c-238">Создание файлов образа для восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-238">Generate the recovery image files</span></span>


<span data-ttu-id="5082c-239">На странице Создание файлов для типов файлов, выбранных на странице Создание образа, создается изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="5082c-239">On the Generate Files page, the DaRT recovery image is generated for the file types that you selected on the Create Image page.</span></span>

**<span data-ttu-id="5082c-240">Создание файлов образа для восстановления</span><span class="sxs-lookup"><span data-stu-id="5082c-240">To generate the recovery image files</span></span>**

-   <span data-ttu-id="5082c-241">На странице **Создание файлов** нажмите кнопку **Далее** , чтобы создать файлы образа для восстановления.</span><span class="sxs-lookup"><span data-stu-id="5082c-241">On the **Generate Files** page, click **Next** to generate the recovery image files.</span></span>

## <span data-ttu-id="5082c-242">Копирование образа для восстановления на компакт-диск, DVD-диск или USB-порт</span><span class="sxs-lookup"><span data-stu-id="5082c-242">Copy the recovery image to a CD, DVD, or USB</span></span>


<span data-ttu-id="5082c-243">На странице Создание загрузочного носителя вы можете при необходимости скопировать файл изображения на компакт-диск, DVD-или USB-накопитель (UFD).</span><span class="sxs-lookup"><span data-stu-id="5082c-243">On the Create Bootable Media page, you can optionally copy the image file to a CD, DVD, or USB flash drive (UFD).</span></span> <span data-ttu-id="5082c-244">Вы также можете создать дополнительные загрузочные носители на этой странице, перезапустите мастер.</span><span class="sxs-lookup"><span data-stu-id="5082c-244">You can also create additional bootable media from this page by restarting the wizard.</span></span>

<span data-ttu-id="5082c-245">**Примечание**  Это средство не поддерживает среду удаленной загрузки (PXE) и локальное развертывание образа, поскольку для них требуются дополнительные корпоративные инструменты, такие как сервер System Center Configuration Manager и Microsoft Development Toolkit.</span><span class="sxs-lookup"><span data-stu-id="5082c-245">**Note** The Preboot execution environment (PXE) and local image deployment are not supported natively by this tool since they require additional enterprise tools, such as System Center Configuration Manager server and Microsoft Development Toolkit.</span></span>

 

**<span data-ttu-id="5082c-246">Копирование образа восстановления на компакт-диск, DVD-диск или USB-порт</span><span class="sxs-lookup"><span data-stu-id="5082c-246">To copy the recovery image to a CD, DVD, or USB</span></span>**

1.  <span data-ttu-id="5082c-247">На странице **Создание загрузочного носителя** выберите ISO-файл, который вы хотите скопировать.</span><span class="sxs-lookup"><span data-stu-id="5082c-247">On the **Create Bootable Media** page, select the iso file that you want to copy.</span></span>

2.  <span data-ttu-id="5082c-248">Вставьте компакт-диск, DVD-диск или USB-устройство, а затем выберите диск.</span><span class="sxs-lookup"><span data-stu-id="5082c-248">Insert a CD, DVD, or USB, and then select the drive.</span></span>

    <span data-ttu-id="5082c-249">**Примечание**  Если диск не распознается и вы устанавливаете новый диск, вы можете нажать кнопку **Обновить** , чтобы заставить мастер обновить список доступных дисков.</span><span class="sxs-lookup"><span data-stu-id="5082c-249">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="5082c-250">Нажмите кнопку " **создать загрузочный носитель** ".</span><span class="sxs-lookup"><span data-stu-id="5082c-250">Click the **Create Bootable Media** button.</span></span>

4.  <span data-ttu-id="5082c-251">Чтобы создать еще один образ восстановления, нажмите кнопку перезапустить или нажмите кнопку **Закрыть** , если вы закончите создание всех нужных файлов.</span><span class="sxs-lookup"><span data-stu-id="5082c-251">To create another recovery image, click Restart, or click **Close** if you have finished creating all of the media that you want.</span></span>

## <span data-ttu-id="5082c-252">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="5082c-252">Related topics</span></span>


[<span data-ttu-id="5082c-253">Обзор средств в DaRT 10</span><span class="sxs-lookup"><span data-stu-id="5082c-253">Overview of the Tools in DaRT 10</span></span>](overview-of-the-tools-in-dart-10.md)

[<span data-ttu-id="5082c-254">Развертывание DaRT 10</span><span class="sxs-lookup"><span data-stu-id="5082c-254">Deploying DaRT 10</span></span>](deploying-dart-10.md)

 

 





