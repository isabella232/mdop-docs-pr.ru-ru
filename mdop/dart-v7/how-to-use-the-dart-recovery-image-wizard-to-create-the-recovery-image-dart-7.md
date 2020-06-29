---
title: Использование мастера образа для восстановления DaRT для создания образа для восстановления
description: Использование мастера образа для восстановления DaRT для создания образа для восстановления
author: dansimp
ms.assetid: 1b8ef983-fff9-4d75-a2f6-53120c5c00c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49253a8c0bf9c9073b57712acc773e4a57e31d72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822922"
---
# <span data-ttu-id="1f6c1-103">Использование мастера образа для восстановления DaRT для создания образа для восстановления</span><span class="sxs-lookup"><span data-stu-id="1f6c1-103">How to Use the DaRT Recovery Image Wizard to Create the Recovery Image</span></span>


<span data-ttu-id="1f6c1-104">Набор средств диагностики и восстановления Microsoft (DaRT) 7 включает **мастер изображений для восстановления DaRT** , который используется в Windows для создания загрузочного образа международной организации по стандартизации (ISO).</span><span class="sxs-lookup"><span data-stu-id="1f6c1-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes the **DaRT Recovery Image Wizard** that is used in Windows to create a bootable International Organization for Standardization (ISO) image.</span></span> <span data-ttu-id="1f6c1-105">ISO-образ — это файл, который представляет собой необработанное содержимое компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-105">An ISO image is a file that represents the raw contents of a CD.</span></span>

<span data-ttu-id="1f6c1-106">**Мастеру создания изображений для восстановления DaRT** требуется следующая информация:</span><span class="sxs-lookup"><span data-stu-id="1f6c1-106">The **DaRT Recovery Image Wizard** requires the following information:</span></span>

-   <span data-ttu-id="1f6c1-107">**Загрузочный образ**°, часть которого требуется, необходимо указать путь к установочным файлам на DVD-диске Windows 7 или Windows 7, которые необходимы для создания изображения для восстановления DART.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-107">**Boot Image**˚˚You must provide the path of a Windows 7 DVD or Windows 7 source files that are required to create the DaRT recovery image.</span></span>

-   <span data-ttu-id="1f6c1-108">**Выбор инструментов**на ° по градусам. Вы можете выбрать инструменты, которые нужно включить в изображение для восстановления DART.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-108">**Tool Selection**˚˚You can select the tools to include on the DaRT recovery image.</span></span>

-   <span data-ttu-id="1f6c1-109">**Удаленные соединения**° по-градусы. Вы можете выбрать, нужно ли использовать в качестве изображения восстановления DaRT возможность устанавливать удаленное соединение между службой поддержки и компьютером конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-109">**Remote Connections**˚˚You can select whether you want the DaRT recovery image to include the ability to establish a remote connection between the helpdesk and the end-user computer.</span></span>

-   <span data-ttu-id="1f6c1-110">**Средства отладки для Windows**° ° вам будет предложено указать расположение средств отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-110">**Debugging Tools for Windows**˚˚You are asked to provide the location of the Debugging Tools for Windows.</span></span>

-   <span data-ttu-id="1f6c1-111">**Определения для автономного чистильщика системы**°, в котором вы можете определить, нужно ли скачивать последние определения на момент создания образа восстановления или скачивания определений позже.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-111">**Definitions for Standalone System Sweeper**˚˚You can decide whether to download the latest definitions at the time that you create the recovery image or download the definitions later.</span></span>

-   <span data-ttu-id="1f6c1-112">**Drivers**° с другими драйверами вы запросите, хотите ли вы добавить драйверы к образу ISO.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-112">**Drivers**˚˚You are asked whether you want to add drivers to the ISO image.</span></span>

-   <span data-ttu-id="1f6c1-113">**Дополнительные файлы**, которые могут помочь при диагностике проблем, вы можете добавить файлы в образ ISO °.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-113">**Additional Files**˚˚You can add files to the ISO image that might help diagnose problems.</span></span>

