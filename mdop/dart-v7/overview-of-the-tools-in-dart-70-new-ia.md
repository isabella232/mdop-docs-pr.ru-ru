---
title: Обзор средств в DaRT 7.0
description: Обзор средств в DaRT 7.0
author: dansimp
ms.assetid: 67c5991e-cbe6-4ce9-9fe5-f1761369d1fe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d327e14fd1851f0e0d82e1c3ad692bcf7842a835
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823442"
---
# <span data-ttu-id="c7f11-103">Обзор средств в DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="c7f11-103">Overview of the Tools in DaRT 7.0</span></span>


<span data-ttu-id="c7f11-104">В окне **набор инструментов Диагностика и восстановление** в наборе средств диагностики и восстановления Microsoft (DART) 7 вы можете запускать любые отдельные инструменты, которые были включены при создании изображения для восстановления DART.</span><span class="sxs-lookup"><span data-stu-id="c7f11-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT)7, you can start any of the individual tools that were included when the DaRT recovery image was created.</span></span> <span data-ttu-id="c7f11-105">Сведения о том, как получить доступ к окну " **инструменты диагностики и восстановления** ", приведены [в разделе восстановление локальных компьютеров с помощью DaRT Recovery](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="c7f11-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers Using the DaRT Recovery Image](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

<span data-ttu-id="c7f11-106">Если он доступен, вы можете воспользоваться **мастером решений** в окне **средства диагностики и восстановления** , чтобы выбрать средство, которое наилучшим решением будет решить определенную ошибку, в зависимости от того, какое из них прошло.</span><span class="sxs-lookup"><span data-stu-id="c7f11-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview.</span></span>

## <span data-ttu-id="c7f11-107">Обзор инструментов DaRT</span><span class="sxs-lookup"><span data-stu-id="c7f11-107">Exploring the DaRT Tools</span></span>


<span data-ttu-id="c7f11-108">В этом разделе описаны различные инструменты, которые являются частью DaRT.</span><span class="sxs-lookup"><span data-stu-id="c7f11-108">This section describes the various tools that are part of DaRT.</span></span>

### <span data-ttu-id="c7f11-109">Редактор реестра</span><span class="sxs-lookup"><span data-stu-id="c7f11-109">Registry Editor</span></span>

<span data-ttu-id="c7f11-110">Вы можете использовать **редактор реестра** для доступа к реестру операционной системы Windows, которую вы анализируете или восстанавливаете, и изменения ее параметров.</span><span class="sxs-lookup"><span data-stu-id="c7f11-110">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="c7f11-111">Сюда входят добавление, удаление и редактирование ключей и значений, а также импорт файлов реестра (REG).</span><span class="sxs-lookup"><span data-stu-id="c7f11-111">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="c7f11-112">**Внимание!**  В этой статье описано, как изменить реестр Windows с помощью редактора реестра.</span><span class="sxs-lookup"><span data-stu-id="c7f11-112">**Caution** This topic describes how to change the Windows registry by using Registry Editor.</span></span> <span data-ttu-id="c7f11-113">Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows.</span><span class="sxs-lookup"><span data-stu-id="c7f11-113">If you change the Windows registry incorrectly, you can cause serious problems that might require you to reinstall Windows.</span></span> <span data-ttu-id="c7f11-114">Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat).</span><span class="sxs-lookup"><span data-stu-id="c7f11-114">You should make a backup copy of the registry files (System.dat and User.dat) before you change the registry.</span></span> <span data-ttu-id="c7f11-115">Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены.</span><span class="sxs-lookup"><span data-stu-id="c7f11-115">Microsoft cannot guarantee that the problems that might occur when you change the registry can be resolved.</span></span> <span data-ttu-id="c7f11-116">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="c7f11-116">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="c7f11-117">Locksmith</span><span class="sxs-lookup"><span data-stu-id="c7f11-117">Locksmith</span></span>

