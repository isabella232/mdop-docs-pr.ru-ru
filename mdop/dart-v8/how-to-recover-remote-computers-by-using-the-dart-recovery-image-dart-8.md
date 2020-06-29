---
title: Восстановление удаленных компьютеров с помощью образа для восстановления DaRT
description: Восстановление удаленных компьютеров с помощью образа для восстановления DaRT
author: dansimp
ms.assetid: 363ccd48-6820-4b5b-a43a-323c0b208a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b3e3155dbea8da18338b8a167d22f73b1c8e4bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824399"
---
# <span data-ttu-id="898c7-103">Восстановление удаленных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="898c7-103">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="898c7-104">С помощью функции удаленного подключения в наборе средств диагностики и восстановления Microsoft (DaRT) 8,0 можно запускать инструменты DaRT удаленно на компьютере с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="898c7-104">Use the Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 to run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="898c7-105">После того как пользователь предложит администратору или сотруднику службы поддержки определенную информацию, он может управлять компьютером конечного пользователя и выполнять необходимые инструменты DaRT удаленно.</span><span class="sxs-lookup"><span data-stu-id="898c7-105">After the end user provides the administrator or help desk worker with certain information, the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="898c7-106">Если вы отключили инструменты DaRT при создании образа восстановления, вы по-прежнему можете получить доступ ко всем средствам.</span><span class="sxs-lookup"><span data-stu-id="898c7-106">If you disabled the DaRT tools when you created the recovery image, you still have access to all of the tools.</span></span> <span data-ttu-id="898c7-107">Все инструменты, кроме удаленных подключений, недоступны для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="898c7-107">All of the tools, except Remote Connection, are unavailable to end users.</span></span>