-   <span data-ttu-id="1f6c1-114">**Расположение изображений ISO**°, на которое нужно указать, где должен находиться образ ISO.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-114">**ISO Image Location**˚˚You are asked to specify where the ISO image should be located.</span></span>

-   <span data-ttu-id="1f6c1-115">**Дисковод CD-и DVD-дисков**°, на котором отображается вопрос, нужно ли использовать компакт-диск или DVD-дисковод для записи CD или DVD.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-115">**CD/DVD Drive**˚˚You are asked to specify whether the CD or DVD drive should be used to burn the CD or DVD.</span></span>

<span data-ttu-id="1f6c1-116">**Примечание**  Размер образа ISO может отличаться в зависимости от средств, выбранных в **мастере создания изображений для восстановления DaRT**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-116">**Note** The ISO image size can vary, depending on the tools that were selected in the **DaRT Recovery Image Wizard**.</span></span>

 

## <span data-ttu-id="1f6c1-117">Создание образа восстановления с помощью мастера создания изображений для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-117">To create the recovery image using the DaRT Recovery Image Wizard</span></span>


<span data-ttu-id="1f6c1-118">Следуйте этим инструкциям, чтобы создать изображение для восстановления DaRT с помощью **мастера создания изображений** для средства DART Recovery.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-118">Follow these instructions to use the **DaRT Recovery Image Wizard** to create the DaRT recovery image.</span></span>

### <span data-ttu-id="1f6c1-119">Выбор инструментов для восстановления с помощью DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-119">To select the tools to include on the DaRT recovery image</span></span>

<span data-ttu-id="1f6c1-120">**Мастер создания изображений для восстановления** с помощью DaRT предлагает диалоговое окно " **Выбор инструмента** ".</span><span class="sxs-lookup"><span data-stu-id="1f6c1-120">The **DaRT Recovery Image Wizard** presents a **Tool Selection** dialog box.</span></span> <span data-ttu-id="1f6c1-121">Вы можете выбрать и удалить инструменты из списка инструментов, которые будут включены в изображение для восстановления DaRT, выделив инструмент и нажав кнопку **включить** или **Отключить** .</span><span class="sxs-lookup"><span data-stu-id="1f6c1-121">You can select or remove tools from the list of tools to be included on the DaRT recovery image by highlighting a tool and then clicking the **Enable** or **Disable** buttons.</span></span>

<span data-ttu-id="1f6c1-122">После выбора всех инструментов, которые вы хотите включить в образ восстановления, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-122">After you have selected all the tools that you want to include on the recovery image, click **Next**.</span></span>

### <span data-ttu-id="1f6c1-123">Добавление параметра для разрешения удаленного подключения</span><span class="sxs-lookup"><span data-stu-id="1f6c1-123">To add the option to allow remote connectivity</span></span>

<span data-ttu-id="1f6c1-124">Вы можете установить флажок **Разрешить удаленные подключения** , чтобы предоставить возможность в окне **средств диагностики и восстановления** для установления удаленного соединения между агентом справочной службы и компьютером конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-124">You can select the **Allow remote connections** check box to provide the option in the **Diagnostics and Recovery Toolset** window to establish a remote connection between the helpdesk agent and an end-user computer.</span></span> <span data-ttu-id="1f6c1-125">После того как агент службы поддержки установит удаленное соединение, он сможет запускать инструменты DaRT на компьютере конечного пользователя, находясь в удаленном расположении.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-125">After a helpdesk agent establishes a remote connection, they can run the DaRT tools on the end-user computer from a remote location.</span></span>

<span data-ttu-id="1f6c1-126">Вы можете установить флажок **задать номер порта** , чтобы указать конкретный номер порта, который будет использоваться при установлении удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-126">You can select the **Specify the port number** check box to enter a specific port number that will be used when establishing a remote connection.</span></span> <span data-ttu-id="1f6c1-127">Вы можете указать номер порта в диапазоне от 1 до 65535.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-127">You can specify a port number between 1 and 65535.</span></span> <span data-ttu-id="1f6c1-128">Чтобы свести к минимуму вероятность конфликта, мы рекомендуем использовать номер порта 1024 или выше.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-128">We recommend that the port number be 1024 or higher to minimize the possibility of a conflict.</span></span>