<span data-ttu-id="c7f11-118">**Мастер Locksmith** позволяет задать или изменить пароль для любой локальной учетной записи в операционной системе Windows, которую вы анализируете или восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="c7f11-118">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="c7f11-119">Вам не нужно знать текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="c7f11-119">You do not have to know the current password.</span></span> <span data-ttu-id="c7f11-120">Тем не менее, заданный вами пароль должен соответствовать требованиям, определенным локальным объектом групповой политики.</span><span class="sxs-lookup"><span data-stu-id="c7f11-120">However, the password that you set must comply with any requirements that are defined by a local Group Policy object.</span></span> <span data-ttu-id="c7f11-121">Это относится к длине и сложности паролей.</span><span class="sxs-lookup"><span data-stu-id="c7f11-121">This includes password length and complexity.</span></span>

<span data-ttu-id="c7f11-122">Вы можете использовать **Locksmith** , когда пароль для локальной учетной записи, например учетной записи локального администратора, неизвестен.</span><span class="sxs-lookup"><span data-stu-id="c7f11-122">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="c7f11-123">Вы не можете использовать **Locksmith** , чтобы установить пароли для учетных записей домена.</span><span class="sxs-lookup"><span data-stu-id="c7f11-123">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="c7f11-124">Анализатор сбоев</span><span class="sxs-lookup"><span data-stu-id="c7f11-124">Crash Analyzer</span></span>

<span data-ttu-id="c7f11-125">С помощью **мастера анализа сбоев** можно быстро определить причину сбоя компьютера, проанализировав файл дампа памяти в операционной системе Windows, которую вы восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="c7f11-125">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer crash by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="c7f11-126">Средство **Crash Analyzer** проверяет файл аварийного дампа для драйвера, который привел к сбою компьютера.</span><span class="sxs-lookup"><span data-stu-id="c7f11-126">**Crash Analyzer** examines the crash dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="c7f11-127">Затем вы можете отключить драйвер устройства с неполадками с помощью узла **службы и драйверы** в средстве **управления компьютером** .</span><span class="sxs-lookup"><span data-stu-id="c7f11-127">Then, you can disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="c7f11-128">**Мастер анализатора сбоев** требует наличия средств отладки для Windows и файлов символов для операционной системы, которую вы восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="c7f11-128">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="c7f11-129">Вы можете включить оба требования при создании изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="c7f11-129">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="c7f11-130">Если они не включены в образ восстановления, но у вас нет доступа к ним на компьютере, который вы восстанавливаете, вы можете скопировать файл дампа памяти на другой компьютер и использовать изолированную версию **анализатора сбоев** для диагностики проблемы.</span><span class="sxs-lookup"><span data-stu-id="c7f11-130">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="c7f11-131">Запуск **анализатора сбоев** — это хорошая идея, даже если вы планируете переобразировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="c7f11-131">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="c7f11-132">На изображении может быть неисправный драйвер, который вызывает проблемы в среде.</span><span class="sxs-lookup"><span data-stu-id="c7f11-132">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="c7f11-133">Выполнив **Анализатор аварийного**восстановления, вы можете определить проблемные драйверы и повысить стабильность работы образа.</span><span class="sxs-lookup"><span data-stu-id="c7f11-133">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="c7f11-134">Дополнительные сведения об **анализаторе сбоев**см. [в разделе Диагностика сбоев системы с помощью анализатора сбоев](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="c7f11-134">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-7.md).</span></span>

### <span data-ttu-id="c7f11-135">Восстановление файлов</span><span class="sxs-lookup"><span data-stu-id="c7f11-135">File Restore</span></span>

<span data-ttu-id="c7f11-136">**Восстановление файлов** позволяет попытаться восстановить файлы, которые были случайно удалены или слишком велики для помещения в корзину.</span><span class="sxs-lookup"><span data-stu-id="c7f11-136">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="c7f11-137">**Восстановление файлов** не ограничивается только обычными томами диска, но может находить и восстанавливать файлы на потерянных томах или томах, зашифрованных с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c7f11-137">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

### <span data-ttu-id="c7f11-138">Disk Commander</span><span class="sxs-lookup"><span data-stu-id="c7f11-138">Disk Commander</span></span>

