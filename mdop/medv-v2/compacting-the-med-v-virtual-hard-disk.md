---
title: Сжатие виртуального жесткого диска MED-V
description: Сжатие виртуального жесткого диска MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823279"
---
# <span data-ttu-id="78588-103">Сжатие виртуального жесткого диска MED-V</span><span class="sxs-lookup"><span data-stu-id="78588-103">Compacting the MED-V Virtual Hard Disk</span></span>


<span data-ttu-id="78588-104">Несмотря на то что этот параметр необязателен, вы можете сжать виртуальный жесткий диск (VHD), чтобы освободить пустое место на диске, а затем уменьшить размер VHD перед настройкой образа Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="78588-104">Although it is optional, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you configure the Windows Virtual PC image.</span></span>

<span data-ttu-id="78588-105">**Важно!**  Прежде чем продолжить, создайте резервную копию образа Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78588-105">**Important** Before you proceed, create a backup copy of your Windows XP image.</span></span>

 

**<span data-ttu-id="78588-106">Подготовка виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="78588-106">Preparing the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="78588-107">Откройте образ Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78588-107">Open your Windows XP image.</span></span>

    <span data-ttu-id="78588-108">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Virtual PC**, **Windows Virtual PC**, а затем дважды щелкните значок Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78588-108">Click **Start**, click **All Programs**, click **Windows Virtual PC**, click **Windows Virtual PC**, then double-click your Windows XP image.</span></span>

2.  <span data-ttu-id="78588-109">Очистите кэш DLL.</span><span class="sxs-lookup"><span data-stu-id="78588-109">Clear the DLL cache.</span></span>

    1.  <span data-ttu-id="78588-110">В командной строке виртуальной машины введите **sfc/CacheSize = 1**.</span><span class="sxs-lookup"><span data-stu-id="78588-110">At a command prompt in the virtual machine, type **sfc /cachesize=1**.</span></span>

    2.  <span data-ttu-id="78588-111">Перезапустите виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="78588-111">Restart the virtual machine.</span></span>

    3.  <span data-ttu-id="78588-112">В командной строке виртуальной машины введите **sfc/purgecache**.</span><span class="sxs-lookup"><span data-stu-id="78588-112">At a command prompt in the virtual machine, type **sfc /purgecache**.</span></span>

3.  <span data-ttu-id="78588-113">Удалите ненужные файлы, такие как программы удаления, временные файлы, файлы журнала, файлы страниц, общие папки и т. д.</span><span class="sxs-lookup"><span data-stu-id="78588-113">Delete unnecessary files, such as uninstallers, temp files, log files, page files, shared folders, and so on.</span></span>

4.  <span data-ttu-id="78588-114">Отключите восстановление системы.</span><span class="sxs-lookup"><span data-stu-id="78588-114">Turn off System Restore.</span></span> <span data-ttu-id="78588-115">Вы также можете указать этот шаг в файле Sysprep. INF.</span><span class="sxs-lookup"><span data-stu-id="78588-115">You can also specify this step in your Sysprep.inf file.</span></span>

    1.  <span data-ttu-id="78588-116">На **панели управления**дважды щелкните значок **система**и выберите вкладку **Восстановление системы** .</span><span class="sxs-lookup"><span data-stu-id="78588-116">In **Control Panel**, double-click **System**, and then select the **System Restore** tab.</span></span>

    2.  <span data-ttu-id="78588-117">Выберите **Отключить восстановление системы**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78588-117">Select **Turn off System Restore**, and then click **OK**.</span></span>

5.  <span data-ttu-id="78588-118">Настройка максимального размера журнала событий и удаление всех событий.</span><span class="sxs-lookup"><span data-stu-id="78588-118">Set maximum event log sizes and clear all events.</span></span>

    1.  <span data-ttu-id="78588-119">Откройте средство просмотра событий.</span><span class="sxs-lookup"><span data-stu-id="78588-119">Open the event viewer.</span></span>

        <span data-ttu-id="78588-120">Нажмите кнопку **Пуск**, выберите пункт **Панель управления**, дважды щелкните элемент **Администрирование**, а затем дважды щелкните **Просмотр событий**.</span><span class="sxs-lookup"><span data-stu-id="78588-120">Click **Start**, click **Control Panel**, double-click **Administrative Tools**, then double-click **Event Viewer**.</span></span>

    2.  <span data-ttu-id="78588-121">Щелкните правой кнопкой мыши **приложение**и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="78588-121">Right-click **Application**, and click **Properties**.</span></span>

    3.  <span data-ttu-id="78588-122">В области **Размер журнала** установите для **максимального размера журнала** значение 512 КБ и выберите параметр **Затирать события по мере необходимости**.</span><span class="sxs-lookup"><span data-stu-id="78588-122">In the **Log Size** area, set **Maximum Log Size** to 512KB and then select **Overwrite events as needed**.</span></span>

    4.  <span data-ttu-id="78588-123">Нажмите **Очистить журнал**.</span><span class="sxs-lookup"><span data-stu-id="78588-123">Click **Clear Log**.</span></span> <span data-ttu-id="78588-124">В появившемся диалоговом окне " **Просмотр событий** " нажмите кнопку **нет**.</span><span class="sxs-lookup"><span data-stu-id="78588-124">In the **Event Viewer** dialog box that appears, click **No**.</span></span>

    5.  <span data-ttu-id="78588-125">В окне " **Свойства** " нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78588-125">In the **Properties** window, click **OK**.</span></span>

    6.  <span data-ttu-id="78588-126">Повторите действия от a до e для журналов **безопасности** и **системы** .</span><span class="sxs-lookup"><span data-stu-id="78588-126">Repeat steps a through e for the **Security** and **System** logs.</span></span>