<span data-ttu-id="1f6c1-129">Вы также можете создать настраиваемое сообщение, которое будет получено конечным пользователем при установке удаленного подключения.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-129">You can also create a customized message that an end user will receive when they establish a remote connection.</span></span> <span data-ttu-id="1f6c1-130">Сообщение не может содержать более 2048 символов.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-130">The message can be a maximum of 2048 characters.</span></span>

<span data-ttu-id="1f6c1-131">Дополнительные сведения об удаленном запуске средств DaRT можно найти в статьях [Восстановление удаленных компьютеров с помощью DaRT Recovery](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="1f6c1-131">For more information about remotely running the DaRT tools, see [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

### <span data-ttu-id="1f6c1-132">Добавление средств отладки для Windows в образ восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-132">To add the Debugging Tools for Windows to the DaRT recovery image</span></span>

<span data-ttu-id="1f6c1-133">В диалоговом окне **анализатора аварийного завершения** **мастера создания изображений для восстановления DaRT**вам будет предложено указать расположение средств отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-133">In the **Crash Analyzer** dialog box of the **DaRT Recovery Image Wizard**, you are asked to specify the location of the Debugging Tools for Windows.</span></span> <span data-ttu-id="1f6c1-134">Если у вас нет копии инструментов, вы можете скачать их из Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-134">If you do not have a copy of the tools, you can download them from Microsoft.</span></span> <span data-ttu-id="1f6c1-135">Ниже приведена ссылка на страницу загрузки, указанная в мастере: [скачивание и установка средств отладки для Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span><span class="sxs-lookup"><span data-stu-id="1f6c1-135">The following link to the download page is provided in the wizard: [Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934).</span></span>

<span data-ttu-id="1f6c1-136">Вы можете указать расположение инструментальных средств отладки на компьютере, на котором запущен **Мастер создания образа для восстановления DaRT**, или вы можете использовать инструменты, которые находятся на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-136">You can either specify the location of the debugging tools on the computer where you are running the **DaRT Recovery Image Wizard**, or you can decide to use the tools that are located on the destination computer.</span></span> <span data-ttu-id="1f6c1-137">Если вы решили использовать копию на другом компьютере, необходимо убедиться, что эти средства установлены на всех компьютерах, на которых выполняется диагностика сбоя.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-137">If you decide to use a copy on another computer, you must make sure that the tools are installed on each computer on which you are diagnosing a crash.</span></span>

<span data-ttu-id="1f6c1-138">**Примечание**  Если вы включите в образ ISO- **Analyzer аварийный анализ** , мы рекомендуем вам также включить средства отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-138">**Note** If you include the **Crash Analyzer** in the ISO image, we recommend that you also include the Debugging Tools for Windows.</span></span>

 

<span data-ttu-id="1f6c1-139">Чтобы добавить инструменты отладки для Windows, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-139">Follow these steps to add the Debugging Tools for Windows:</span></span>

1.  <span data-ttu-id="1f6c1-140">Необязательно Щелкните гиперссылку, чтобы загрузить инструменты отладки для Windows.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-140">(Optional) Click the hyperlink to download the Debugging Tools for Windows.</span></span>

2.  <span data-ttu-id="1f6c1-141">Выберите один из следующих вариантов:</span><span class="sxs-lookup"><span data-stu-id="1f6c1-141">Select one of the following options:</span></span>

    -   <span data-ttu-id="1f6c1-142">**Используйте инструменты отладки для Windows в следующем расположении**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-142">**Use the Debugging Tools for Windows in the following location**.</span></span> <span data-ttu-id="1f6c1-143">Если выбрать этот параметр, вы можете перейти к расположению инструментов.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-143">If you select this option, you can browse to the location of the tools.</span></span>

    -   <span data-ttu-id="1f6c1-144">**Найдите инструменты отладки для Windows в системе, которую вы хотите восстановить**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-144">**Locate the Debugging Tools for Windows on the system that you are repairing**.</span></span> <span data-ttu-id="1f6c1-145">Если вы выберете этот параметр, **анализатор сбоев** не будет работать, если средства отладки для Windows не будут найдены на компьютере с неполадками.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-145">If you select this option, the **Crash Analyzer** will not work if the Debugging Tools for Windows are not found on the problem computer.</span></span>

3.  <span data-ttu-id="1f6c1-146">Закончив, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-146">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="1f6c1-147">Добавление определений для автономного очистки системы в образ восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-147">To add definitions for Standalone System Sweeper to the DaRT recovery image</span></span>

<span data-ttu-id="1f6c1-148">Определения — это репозиторий известных вредоносных программ и другой потенциально нежелательной программы.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-148">Definitions are a repository of known malware and other potentially unwanted software.</span></span> <span data-ttu-id="1f6c1-149">Поскольку вредоносные программы постоянно разрабатываются, **автономный** средство проверки системы основывается на текущих определениях, чтобы определить, является ли программное обеспечение, которое пытается установить, запустить или изменить параметры на компьютере, может быть нежелательным или вредоносным программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-149">Because malware is being continually developed, **Standalone System Sweeper** relies on current definitions to determine whether software that is trying to install, run, or change settings on a computer is potentially unwanted or malicious software.</span></span>

<span data-ttu-id="1f6c1-150">Чтобы включить последние определения в изображение для восстановления DaRT (рекомендуемый вариант), нажмите кнопку **Да, чтобы скачать последние определения.**</span><span class="sxs-lookup"><span data-stu-id="1f6c1-150">To include the latest definitions in the DaRT recovery image (recommended), click **Yes, download the latest definitions.**</span></span> <span data-ttu-id="1f6c1-151">Обновление определений запускается автоматически.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-151">The definition update starts automatically.</span></span> <span data-ttu-id="1f6c1-152">Для выполнения этой процедуры необходимо подключение к Интернету.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-152">You must be connected to the Internet to complete this process.</span></span>

<span data-ttu-id="1f6c1-153">Чтобы пропустить обновление определения, нажмите кнопку **нет, загрузив определения позже вручную**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-153">To skip the definition update, click **No, manually download definitions later**.</span></span> <span data-ttu-id="1f6c1-154">Определения не будут включены в образ восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-154">Definitions will not be included in the DaRT recovery image.</span></span>

<span data-ttu-id="1f6c1-155">Если вы решили не включать последние определения в образ восстановления или если определения, включенные в образ восстановления, больше не являются актуальными в момент, когда вы будете готовы использовать **автономный**средство проверки системы, получите последние определения перед началом сканирования, следуя инструкциям, приведенным в **автономном**выходе системы.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-155">If you decide not to include the latest definitions on the recovery image, or if the definitions included on the recovery image are no longer current by the time that you are ready to use **Standalone System Sweeper**, obtain the latest definitions before you begin a scan by following the instructions that are provided in the **Standalone System Sweeper**.</span></span>

<span data-ttu-id="1f6c1-156">**Важно!**  Вы не можете проверить, нет ли каких – либо определений.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-156">**Important** You cannot scan if there are no definitions.</span></span>

 

<span data-ttu-id="1f6c1-157">Закончив, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-157">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="1f6c1-158">Добавление драйверов в образ восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-158">To add drivers to the DaRT recovery image</span></span>

<span data-ttu-id="1f6c1-159">**Внимание!**  По умолчанию при добавлении драйвера в образ восстановления DaRT все дополнительные файлы и вложенные папки, расположенные в этой папке, добавляются в образ восстановления.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-159">**Caution** By default, when you add a driver to the DaRT recovery image, all additional files and subfolders that are located in that folder are added into the recovery image.</span></span> <span data-ttu-id="1f6c1-160">Дополнительные сведения можно найти в разделе [Устранение неполадок DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="1f6c1-160">For more information, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>

 

<span data-ttu-id="1f6c1-161">Вы должны добавить в образ восстановления дополнительные драйверы для DaRT7, которые могут потребоваться при восстановлении компьютера.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-161">You should include additional drivers on the recovery image for DaRT7 that you may need when repairing a computer.</span></span> <span data-ttu-id="1f6c1-162">Сюда обычно относятся устройства хранения данных или сетевые контроллеры, не включенные в DVD-диск Windows.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-162">These may typically include storage or network controllers that are not included on the Windows DVD.</span></span>

<span data-ttu-id="1f6c1-163">**Важно!**  Если вы выбрали драйвер для включения, имейте в виду, что в DaRT не поддерживается беспроводная связь (например, Bluetooth или 802.11 a/b/g/n).</span><span class="sxs-lookup"><span data-stu-id="1f6c1-163">**Important** When you select drivers to include, be aware that wireless connectivity (such as Bluetooth or 802.11a/b/g/n) is not supported in DaRT.</span></span>

 

**<span data-ttu-id="1f6c1-164">Добавление драйвера хранилища или сетевого контроллера в образ восстановления</span><span class="sxs-lookup"><span data-stu-id="1f6c1-164">To add a storage or network controller driver to the recovery image</span></span>**

1.  <span data-ttu-id="1f6c1-165">В диалоговом окне **Дополнительные драйверы** **мастера создания изображений для восстановления DaRT**нажмите кнопку **Добавить устройство**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-165">In the **Additional Drivers** dialog box of the **DaRT Recovery Image Wizard**, click **Add Device**.</span></span>

2.  <span data-ttu-id="1f6c1-166">Перейдите к файлу, который нужно добавить для драйвера, и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-166">Browse to the file to be added for the driver, and then click **Open**.</span></span>

    <span data-ttu-id="1f6c1-167">**Примечание**  Файл **драйвера** предоставляется производителем устройства хранения или сетевого контроллера.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-167">**Note** The **driver** file is provided by the manufacturer of the storage or network controller.</span></span>

     

3.  <span data-ttu-id="1f6c1-168">Повторите действия 1 и 2 для каждого драйвера, который вы хотите включить.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-168">Repeat Steps 1 and 2 for every driver that you want to include.</span></span>

4.  <span data-ttu-id="1f6c1-169">Закончив, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-169">After you have finished, click **Next**.</span></span>

### <span data-ttu-id="1f6c1-170">Добавление файлов в образ восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-170">To add files to the DaRT recovery image</span></span>

<span data-ttu-id="1f6c1-171">Выполните эти действия, чтобы добавить файлы в образ восстановления, чтобы их можно было использовать для диагностики неполадок на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-171">Follow these steps to add files to the recovery image so that you can use them to diagnose computer problems.</span></span>

1.  <span data-ttu-id="1f6c1-172">В диалоговом окне **Дополнительные файлы** **мастера изображений для восстановления DaRT**нажмите кнопку **Показать файлы**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-172">In the **Additional Files** dialog box of the **DaRT Recovery Image Wizard**, click **Show Files**.</span></span> <span data-ttu-id="1f6c1-173">Откроется окно проводника, в котором отображается папка, в которой хранятся общие файлы.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-173">This opens an Explorer window that displays the folder that holds the shared files.</span></span>

2.  <span data-ttu-id="1f6c1-174">Создайте вложенную папку в папке, которая указана в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-174">Create a subfolder in the folder that is listed in the dialog box.</span></span>

3.  <span data-ttu-id="1f6c1-175">Скопируйте файлы, которые вы хотите добавить в новую вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-175">Copy the files that you want to the new subfolder.</span></span>

4.  <span data-ttu-id="1f6c1-176">Закончив, нажмите кнопку **Далее.**</span><span class="sxs-lookup"><span data-stu-id="1f6c1-176">After you have finished, click **Next.**</span></span>

### <span data-ttu-id="1f6c1-177">Выбор расположения ISO-файла, содержащего изображение для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="1f6c1-177">To select a location for the ISO that contains the DaRT recovery image</span></span>

<span data-ttu-id="1f6c1-178">Чтобы указать расположение для создания образа ISO, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-178">Follow these steps to specify the location where the ISO image is created:</span></span>

1.  <span data-ttu-id="1f6c1-179">В диалоговом окне **Создание образа запуска** **мастера изображений для восстановления DaRT**нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-179">In the **Create Startup Image** dialog box of the **DaRT Recovery Image Wizard**, click **Browse**.</span></span>

2.  <span data-ttu-id="1f6c1-180">Найдите нужное расположение в окне " **Сохранить как** " и нажмите кнопку " **сохранить**".</span><span class="sxs-lookup"><span data-stu-id="1f6c1-180">Browse to the preferred location in the **Save As** window, and then click **Save**.</span></span>

3.  <span data-ttu-id="1f6c1-181">Закончив, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-181">After you have finished, click **Next**.</span></span>

<span data-ttu-id="1f6c1-182">Размер образа ISO может зависеть от выбранных вами инструментов и файлов, которые вы добавляете в мастере.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-182">The size of the ISO image will vary, depending on the tools that you select and the files that you add in the wizard.</span></span>

<span data-ttu-id="1f6c1-183">Для мастера требуется, чтобы ISO-образ имел расширение имени **. ISO** , так как в большинстве программ, которые занимают CD или DVD, требуется это расширение.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-183">The wizard requires the ISO image to have an **.iso** file name extension because most programs that burn a CD or DVD require that extension.</span></span> <span data-ttu-id="1f6c1-184">Если вы не укажете другое расположение, на рабочем столе создается образ ISO с именем **DaRT70. ISO**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-184">If you do not specify a different location, the ISO image is created on your desktop with the name **DaRT70.ISO**.</span></span>

### <span data-ttu-id="1f6c1-185">Запись образа восстановления на компакт-диск или DVD-диск</span><span class="sxs-lookup"><span data-stu-id="1f6c1-185">To burn the recovery image to a CD or DVD</span></span>

<span data-ttu-id="1f6c1-186">Если **Мастер создания изображений для восстановления** с помощью DaRT обнаружит на компьютере совместимый дисковод CD-RW, он предложит записать образ ISO на диск.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-186">If the **DaRT Recovery Image Wizard** detects a compatible CD-RW drive on your computer, it offers to burn the ISO image to a disc for you.</span></span> <span data-ttu-id="1f6c1-187">Если вы хотите записать CD или DVD-диск, а мастер не распознает диск, необходимо использовать другую программу, например программу, которая была включена в диск.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-187">If you want to burn a CD or DVD and the wizard does not recognize your drive, you must use another program, such as the program that was included with your drive.</span></span> <span data-ttu-id="1f6c1-188">Вы можете создавать дополнительные копии с помощью дубликата, службы дублирования или программного обеспечения для записи DVD-дисков.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-188">You can use a duplicator, a duplicating service, or CD or DVD-burning software to make any additional copies.</span></span>

1.  <span data-ttu-id="1f6c1-189">В диалоговом окне **записать на компакт-диск или DVD** -диск с помощью **мастера создания изображений для восстановления DaRT**выберите **записать изображение на записываемый компакт-диск или DVD-дисковод**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-189">In the **Burn to a recordable CD/DVD** dialog box of the **DaRT Recovery Image Wizard**, select **Burn the image to the following recordable CD/DVD drive**.</span></span>

2.  <span data-ttu-id="1f6c1-190">Выберите CD или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-190">Select the CD or DVD drive.</span></span>

    <span data-ttu-id="1f6c1-191">**Примечание**  Если диск не распознается и вы установили новый диск, вы можете нажать кнопку **Обновить список дисков** , чтобы заставить мастер обновить список доступных дисков.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-191">**Note** If a drive is not recognized and you install a new drive, you can click **Refresh Drive List** to force the wizard to update the list of available drives.</span></span>

     

3.  <span data-ttu-id="1f6c1-192">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-192">Click **Next**.</span></span>

## <span data-ttu-id="1f6c1-193">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="1f6c1-193">Related topics</span></span>


[<span data-ttu-id="1f6c1-194">Создание образа для восстановления DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="1f6c1-194">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