<span data-ttu-id="c7f11-139">**Disk Commander** позволяет восстанавливать и восстанавливать разделы и тома диска с помощью одного из следующих процессов восстановления.</span><span class="sxs-lookup"><span data-stu-id="c7f11-139">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="c7f11-140">Восстановление основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="c7f11-140">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="c7f11-141">Восстановление одного или нескольких потерянных томов</span><span class="sxs-lookup"><span data-stu-id="c7f11-141">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="c7f11-142">Восстановление таблиц разделов из резервной копии **Disk Commander**</span><span class="sxs-lookup"><span data-stu-id="c7f11-142">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="c7f11-143">Сохранение таблиц разделов в резервной копии **диска**</span><span class="sxs-lookup"><span data-stu-id="c7f11-143">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="c7f11-144">**Предупреждение**  Рекомендуется создать резервную копию диска перед тем, как восстановить его с помощью **диска** .</span><span class="sxs-lookup"><span data-stu-id="c7f11-144">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="c7f11-145">С помощью **Disk Commander**вы можете повредить тома и сделать их недоступными.</span><span class="sxs-lookup"><span data-stu-id="c7f11-145">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="c7f11-146">Кроме того, изменение одного тома может повлиять на другие тома, так как тома на диске имеют доступ к таблице разделов.</span><span class="sxs-lookup"><span data-stu-id="c7f11-146">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

### <span data-ttu-id="c7f11-147">Очистка диска</span><span class="sxs-lookup"><span data-stu-id="c7f11-147">Disk Wipe</span></span>

<span data-ttu-id="c7f11-148">С помощью **очистки диска** можно удалить все данные с диска или тома, даже те данные, которые остались после переформатирования жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="c7f11-148">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="c7f11-149">С помощью средства **очистки диска** можно выделять данные из одной или двух проходов, что соответствует текущему Отделу стандартов обороны США.</span><span class="sxs-lookup"><span data-stu-id="c7f11-149">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="c7f11-150">**Предупреждение**  После того как вы восстановите диск или том, вы не сможете восстановить данные.</span><span class="sxs-lookup"><span data-stu-id="c7f11-150">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="c7f11-151">Проверьте размер и метку тома, прежде чем выполнять его стирание.</span><span class="sxs-lookup"><span data-stu-id="c7f11-151">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="c7f11-152">Управление компьютерами</span><span class="sxs-lookup"><span data-stu-id="c7f11-152">Computer Management</span></span>

<span data-ttu-id="c7f11-153">**Управление компьютером** — это набор средств администрирования Windows, которые помогают устранить неполадки компьютера.</span><span class="sxs-lookup"><span data-stu-id="c7f11-153">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="c7f11-154">С помощью средств **управления компьютером** для DART можно просматривать сведения о системе и журналы событий, управлять дисками, автозапусками списков и управлять службами и драйверами.</span><span class="sxs-lookup"><span data-stu-id="c7f11-154">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="c7f11-155">Настройка консоли **управления компьютером** помогает диагностировать и устранять проблемы, которые могут препятствовать запуску операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="c7f11-155">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

### <span data-ttu-id="c7f11-156">Explorer</span><span class="sxs-lookup"><span data-stu-id="c7f11-156">Explorer</span></span>

<span data-ttu-id="c7f11-157">С помощью средства **проводник** можно просматривать файловую систему компьютера и сетевые папки, чтобы можно было удалить важные данные, хранящиеся на локальном диске, прежде чем пытаться восстановить или переобразировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="c7f11-157">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="c7f11-158">А так как вы можете сопоставить буквы дисков с сетевыми папками, вы можете легко скопировать и переместить файлы с компьютера в сеть для их восстановления или из сети на компьютер.</span><span class="sxs-lookup"><span data-stu-id="c7f11-158">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="c7f11-159">Мастер решений</span><span class="sxs-lookup"><span data-stu-id="c7f11-159">Solution Wizard</span></span>

