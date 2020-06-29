---
title: Обзор средств в DaRT 10
description: Обзор средств в DaRT 10
author: dansimp
ms.assetid: 752467dd-b646-4335-82ce-9090d4651f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8bef2b92e998bebffae526d4288c76be081fe0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822992"
---
# <span data-ttu-id="801fe-103">Обзор средств в DaRT 10</span><span class="sxs-lookup"><span data-stu-id="801fe-103">Overview of the Tools in DaRT 10</span></span>


<span data-ttu-id="801fe-104">В окне **набор инструментов Диагностика и восстановление** в наборе средств диагностики и восстановления Microsoft (DART) 10 вы можете запускать любые отдельные инструменты, которые вы включаете при создании образа для DART 10.</span><span class="sxs-lookup"><span data-stu-id="801fe-104">From the **Diagnostics and Recovery Toolset** window in Microsoft Diagnostics and Recovery Toolset (DaRT) 10, you can start any of the individual tools that you include when you create the DaRT 10 recovery image.</span></span> <span data-ttu-id="801fe-105">Сведения о том, как получить доступ к окну **инструментария диагностики и восстановления** , приведены [в разделе восстановление локальных компьютеров с помощью DaRT Recovery](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="801fe-105">For information about how to access the **Diagnostics and Recovery Toolset** window, see [How to Recover Local Computers by Using the DaRT Recovery Image](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).</span></span>

<span data-ttu-id="801fe-106">Если он доступен, можно воспользоваться **мастером решений** в окне **средства диагностики и восстановления** для выбора средства, которое лучше подходит для конкретной проблемы, на основе короткого собеседования, предоставленного мастером.</span><span class="sxs-lookup"><span data-stu-id="801fe-106">If it is available, you can use the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to select the tool that best addresses your particular issue, based on a brief interview that the wizard provides.</span></span>

## <span data-ttu-id="801fe-107">Обзор инструментов DaRT</span><span class="sxs-lookup"><span data-stu-id="801fe-107">Exploring the DaRT tools</span></span>


<span data-ttu-id="801fe-108">Ниже приведено описание инструментов DaRT 10.</span><span class="sxs-lookup"><span data-stu-id="801fe-108">A description of the DaRT 10 tools follows.</span></span>

### <span data-ttu-id="801fe-109">Управление компьютерами</span><span class="sxs-lookup"><span data-stu-id="801fe-109">Computer Management</span></span>

<span data-ttu-id="801fe-110">**Управление компьютером** — это набор средств администрирования Windows, которые помогают устранить неполадки компьютера.</span><span class="sxs-lookup"><span data-stu-id="801fe-110">**Computer Management** is a collection of Windows administrative tools that help you troubleshoot a problem computer.</span></span> <span data-ttu-id="801fe-111">С помощью средств **управления компьютером** для DART можно просматривать сведения о системе и журналы событий, управлять дисками, автозапусками списков и управлять службами и драйверами.</span><span class="sxs-lookup"><span data-stu-id="801fe-111">You can use the **Computer Management** tools in DaRT to view system information and event logs, manage disks, list autoruns, and manage services and drivers.</span></span> <span data-ttu-id="801fe-112">Настройка консоли **управления компьютером** помогает диагностировать и устранять проблемы, которые могут препятствовать запуску операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="801fe-112">The **Computer Management** console is customized to help you diagnose and repair problems that might be preventing the Windows operating system from starting.</span></span>

<span data-ttu-id="801fe-113">**Примечание**  Восстановление динамических дисков с помощью DaRT не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="801fe-113">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="801fe-114">Анализатор сбоев</span><span class="sxs-lookup"><span data-stu-id="801fe-114">Crash Analyzer</span></span>

<span data-ttu-id="801fe-115">С помощью **мастера анализа сбоев** можно быстро определить причину сбоя компьютера, проанализировав файл дампа памяти в операционной системе Windows, которую вы восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="801fe-115">Use the **Crash Analyzer Wizard** to quickly determine the cause of a computer failure by analyzing the memory dump file on the Windows operating system that you are repairing.</span></span> <span data-ttu-id="801fe-116">Средство **Crash Analyzer** проверяет файл дампа памяти драйвера, который привел к сбою компьютера.</span><span class="sxs-lookup"><span data-stu-id="801fe-116">**Crash Analyzer** examines the memory dump file for the driver that caused a computer to fail.</span></span> <span data-ttu-id="801fe-117">Затем вы можете отключить драйвер устройства с неполадками с помощью узла **службы и драйверы** в средстве **управления компьютером** .</span><span class="sxs-lookup"><span data-stu-id="801fe-117">You can then disable the problem device driver by using the **Services and Drivers** node in the **Computer Management** tool.</span></span>

<span data-ttu-id="801fe-118">**Мастер анализатора сбоев** требует наличия средств отладки для Windows и файлов символов для операционной системы, которую вы восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="801fe-118">The **Crash Analyzer Wizard** requires the Debugging Tools for Windows and symbol files for the operating system that you are repairing.</span></span> <span data-ttu-id="801fe-119">Вы можете включить оба требования при создании изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="801fe-119">You can include both requirements when you create the DaRT recovery image.</span></span> <span data-ttu-id="801fe-120">Если они не включены в образ восстановления, но у вас нет доступа к ним на компьютере, который вы восстанавливаете, вы можете скопировать файл дампа памяти на другой компьютер и использовать изолированную версию **анализатора сбоев** для диагностики проблемы.</span><span class="sxs-lookup"><span data-stu-id="801fe-120">If they are not included on the recovery image and you do not have access to them on the computer that you are repairing, you can copy the memory dump file to another computer and use the stand-alone version of **Crash Analyzer** to diagnose the problem.</span></span>

<span data-ttu-id="801fe-121">Запуск **анализатора сбоев** — это хорошая идея, даже если вы планируете переобразировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="801fe-121">Running **Crash Analyzer** is a good idea even if you plan to reimage the computer.</span></span> <span data-ttu-id="801fe-122">На изображении может быть неисправный драйвер, который вызывает проблемы в среде.</span><span class="sxs-lookup"><span data-stu-id="801fe-122">The image could have a defective driver that is causing problems in your environment.</span></span> <span data-ttu-id="801fe-123">Выполнив **Анализатор аварийного**восстановления, вы можете определить проблемные драйверы и повысить стабильность работы образа.</span><span class="sxs-lookup"><span data-stu-id="801fe-123">By running **Crash Analyzer**, you can identify problem drivers and improve the image stability.</span></span>

<span data-ttu-id="801fe-124">Дополнительные сведения об **анализаторе сбоев**см. [в разделе Диагностика сбоев системы с помощью анализатора сбоев](diagnosing-system-failures-with-crash-analyzer-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="801fe-124">For more information about **Crash Analyzer**, see [Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md).</span></span>

### <span data-ttu-id="801fe-125">Disk Commander</span><span class="sxs-lookup"><span data-stu-id="801fe-125">Disk Commander</span></span>

<span data-ttu-id="801fe-126">**Disk Commander** позволяет восстанавливать и восстанавливать разделы и тома диска с помощью одного из следующих процессов восстановления.</span><span class="sxs-lookup"><span data-stu-id="801fe-126">**Disk Commander** lets you recover and repair disk partitions or volumes by using one of the following recovery processes:</span></span>

-   <span data-ttu-id="801fe-127">Восстановление основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="801fe-127">Restore the master boot record (MBR)</span></span>

-   <span data-ttu-id="801fe-128">Восстановление одного или нескольких потерянных томов</span><span class="sxs-lookup"><span data-stu-id="801fe-128">Recover one or more lost volumes</span></span>

-   <span data-ttu-id="801fe-129">Восстановление таблиц разделов из резервной копии **Disk Commander**</span><span class="sxs-lookup"><span data-stu-id="801fe-129">Restore partition tables from **Disk Commander** backup</span></span>

-   <span data-ttu-id="801fe-130">Сохранение таблиц разделов в резервной копии **диска**</span><span class="sxs-lookup"><span data-stu-id="801fe-130">Save partition tables to **Disk Commander** backup</span></span>

<span data-ttu-id="801fe-131">**Предупреждение**  Рекомендуется создать резервную копию диска перед тем, как восстановить его с помощью **диска** .</span><span class="sxs-lookup"><span data-stu-id="801fe-131">**Warning** We recommend that you back up a disk before you use **Disk Commander** to repair it.</span></span> <span data-ttu-id="801fe-132">С помощью **Disk Commander**вы можете повредить тома и сделать их недоступными.</span><span class="sxs-lookup"><span data-stu-id="801fe-132">By using **Disk Commander**, you can potentially damage volumes and make them inaccessible.</span></span> <span data-ttu-id="801fe-133">Кроме того, изменение одного тома может повлиять на другие тома, так как тома на диске имеют доступ к таблице разделов.</span><span class="sxs-lookup"><span data-stu-id="801fe-133">Additionally, changes to one volume can affect other volumes because volumes on a disk share a partition table.</span></span>

 

<span data-ttu-id="801fe-134">**Примечание**  Восстановление динамических дисков с помощью DaRT не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="801fe-134">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="801fe-135">Очистка диска</span><span class="sxs-lookup"><span data-stu-id="801fe-135">Disk Wipe</span></span>

<span data-ttu-id="801fe-136">С помощью **очистки диска** можно удалить все данные с диска или тома, даже те данные, которые остались после переформатирования жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="801fe-136">You can use **Disk Wipe** to delete all data from a disk or volume, even the data that is left behind after you reformat a hard disk drive.</span></span> <span data-ttu-id="801fe-137">С помощью средства **очистки диска** можно выделять данные из одной или двух проходов, что соответствует текущему Отделу стандартов обороны США.</span><span class="sxs-lookup"><span data-stu-id="801fe-137">**Disk Wipe** lets you select from either a single-pass overwrite or a four-pass overwrite, which meets current U.S. Department of Defense standards.</span></span>

<span data-ttu-id="801fe-138">**Предупреждение**  После того как вы восстановите диск или том, вы не сможете восстановить данные.</span><span class="sxs-lookup"><span data-stu-id="801fe-138">**Warning** After wiping a disk or volume, you cannot recover the data.</span></span> <span data-ttu-id="801fe-139">Проверьте размер и метку тома, прежде чем выполнять его стирание.</span><span class="sxs-lookup"><span data-stu-id="801fe-139">Verify the size and label of a volume before erasing it.</span></span>

 

### <span data-ttu-id="801fe-140">Explorer</span><span class="sxs-lookup"><span data-stu-id="801fe-140">Explorer</span></span>

<span data-ttu-id="801fe-141">С помощью средства **проводник** можно просматривать файловую систему компьютера и сетевые папки, чтобы можно было удалить важные данные, хранящиеся на локальном диске, прежде чем пытаться восстановить или переобразировать компьютер.</span><span class="sxs-lookup"><span data-stu-id="801fe-141">The **Explorer** tool lets you browse the computer’s file system and network shares so that you can remove important data that the user stored on the local drive before you try to repair or reimage the computer.</span></span> <span data-ttu-id="801fe-142">А так как вы можете сопоставить буквы дисков с сетевыми папками, вы можете легко скопировать и переместить файлы с компьютера в сеть для их восстановления или из сети на компьютер.</span><span class="sxs-lookup"><span data-stu-id="801fe-142">And because you can map drive letters to network shares, you can easily copy and move files from the computer to the network for safekeeping or from the network to the computer to restore them.</span></span>

### <span data-ttu-id="801fe-143">Восстановление файлов</span><span class="sxs-lookup"><span data-stu-id="801fe-143">File Restore</span></span>

<span data-ttu-id="801fe-144">**Восстановление файлов** позволяет попытаться восстановить файлы, которые были случайно удалены или слишком велики для помещения в корзину.</span><span class="sxs-lookup"><span data-stu-id="801fe-144">**File Restore** lets you try to restore files that were accidentally deleted or that were too big to fit in the Recycle Bin.</span></span> <span data-ttu-id="801fe-145">**Восстановление файлов** не ограничивается только обычными томами диска, но может находить и восстанавливать файлы на потерянных томах или томах, зашифрованных с помощью BitLocker.</span><span class="sxs-lookup"><span data-stu-id="801fe-145">**File Restore** is not limited to regular disk volumes, but can find and restore files on lost volumes or on volumes that are encrypted by BitLocker.</span></span>

<span data-ttu-id="801fe-146">**Примечание**  Восстановление динамических дисков с помощью DaRT не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="801fe-146">**Note** The recovery of dynamic disks with DaRT is not supported.</span></span>

 

### <span data-ttu-id="801fe-147">Поиск файлов</span><span class="sxs-lookup"><span data-stu-id="801fe-147">File Search</span></span>

<span data-ttu-id="801fe-148">Перед тем как reimaging компьютер, необходимо восстановить файлы с локального жесткого диска, особенно если пользователь не имел резервных копий или не хранил файлы в другом месте.</span><span class="sxs-lookup"><span data-stu-id="801fe-148">Before reimaging a computer, recovering files from the local hard disk is important, especially when the user might not have backed up or stored the files elsewhere.</span></span>

<span data-ttu-id="801fe-149">Средство **поиска** открывает окно **поиска файлов** , которое можно использовать для поиска документов, если вы не знаете путь к файлу или не можете искать файлы общего типа на всех локальных дисках.</span><span class="sxs-lookup"><span data-stu-id="801fe-149">The **Search** tool opens a **File Search** window that you can use to find documents when you do not know the file path or to search for general kinds of files across all local hard disks.</span></span> <span data-ttu-id="801fe-150">Вы можете искать определенные шаблоны имен файлов в конкретных путях.</span><span class="sxs-lookup"><span data-stu-id="801fe-150">You can search for specific file-name patterns in specific paths.</span></span> <span data-ttu-id="801fe-151">Вы также можете ограничить результаты диапазоном дат или диапазоном размеров.</span><span class="sxs-lookup"><span data-stu-id="801fe-151">You can also limit results to a date range or size range.</span></span>

### <span data-ttu-id="801fe-152">Удаление исправления</span><span class="sxs-lookup"><span data-stu-id="801fe-152">Hotfix Uninstall</span></span>

<span data-ttu-id="801fe-153">С помощью **мастера удаления исправления** вы можете удалить из операционной системы Windows исправления и пакеты обновления, установленные на компьютере, который вы хотите восстановить.</span><span class="sxs-lookup"><span data-stu-id="801fe-153">The **Hotfix Uninstall Wizard** lets you remove hotfixes or service packs from the Windows operating system on the computer that you are repairing.</span></span> <span data-ttu-id="801fe-154">Это средство следует использовать в том случае, если вы препятствует запуску операционной системы с помощью исправления или пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="801fe-154">Use this tool when a hotfix or service pack is suspected in preventing the operating system from starting.</span></span>

<span data-ttu-id="801fe-155">Мы рекомендуем удалить только одно исправление в каждый момент времени, даже если это средство позволяет удалить более одного.</span><span class="sxs-lookup"><span data-stu-id="801fe-155">We recommend that you uninstall only one hotfix at a time, even though the tool lets you uninstall more than one.</span></span>

<span data-ttu-id="801fe-156">**Важно!**  Программы, которые были установлены или обновлены после установки исправления, могут работать неправильно после удаления исправления.</span><span class="sxs-lookup"><span data-stu-id="801fe-156">**Important** Programs that were installed or updated after a hotfix was installed might not work correctly after you uninstall a hotfix.</span></span>

 

### <span data-ttu-id="801fe-157">Locksmith</span><span class="sxs-lookup"><span data-stu-id="801fe-157">Locksmith</span></span>

<span data-ttu-id="801fe-158">**Мастер Locksmith** позволяет задать или изменить пароль для любой локальной учетной записи в операционной системе Windows, которую вы анализируете или восстанавливаете.</span><span class="sxs-lookup"><span data-stu-id="801fe-158">The **Locksmith Wizard** lets you set or change the password for any local account on the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="801fe-159">Вам не нужно знать текущий пароль.</span><span class="sxs-lookup"><span data-stu-id="801fe-159">You do not have to know the current password.</span></span> <span data-ttu-id="801fe-160">Тем не менее, заданный вами пароль должен соответствовать требованиям, определенным локальным объектом групповой политики.</span><span class="sxs-lookup"><span data-stu-id="801fe-160">However, the password that you set must comply with any requirements that are defined by a local Group Policy Object.</span></span> <span data-ttu-id="801fe-161">Это относится к длине и сложности паролей.</span><span class="sxs-lookup"><span data-stu-id="801fe-161">This includes password length and complexity.</span></span>

<span data-ttu-id="801fe-162">Вы можете использовать **Locksmith** , когда пароль для локальной учетной записи, например учетной записи локального администратора, неизвестен.</span><span class="sxs-lookup"><span data-stu-id="801fe-162">You can use **Locksmith** when the password for a local account, such as the local Administrator account, is unknown.</span></span> <span data-ttu-id="801fe-163">Вы не можете использовать **Locksmith** , чтобы установить пароли для учетных записей домена.</span><span class="sxs-lookup"><span data-stu-id="801fe-163">You cannot use **Locksmith** to set passwords for domain accounts.</span></span>

### <span data-ttu-id="801fe-164">Редактор реестра</span><span class="sxs-lookup"><span data-stu-id="801fe-164">Registry Editor</span></span>

<span data-ttu-id="801fe-165">Вы можете использовать **редактор реестра** для доступа к реестру операционной системы Windows, которую вы анализируете или восстанавливаете, и изменения ее параметров.</span><span class="sxs-lookup"><span data-stu-id="801fe-165">You can use **Registry Editor** to access and change the registry of the Windows operating system that you are analyzing or repairing.</span></span> <span data-ttu-id="801fe-166">Сюда входят добавление, удаление и редактирование ключей и значений, а также импорт файлов реестра (REG).</span><span class="sxs-lookup"><span data-stu-id="801fe-166">This includes adding, removing, and editing keys and values, and importing registry (.reg) files.</span></span>

<span data-ttu-id="801fe-167">**Предупреждение**  Неправильное изменение реестра с помощью **редактора реестра**может привести к серьезным неполадкам.</span><span class="sxs-lookup"><span data-stu-id="801fe-167">**Warning** Serious problems can occur if you change the registry incorrectly by using **Registry Editor**.</span></span> <span data-ttu-id="801fe-168">Эти проблемы могут привести к необходимости переустановки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="801fe-168">These problems might require you to reinstall the operating system.</span></span> <span data-ttu-id="801fe-169">Прежде чем вносить изменения в реестр, необходимо создать резервную копию всех важных данных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="801fe-169">Before you make changes to the registry, you should back up any valued data on the computer.</span></span> <span data-ttu-id="801fe-170">Изменение реестра на свой страх и риск.</span><span class="sxs-lookup"><span data-stu-id="801fe-170">Change the registry at your own risk.</span></span>

 

### <span data-ttu-id="801fe-171">Проверка для SFC</span><span class="sxs-lookup"><span data-stu-id="801fe-171">SFC Scan</span></span>

<span data-ttu-id="801fe-172">Средство **SFC Scan** запускает **Мастер восстановления системных файлов** и позволяет восстановить системные файлы, препятствующие запуску установленной операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="801fe-172">The **SFC Scan** tool starts the **System File Repair Wizard** and lets you repair system files that are preventing the installed Windows operating system from starting.</span></span> <span data-ttu-id="801fe-173">**Мастер восстановления системных файлов** может автоматически восстанавливать поврежденные или отсутствующие системные файлы, а также может запрашивать подтверждение перед выполнением каких – либо исправлений.</span><span class="sxs-lookup"><span data-stu-id="801fe-173">The **System File Repair Wizard** can automatically repair system files that are corrupted or missing, or it can prompt you before it performs any repairs.</span></span>

### <span data-ttu-id="801fe-174">Мастер решений</span><span class="sxs-lookup"><span data-stu-id="801fe-174">Solution Wizard</span></span>

<span data-ttu-id="801fe-175">**Мастер решений** предлагает ряд вопросов, а затем предлагает наиболее подходящее средство для ситуации в зависимости от ваших ответов.</span><span class="sxs-lookup"><span data-stu-id="801fe-175">The **Solution Wizard** presents a series of questions and then recommends the best tool for the situation, based on your answers.</span></span> <span data-ttu-id="801fe-176">Этот мастер поможет вам определить, какой инструмент следует использовать, если вы не знакомы с инструментами на DaRT.</span><span class="sxs-lookup"><span data-stu-id="801fe-176">This wizard helps you determine which tool to use when you are not familiar with the tools in DaRT.</span></span>

### <span data-ttu-id="801fe-177">Конфигурация TCP/IP</span><span class="sxs-lookup"><span data-stu-id="801fe-177">TCP/IP Config</span></span>

<span data-ttu-id="801fe-178">Когда вы загружаете на DaRT компьютер с проблемой, он автоматически получает настройки TCP/IP (IP-адрес и DNS-сервер) от протокола DHCP (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="801fe-178">When you boot a problem computer into DaRT, it is set to automatically obtain its TCP/IP configuration (IP address and DNS server) from Dynamic Host Configuration Protocol (DHCP).</span></span> <span data-ttu-id="801fe-179">Если служба DHCP недоступна, вы можете вручную настроить протокол TCP/IP с помощью средства **настройки TCP/IP** .</span><span class="sxs-lookup"><span data-stu-id="801fe-179">If DHCP is unavailable, you can manually configure TCP/IP by using the **TCP/IP Config** tool.</span></span> <span data-ttu-id="801fe-180">Сначала выберите сетевой адаптер и настройте IP-адрес и DNS-сервер для этого адаптера.</span><span class="sxs-lookup"><span data-stu-id="801fe-180">You first select a network adapter, and then configure the IP address and DNS server for that adapter.</span></span>

## <span data-ttu-id="801fe-181">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="801fe-181">Related topics</span></span>


[<span data-ttu-id="801fe-182">Начало работы с DaRT 10</span><span class="sxs-lookup"><span data-stu-id="801fe-182">Getting Started with DaRT 10</span></span>](getting-started-with-dart-10.md)

 

 