6.  <span data-ttu-id="78588-127">Запустите средство очистки диска.</span><span class="sxs-lookup"><span data-stu-id="78588-127">Run the Disk Cleanup Tool.</span></span>

    <span data-ttu-id="78588-128">Нажмите кнопку **Пуск**, **выберите все программы**, затем **стандартные**, **выберите пункт Служебные**и нажмите кнопку **Очистка диска**.</span><span class="sxs-lookup"><span data-stu-id="78588-128">Click **Start**, click **All Programs**, click **Accessories**, click **System Tools**, and then click **Disk Cleanup**.</span></span>

7.  <span data-ttu-id="78588-129">Настройте файл на странице в соответствии с вашими требованиями для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="78588-129">Configure your page file as needed for your applications.</span></span>

    1.  <span data-ttu-id="78588-130">На **панели управления**дважды щелкните значок **система**и перейдите на вкладку **Дополнительно** .</span><span class="sxs-lookup"><span data-stu-id="78588-130">In **Control Panel**, double-click **System**, and then select the **Advanced** tab.</span></span>

    2.  <span data-ttu-id="78588-131">В области **Performance (производительность** ) нажмите кнопку **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="78588-131">In the **Performance** area, click **Settings**.</span></span>

    3.  <span data-ttu-id="78588-132">В области **Виртуальная память** нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="78588-132">In the **Virtual Memory** area, click **Change**.</span></span>

    4.  <span data-ttu-id="78588-133">Настройка параметров файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="78588-133">Configure your page file settings.</span></span>

8.  <span data-ttu-id="78588-134">Завершите работу с изображением Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78588-134">Shut down the Windows XP image.</span></span>

**<span data-ttu-id="78588-135">Дефрагментация и предварительное сжатие виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="78588-135">Defragmenting and Pre-compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="78588-136">На главном компьютере под управлением Windows 7 на **панели управления** выберите элемент **Администрирование**, дважды щелкните **Управление компьютером**, а затем — **Управление дисками**.</span><span class="sxs-lookup"><span data-stu-id="78588-136">In **Control Panel** on the host computer that is running Windows 7, click **Administrative Tools**, double-click **Computer Management**, then click **Disk Management**.</span></span>

2.  <span data-ttu-id="78588-137">С помощью консоли управления дисками Прикрепите (Подключите) виртуальный жесткий диск и Дефрагментация диска.</span><span class="sxs-lookup"><span data-stu-id="78588-137">By using the Disk Management Console, attach (mount) the virtual hard disk and then defragment the disk.</span></span>

3.  <span data-ttu-id="78588-138">С помощью средства извлечения ISO-файлов извлеките файлы из файла recompact. ISO, расположенного в папке \\Program Files\\Windows Virtual PC\\Integration Components.</span><span class="sxs-lookup"><span data-stu-id="78588-138">By using an ISO extraction tool, extract the precompact.iso located in the \\Program Files\\Windows Virtual PC\\Integration Components folder.</span></span>

4.  <span data-ttu-id="78588-139">Используйте программу precompact.exe для сжатия виртуального жесткого диска Windows XP.</span><span class="sxs-lookup"><span data-stu-id="78588-139">Use the precompact.exe program to compress the Windows XP virtual hard disk.</span></span>

5.  <span data-ttu-id="78588-140">С помощью консоли управления дисками отключите виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="78588-140">By using the Disk Management Console, detach the virtual hard disk.</span></span>

**<span data-ttu-id="78588-141">Сжатие виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="78588-141">Compacting the Virtual Hard Disk</span></span>**

1.  <span data-ttu-id="78588-142">Откройте Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="78588-142">Open Windows Virtual PC.</span></span>

    <span data-ttu-id="78588-143">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Virtual PC**и **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="78588-143">Click **Start**, click **All Programs**, click **Windows Virtual PC**, then click **Windows Virtual PC**.</span></span>

2.  <span data-ttu-id="78588-144">Щелкните правой кнопкой мыши образ Windows XP и выберите пункт **Параметры**.</span><span class="sxs-lookup"><span data-stu-id="78588-144">Right-click your Windows XP image and select **Settings**.</span></span>

3.  <span data-ttu-id="78588-145">Выберите **жесткий диск** , соответствующий вашему образу Windows XP, и нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="78588-145">Click **Hard Disk** for the one that corresponds to your Windows XP image, and then click **Modify**.</span></span>

4.  <span data-ttu-id="78588-146">Выберите **Сжатие виртуального жесткого диска**.</span><span class="sxs-lookup"><span data-stu-id="78588-146">Click **Compact virtual hard disk**.</span></span>

5.  <span data-ttu-id="78588-147">Нажмите кнопку **Сжать** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="78588-147">Click **Compact** and then click **OK**.</span></span>

<span data-ttu-id="78588-148">Создайте резервную копию сжатого виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="78588-148">Create a backup copy of your compacted virtual hard disk.</span></span>

## <span data-ttu-id="78588-149">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="78588-149">Related topics</span></span>


[<span data-ttu-id="78588-150">Настройка образа Windows Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="78588-150">Configuring a Windows Virtual PC Image for MED-V</span></span>](configuring-a-windows-virtual-pc-image-for-med-v.md)

[<span data-ttu-id="78588-151">Технический справочник по MED-V</span><span class="sxs-lookup"><span data-stu-id="78588-151">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