<span data-ttu-id="c7f11-160">**Мастер решений** предлагает ряд вопросов, а затем предлагает наиболее подходящее средство для ситуации в зависимости от ваших ответов.</span><span class="sxs-lookup"><span data-stu-id="c7f11-160">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="c7f11-161">Этот мастер поможет вам определить, какой инструмент следует использовать, если вы не знакомы с инструментами на DaRT.</span><span class="sxs-lookup"><span data-stu-id="c7f11-161">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="c7f11-162">Конфигурация TCP/IP</span><span class="sxs-lookup"><span data-stu-id="c7f11-162">TCP/IP Config</span></span>

<span data-ttu-id="c7f11-163">Когда вы загружаете на DaRT компьютер с проблемой, он автоматически получает настройки TCP/IP (IP-адрес и DNS-сервер) от протокола DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="c7f11-163">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="c7f11-164">Если служба DHCP недоступна, вы можете вручную настроить протокол TCP/IP с помощью средства **настройки TCP/IP** .</span><span class="sxs-lookup"><span data-stu-id="c7f11-164">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="c7f11-165">Сначала выберите сетевой адаптер и настройте IP-адрес и DNS-сервер для этого адаптера.</span><span class="sxs-lookup"><span data-stu-id="c7f11-165">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

### <span data-ttu-id="c7f11-166">Удаление исправления</span><span class="sxs-lookup"><span data-stu-id="c7f11-166">Hotfix Uninstall</span></span>

<span data-ttu-id="c7f11-167">С помощью **мастера удаления исправления** вы можете удалить из операционной системы Windows исправления и пакеты обновления, установленные на компьютере, который вы хотите восстановить.</span><span class="sxs-lookup"><span data-stu-id="c7f11-167">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="c7f11-168">Это средство следует использовать в том случае, если вы препятствует запуску операционной системы с помощью исправления или пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="c7f11-168">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="c7f11-169">Мы рекомендуем удалить только одно исправление в каждый момент времени, даже если это средство позволяет удалить более одного.</span><span class="sxs-lookup"><span data-stu-id="c7f11-169">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="c7f11-170">**Важно!**  Программы, которые были установлены или обновлены после установки исправления, могут работать неправильно после удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="c7f11-170">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="c7f11-171">Проверка для SFC</span><span class="sxs-lookup"><span data-stu-id="c7f11-171">SFC Scan</span></span>

<span data-ttu-id="c7f11-172">Средство **SFC Scan** запускает **Мастер восстановления системных файлов** и позволяет восстановить системные файлы, препятствующие запуску установленной операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="c7f11-172">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="c7f11-173">**Мастер восстановления системных файлов** может автоматически восстанавливать поврежденные или отсутствующие системные файлы, а также может запрашивать подтверждение перед выполнением каких – либо исправлений.</span><span class="sxs-lookup"><span data-stu-id="c7f11-173">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="c7f11-174">Поиск</span><span class="sxs-lookup"><span data-stu-id="c7f11-174">Search</span></span>

<span data-ttu-id="c7f11-175">Перед тем как reimaging компьютер, необходимо восстановить файлы с локального жесткого диска, особенно если пользователь не имел резервных копий или не хранил файлы в другом месте.</span><span class="sxs-lookup"><span data-stu-id="c7f11-175">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="c7f11-176">Средство **поиска** открывает окно **поиска файлов** , которое можно использовать для поиска документов, если вы не знаете путь к файлу или не можете искать файлы общего типа на всех локальных дисках.</span><span class="sxs-lookup"><span data-stu-id="c7f11-176">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="c7f11-177">Вы можете искать определенные шаблоны имен файлов в конкретных путях.</span><span class="sxs-lookup"><span data-stu-id="c7f11-177">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="c7f11-178">Вы также можете ограничить результаты диапазоном дат или диапазоном размеров.</span><span class="sxs-lookup"><span data-stu-id="c7f11-178">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="c7f11-179">Автономное средство очистки системы</span><span class="sxs-lookup"><span data-stu-id="c7f11-179">Standalone System Sweeper</span></span>