**<span data-ttu-id="898c7-108">Восстановление удаленного компьютера с помощью изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="898c7-108">To recover a remote computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="898c7-109">Загрузите компьютер с конечным пользователем, используя изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="898c7-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="898c7-110">Вы обычно используете один из указанных ниже способов для загрузки DaRT для восстановления удаленного компьютера, в зависимости от того, как вы разворачиваете изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="898c7-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="898c7-111">Дополнительные сведения о развертывании изображения для восстановления DaRT можно найти в разделе [развертывание dart 8,0](deploying-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="898c7-111">For more information about deploying the DaRT recovery image, see [Deploying DaRT 8.0](deploying-dart-80-dart-8.md).</span></span>

    -   <span data-ttu-id="898c7-112">Загрузите элемент DaRT из раздела восстановления на компьютере с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="898c7-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="898c7-113">Загрузите элемент DaRT из удаленной секции в сети.</span><span class="sxs-lookup"><span data-stu-id="898c7-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="898c7-114">Сведения о преимуществах и недостатках каждого из этих методов можно найти в разделе [Планирование сохранения и развертывания образа восстановления DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="898c7-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

    <span data-ttu-id="898c7-115">Какой бы метод вы использовали для загрузки в DaRT, необходимо включить загрузочное устройство в BIOS для варианта загрузки или параметров, которые должны быть доступны для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="898c7-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="898c7-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="898c7-116">Note</span></span>**  
    <span data-ttu-id="898c7-117">Настройка BIOS является уникальной в зависимости от типа жесткого диска, сетевых адаптеров и другого оборудования, которое используется в Организации.</span><span class="sxs-lookup"><span data-stu-id="898c7-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. <span data-ttu-id="898c7-118">Когда появится вопрос о том, нужно ли инициализировать сетевые службы, выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="898c7-118">When you are asked whether you want to initialize network services, select one of the following:</span></span>

   <span data-ttu-id="898c7-119">**Да** , предполагается, что в сети есть DHCP-сервер, и делается попытка получить IP-адрес с сервера.</span><span class="sxs-lookup"><span data-stu-id="898c7-119">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="898c7-120">Если в сети вместо DHCP используются статические IP-адреса, вы можете позже воспользоваться средством **настройки TCP/IP** в DART, чтобы указать статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="898c7-120">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

   <span data-ttu-id="898c7-121">**Нет** -пропускать процесс инициализации сети.</span><span class="sxs-lookup"><span data-stu-id="898c7-121">**No** - skip the network initialization process.</span></span>

3. <span data-ttu-id="898c7-122">Укажите, нужно ли переназначить буквы дисков.</span><span class="sxs-lookup"><span data-stu-id="898c7-122">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="898c7-123">При запуске Windows Online системный том обычно отображается на диске C. Однако при запуске Windows в автономном режиме в среде WinRE исходный системный том может быть сопоставлен с другим диском, и это может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="898c7-123">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="898c7-124">Если вы решили выполнить повторное сопоставление, DaRT попытается сопоставить буквы для автономного диска с буквами, заданными в сети.</span><span class="sxs-lookup"><span data-stu-id="898c7-124">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="898c7-125">Повторное сопоставление выполняется только в том случае, если в процессе запуска выбрана автономная операционная система.</span><span class="sxs-lookup"><span data-stu-id="898c7-125">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4. <span data-ttu-id="898c7-126">В диалоговом окне " **Параметры восстановления системы** " выберите раскладку клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="898c7-126">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5. <span data-ttu-id="898c7-127">Проверьте отображаемый корневой каталог системы, версию операционной системы и размер раздела.</span><span class="sxs-lookup"><span data-stu-id="898c7-127">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="898c7-128">Если вы не видите указанную в списке операционную систему и подозреваете, что причиной сбоя является отсутствующий драйвер, нажмите **загрузить драйверы** для загрузки подозрительных драйверов, а затем вставьте установочный носитель для устройства и выберите драйвер.</span><span class="sxs-lookup"><span data-stu-id="898c7-128">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6. <span data-ttu-id="898c7-129">Выберите установку, которую вы хотите восстановить или диагностировать, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="898c7-129">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

   **<span data-ttu-id="898c7-130">Примечание.</span><span class="sxs-lookup"><span data-stu-id="898c7-130">Note</span></span>**  
   <span data-ttu-id="898c7-131">Если среда восстановления Windows (WinRE) обнаруживает или подозреваете, что система Windows 8 не запустилась надлежащим образом, программа **восстановления запуска** может запуститься автоматически.</span><span class="sxs-lookup"><span data-stu-id="898c7-131">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 8 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="898c7-132">Сведения о том, как устранить эту проблему, можно найти в разделе [Устранение неполадок DaRT 8,0](troubleshooting-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="898c7-132">For information about how to resolve this issue, see [Troubleshooting DaRT 8.0](troubleshooting-dart-80-dart-8.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="898c7-133">В окне **Параметры восстановления системы** выберите набор **средств диагностики и восстановления Microsoft** , чтобы открыть **набор средств диагностики и восстановления**.</span><span class="sxs-lookup"><span data-stu-id="898c7-133">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset**.</span></span>

8. <span data-ttu-id="898c7-134">В окне **Инструменты Диагностика и восстановление** щелкните **удаленное подключение** , чтобы открыть окно **удаленного подключения DART** .</span><span class="sxs-lookup"><span data-stu-id="898c7-134">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="898c7-135">Если вам будет предложено предоставить службе поддержки удаленный доступ, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="898c7-135">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="898c7-136">Откроется окно с удаленным подключением DaRT, в котором отображается номер билета, IP-адрес и сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="898c7-136">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

9. <span data-ttu-id="898c7-137">На компьютере службы поддержки откройте **средство просмотра удаленных подключений DART**.</span><span class="sxs-lookup"><span data-stu-id="898c7-137">On the help desk computer, open the **DaRT Remote Connection Viewer**.</span></span>

10. <span data-ttu-id="898c7-138">Нажмите кнопку **Пуск**, выберите **все программы**, нажмите **Microsoft DART 8,0**, а затем — **средство просмотра удаленных подключений для DART**.</span><span class="sxs-lookup"><span data-stu-id="898c7-138">Click **Start**, click **All Programs**, click **Microsoft DaRT 8.0**, and then click **DaRT Remote Connection Viewer**.</span></span>

11. <span data-ttu-id="898c7-139">В окне **удаленного подключения DART** введите необходимый билет, IP-адрес и сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="898c7-139">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="898c7-140">Примечание.</span><span class="sxs-lookup"><span data-stu-id="898c7-140">Note</span></span>**  
   <span data-ttu-id="898c7-141">Эти сведения создаются на компьютере пользователя и должны быть предоставлены конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="898c7-141">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="898c7-142">Возможно, вы можете выбрать несколько IP-адресов, в зависимости от того, сколько доступно на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="898c7-142">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



12. <span data-ttu-id="898c7-143">Нажмите кнопку **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="898c7-143">Click **Connect**.</span></span>

<span data-ttu-id="898c7-144">Теперь ИТ-администратор может управлять компьютером конечного пользователя и удаленно запускать инструменты DaRT.</span><span class="sxs-lookup"><span data-stu-id="898c7-144">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="898c7-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="898c7-145">Note</span></span>**  
<span data-ttu-id="898c7-146">Файл с именем inv32.xml и содержит сведения об удаленном подключении, такие как номер порта и IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="898c7-146">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="898c7-147">По умолчанию файл обычно размещается по адресу%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="898c7-147">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="898c7-148">Настройка процесса удаленного подключения</span><span class="sxs-lookup"><span data-stu-id="898c7-148">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="898c7-149">Вы можете настроить процесс удаленного подключения, изменив файл winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="898c7-149">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="898c7-150">Дополнительные сведения о том, как изменить winpeshl.ini файл, можно найти в разделе [Winpeshl.ini файлы](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="898c7-150">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="898c7-151">Укажите указанные ниже команды и параметры, чтобы настроить способ установки удаленного подключения для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="898c7-151">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="898c7-152">Команда</span><span class="sxs-lookup"><span data-stu-id="898c7-152">Command</span></span></th>
   <th align="left"><span data-ttu-id="898c7-153">Параметр</span><span class="sxs-lookup"><span data-stu-id="898c7-153">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="898c7-154">Описание</span><span class="sxs-lookup"><span data-stu-id="898c7-154">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="898c7-155">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="898c7-155">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="898c7-156">-е сообщение</span><span class="sxs-lookup"><span data-stu-id="898c7-156">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="898c7-157">Указывает, что запрос подтверждения не отображается.</span><span class="sxs-lookup"><span data-stu-id="898c7-157">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="898c7-158">Удаленное соединение </strong> продолжится так, как будто конечный пользователь &quot; ответил &quot; на запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="898c7-158">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="898c7-159">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="898c7-159">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="898c7-160">нет</span><span class="sxs-lookup"><span data-stu-id="898c7-160">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="898c7-161">Предотвращает продолжение настраиваемого сценария, пока <strong> </strong> не будет запущено удаленное подключение или не будет установлено действующее соединение с конечным компьютером пользователя.</span><span class="sxs-lookup"><span data-stu-id="898c7-161">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="898c7-162">Важно.</span><span class="sxs-lookup"><span data-stu-id="898c7-162">Important</span></span></strong><br/><p><span data-ttu-id="898c7-163">Эта команда не выполняет никаких функций, если она указана независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="898c7-163">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="898c7-164">Он должен быть указан в сценарии для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="898c7-164">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="898c7-165">Ниже приведен пример файла winpeshl.ini, который настроен таким образом, чтобы открыть средство **удаленного подключения** , как только вы попытаетесь загрузить DART:</span><span class="sxs-lookup"><span data-stu-id="898c7-165">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

<span data-ttu-id="898c7-166">При запуске DaRT создается файл inv32.xml в \\Windows\\System32\\ на ЭЛЕКТРОНном диске.</span><span class="sxs-lookup"><span data-stu-id="898c7-166">When DaRT starts, it creates the file inv32.xml in \\Windows\\System32\\ on the RAM disk.</span></span> <span data-ttu-id="898c7-167">Этот файл имеет сведения о подключении: IP-адрес, порт и номер билета.</span><span class="sxs-lookup"><span data-stu-id="898c7-167">This file contains connection information: IP address, port, and ticket number.</span></span> <span data-ttu-id="898c7-168">Вы можете скопировать этот файл в общую сетевую информацию, чтобы активировать рабочий процесс службы поддержки.</span><span class="sxs-lookup"><span data-stu-id="898c7-168">You can copy this file to a network share to trigger a Help desk workflow.</span></span> <span data-ttu-id="898c7-169">Например, настраиваемая программа может проверить сетевую почту для файлов подключения, а затем создать билет поддержки или отправить уведомления по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="898c7-169">For example, a custom program can check the network share for connection files, and then create a support ticket or send email notifications.</span></span>

**<span data-ttu-id="898c7-170">Запуск средства просмотра удаленных подключений из командной строки</span><span class="sxs-lookup"><span data-stu-id="898c7-170">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="898c7-171">Чтобы запустить **средство просмотра удаленной связи** с помощью DaRT в командной строке, укажите команду **DartRemoteViewer.exe** и используйте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="898c7-171">To run the **DaRT Remote Connection Viewer** at the command prompt, specify the **DartRemoteViewer.exe** command and use the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="898c7-172">Параметр</span><span class="sxs-lookup"><span data-stu-id="898c7-172">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="898c7-173">Описание</span><span class="sxs-lookup"><span data-stu-id="898c7-173">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="898c7-174">-билета = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="898c7-174">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="898c7-175">Где &lt; <em> ticketnumber </em> &gt; — номер билета, включая тире, которое генерируется удаленным соединением.</span><span class="sxs-lookup"><span data-stu-id="898c7-175">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="898c7-176">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="898c7-176">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="898c7-177">&lt; <em> </em> &gt; IP-адрес, который генерируется удаленным подключением, где IPAddress.</span><span class="sxs-lookup"><span data-stu-id="898c7-177">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="898c7-178">-Port = &lt; <em> Port (порт)</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="898c7-178">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="898c7-179">Если &lt; <em> Port (порт) </em> &gt; — порт, соответствующий указанному IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="898c7-179">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="898c7-180">Если указаны все три параметра и данные являются допустимыми, при запуске программы немедленно исключается соединение.</span><span class="sxs-lookup"><span data-stu-id="898c7-180">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="898c7-181">Если какой – либо параметр является недопустимым, программа запускается так, как если бы не были указаны параметры.</span><span class="sxs-lookup"><span data-stu-id="898c7-181">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="898c7-182">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="898c7-182">Related topics</span></span>


[<span data-ttu-id="898c7-183">Операции DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="898c7-183">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

[<span data-ttu-id="898c7-184">Восстановление компьютеров с помощью DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="898c7-184">Recovering Computers Using DaRT 8.0</span></span>](recovering-computers-using-dart-80-dart-8.md)