<span data-ttu-id="c7f11-180">**Важно!**  Среды с развернутым автономным чистильщиком системы должны вместо этого использовать образ защиты от Microsoft Defender Offline (WDO) для обнаружения вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="c7f11-180">**Important** Environments with the Standalone System Sweeper deployed should instead use the Microsoft Defender Offline (WDO) protection image for malware detection.</span></span> <span data-ttu-id="c7f11-181">Из-за того, как средство для средства очистки системы интегрируется в DaRT, все поддерживаемые развертывания версий DaRT не могут применять эти обновления для защиты от вредоносных программ к изображениям DaRT.</span><span class="sxs-lookup"><span data-stu-id="c7f11-181">Because of how the Standalone System Sweeper tool integrates into DaRT, all supported DaRT version deployments cannot apply these anti-malware updates to their DaRT images.</span></span>

 

<span data-ttu-id="c7f11-182">**Автономное средство очистки системы** помогает обнаружить вредоносные и нежелательные программы и предупреждать о рисках нарушения безопасности.</span><span class="sxs-lookup"><span data-stu-id="c7f11-182">The **Standalone System Sweeper** can help detect malware and unwanted software and warn you of security risks.</span></span> <span data-ttu-id="c7f11-183">Вы можете использовать это средство для проверки компьютера и удаления вредоносных программ, даже если установленная операционная система Windows не запущена.</span><span class="sxs-lookup"><span data-stu-id="c7f11-183">You can use this tool to scan a computer for and remove malware even when the installed Windows operating system is not running.</span></span> <span data-ttu-id="c7f11-184">Когда **автономный средство очистки системы** обнаруживает вредоносные или нежелательные программы, оно предлагает удалить, включить или отключить их для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="c7f11-184">When the **Standalone System Sweeper** detects malicious or unwanted software, it prompts you to remove, quarantine, or allow for each item.</span></span>

<span data-ttu-id="c7f11-185">Вредоносные программы, использующие rootkit, могут быть скрыты от работающей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="c7f11-185">Malware that uses rootkits can mask itself from the running operating system.</span></span> <span data-ttu-id="c7f11-186">Если на компьютере установлена антивирусная программа или шпионское программное обеспечение, в большинстве средств проверки и удаления в реальном времени оно больше не отображается и не удаляется.</span><span class="sxs-lookup"><span data-stu-id="c7f11-186">If a rootkit-enabled virus or spyware is in a computer, most real-time scanning and removal tools can no longer see it or remove it.</span></span> <span data-ttu-id="c7f11-187">Так как вы загружаете проблему на DaRT и установленная операционная система находится в автономном режиме, вы можете обнаружить, что Rootkit-программы не смогут сами ее скрыть.</span><span class="sxs-lookup"><span data-stu-id="c7f11-187">Because you boot the problem computer into DaRT and the installed operating system is offline, you can detect the rootkit without it being able to mask itself.</span></span>

### <span data-ttu-id="c7f11-188">Удаленное соединение</span><span class="sxs-lookup"><span data-stu-id="c7f11-188">Remote Connection</span></span>

<span data-ttu-id="c7f11-189">Средство **удаленного подключения** для DART позволяет удаленно запускать инструменты DART на компьютере с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="c7f11-189">The **Remote Connection** tool in DaRT lets you remotely run the DaRT tools on an end-user computer.</span></span> <span data-ttu-id="c7f11-190">После того как вы закончите определенную информацию конечным пользователем (или специалистом службы поддержки, работающей на компьютере пользователя), ИТ-администратор может управлять компьютером конечного пользователя и удаленно запускать необходимые инструменты DaRT.</span><span class="sxs-lookup"><span data-stu-id="c7f11-190">After certain specific information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="c7f11-191">**Важно!**  Два компьютера, на которых установлено удаленное подключение, должны входить в одну и ту же сеть.</span><span class="sxs-lookup"><span data-stu-id="c7f11-191">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

## <span data-ttu-id="c7f11-192">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c7f11-192">Related topics</span></span>


[<span data-ttu-id="c7f11-193">Начало работы с DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="c7f11-193">Getting Started with DaRT 7.0</span></span>](getting-started-with-dart-70-new-ia.md)

 

 





