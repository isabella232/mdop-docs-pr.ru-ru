---
title: Восстановление удаленных компьютеров с помощью образа для восстановления DaRT
description: Восстановление удаленных компьютеров с помощью образа для восстановления DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822792"
---
# <span data-ttu-id="a570b-103">Восстановление удаленных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="a570b-103">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="a570b-104">Функция удаленного подключения в наборе средств диагностики и восстановления Microsoft (DaRT) 7 позволяет ИТ-администратору запускать инструменты DaRT удаленно на компьютере с конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="a570b-104">The Remote Connection feature in Microsoft Diagnostics and Recovery Toolset (DaRT) 7 lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="a570b-105">После того как конечные пользователи предоставляют определенную информацию (или специалист службы поддержки, работающий на компьютере пользователя), он может управлять компьютером конечного пользователя и запускать необходимые инструменты DaRT удаленно.</span><span class="sxs-lookup"><span data-stu-id="a570b-105">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

**<span data-ttu-id="a570b-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="a570b-106">Important</span></span>**  
<span data-ttu-id="a570b-107">Два компьютера, на которых установлено удаленное подключение, должны входить в одну и ту же сеть.</span><span class="sxs-lookup"><span data-stu-id="a570b-107">The two computers establishing a remote connection must be part of the same network.</span></span>



**<span data-ttu-id="a570b-108">Восстановление удаленного компьютера с помощью DaRT</span><span class="sxs-lookup"><span data-stu-id="a570b-108">To recover a remote computer by using DaRT</span></span>**

1.  <span data-ttu-id="a570b-109">Загрузите компьютер с конечным пользователем, используя изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="a570b-109">Boot an end-user computer by using the DaRT recovery image.</span></span>

    <span data-ttu-id="a570b-110">Вы обычно используете один из указанных ниже способов для загрузки DaRT для восстановления удаленного компьютера, в зависимости от того, как вы разворачиваете изображение для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="a570b-110">You will typically use one of the following methods to boot into DaRT to recover a remote computer, depending on how you deploy the DaRT recovery image.</span></span> <span data-ttu-id="a570b-111">Дополнительные сведения о развертывании изображения для восстановления DaRT можно найти [в разделе Развертывание образа восстановления dart 7,0](deploying-the-dart-70-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="a570b-111">For more information about deploying the DaRT recovery image, see [Deploying the DaRT 7.0 Recovery Image](deploying-the-dart-70-recovery-image-dart-7.md).</span></span>

    -   <span data-ttu-id="a570b-112">Загрузите элемент DaRT из раздела восстановления на компьютере с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a570b-112">Boot into DaRT from a recovery partition on the problem computer.</span></span>

    -   <span data-ttu-id="a570b-113">Загрузите элемент DaRT из удаленной секции в сети.</span><span class="sxs-lookup"><span data-stu-id="a570b-113">Boot into DaRT from a remote partition on the network.</span></span>

    <span data-ttu-id="a570b-114">Сведения о преимуществах и недостатках каждого из этих методов можно найти в разделе [Планирование сохранения и развертывания образа восстановления DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="a570b-114">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

    <span data-ttu-id="a570b-115">Какой бы метод вы использовали для загрузки в DaRT, необходимо включить загрузочное устройство в BIOS для варианта загрузки или параметров, которые должны быть доступны для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a570b-115">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

    **<span data-ttu-id="a570b-116">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a570b-116">Note</span></span>**  
    <span data-ttu-id="a570b-117">Настройка BIOS является уникальной в зависимости от типа жесткого диска, сетевых адаптеров и другого оборудования, которое используется в Организации.</span><span class="sxs-lookup"><span data-stu-id="a570b-117">Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>



2.  <span data-ttu-id="a570b-118">При загрузке на изображение для восстановления DaRT на экране появится диалоговое окно " **NetStart** ".</span><span class="sxs-lookup"><span data-stu-id="a570b-118">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="a570b-119">Вам будет предложено указать, нужно ли инициализировать сетевые службы.</span><span class="sxs-lookup"><span data-stu-id="a570b-119">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="a570b-120">Если нажать кнопку **Да**, предполагается, что в сети есть DHCP-сервер и сделана попытка получить IP-адрес с сервера.</span><span class="sxs-lookup"><span data-stu-id="a570b-120">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="a570b-121">Если в сети вместо DHCP используются статические IP-адреса, вы можете позже воспользоваться средством **настройки TCP/IP** в DART, чтобы указать статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a570b-121">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="a570b-122">Чтобы пропустить процесс инициализации сети, нажмите кнопку **нет**.</span><span class="sxs-lookup"><span data-stu-id="a570b-122">To skip the network initialization process, click **No**.</span></span>

3.  <span data-ttu-id="a570b-123">В диалоговом окне "инициализация сети" появится вопрос о том, нужно ли переназначить буквы дисков.</span><span class="sxs-lookup"><span data-stu-id="a570b-123">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="a570b-124">При запуске Windows Online системный том обычно отображается на диске C. Однако при запуске Windows в автономном режиме в среде WinRE исходный системный том может быть сопоставлен с другим диском, и это может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="a570b-124">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="a570b-125">Если вы решили выполнить повторное сопоставление, DaRT попытается сопоставить буквы для автономного диска с буквами, заданными в сети.</span><span class="sxs-lookup"><span data-stu-id="a570b-125">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="a570b-126">Повторное сопоставление выполняется только в том случае, если в процессе запуска выбрана автономная операционная система.</span><span class="sxs-lookup"><span data-stu-id="a570b-126">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="a570b-127">В диалоговом окне Изменение сопоставления в диалоговом окне **Параметры восстановления системы** появляется запрос на выбор раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a570b-127">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="a570b-128">Затем отображается корневой каталог системы, вариант установленной операционной системы и размер раздела.</span><span class="sxs-lookup"><span data-stu-id="a570b-128">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="a570b-129">Если вы не видите указанную в списке операционную систему и подозреваете, что причиной сбоя является нехватка драйверов, нажмите **загрузить драйверы** , чтобы загрузить подозрительные драйверы.</span><span class="sxs-lookup"><span data-stu-id="a570b-129">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="a570b-130">В этом случае вам будет предложено вставить установочный носитель для устройства и выбрать драйвер.</span><span class="sxs-lookup"><span data-stu-id="a570b-130">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="a570b-131">Выберите установку, которую вы хотите восстановить или диагностировать, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a570b-131">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="a570b-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a570b-132">Note</span></span>**  
    <span data-ttu-id="a570b-133">Если среда восстановления Windows (WinRE) обнаруживает или подозреваете, что Windows 7 не запускается надлежащим образом в последний раз, программа **восстановления запуска** может начать выполняться автоматически.</span><span class="sxs-lookup"><span data-stu-id="a570b-133">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span> <span data-ttu-id="a570b-134">Сведения об этой ситуации, в том числе о том, как ее устранить, приведены в разделе [Устранение неполадок DaRT 7,0](troubleshooting-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="a570b-134">For information about this situation including how to resolve it, see [Troubleshooting DaRT 7.0](troubleshooting-dart-70-new-ia.md).</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. <span data-ttu-id="a570b-135">В окне **Параметры восстановления системы** выберите **набор средств диагностики и восстановления Microsoft** , чтобы открыть окно **инструментов Диагностика и восстановление** .</span><span class="sxs-lookup"><span data-stu-id="a570b-135">On the **System Recovery Options** window, select **Microsoft Diagnostics and Recovery Toolset** to open the **Diagnostics and Recovery Toolset** window.</span></span>

6. <span data-ttu-id="a570b-136">В окне **Инструменты Диагностика и восстановление** щелкните **удаленное подключение** , чтобы открыть окно **удаленного подключения DART** .</span><span class="sxs-lookup"><span data-stu-id="a570b-136">On the **Diagnostics and Recovery Toolset** window, click **Remote Connection** to open the **DaRT Remote Connection** window.</span></span> <span data-ttu-id="a570b-137">Если вам будет предложено предоставить службе поддержки удаленный доступ, нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a570b-137">If you are prompted to give the help desk remote access, click **OK**.</span></span>

   <span data-ttu-id="a570b-138">Откроется окно с удаленным подключением DaRT, в котором отображается номер билета, IP-адрес и сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="a570b-138">The DaRT Remote Connection window opens and displays a ticket number, IP address, and port information.</span></span>

7. <span data-ttu-id="a570b-139">На компьютере агента службы поддержки откройте **средство просмотра удаленных подключений DART**.</span><span class="sxs-lookup"><span data-stu-id="a570b-139">On the helpdesk agent computer, open the **DaRT Remote Connection Viewer**.</span></span>

   <span data-ttu-id="a570b-140">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft DaRT 7**, а затем — **средство просмотра удаленных подключений для DART**.</span><span class="sxs-lookup"><span data-stu-id="a570b-140">Click **Start**, click **All Programs**, click **Microsoft DaRT 7**, and then click **DaRT Remote Connection Viewer**.</span></span>

8. <span data-ttu-id="a570b-141">В окне **удаленного подключения DART** введите необходимый билет, IP-адрес и сведения о порте.</span><span class="sxs-lookup"><span data-stu-id="a570b-141">In the **DaRT Remote Connection** window, enter the required ticket, IP address, and port information.</span></span>

   **<span data-ttu-id="a570b-142">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a570b-142">Note</span></span>**  
   <span data-ttu-id="a570b-143">Эти сведения создаются на компьютере пользователя и должны быть предоставлены конечным пользователем.</span><span class="sxs-lookup"><span data-stu-id="a570b-143">This information is created on the end-user computer and must be provided by the end user.</span></span> <span data-ttu-id="a570b-144">Возможно, вы можете выбрать несколько IP-адресов, в зависимости от того, сколько доступно на компьютере конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a570b-144">There might be multiple IP addresses to choose from, depending on how many are available on the end-user computer.</span></span>



9. <span data-ttu-id="a570b-145">Нажмите кнопку **Подключить**.</span><span class="sxs-lookup"><span data-stu-id="a570b-145">Click **Connect**.</span></span>

<span data-ttu-id="a570b-146">Теперь ИТ-администратор может управлять компьютером конечного пользователя и удаленно запускать инструменты DaRT.</span><span class="sxs-lookup"><span data-stu-id="a570b-146">The IT administrator now assumes control of the end-user computer and can run the DaRT tools remotely.</span></span>

**<span data-ttu-id="a570b-147">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a570b-147">Note</span></span>**  
<span data-ttu-id="a570b-148">Файл с именем inv32.xml и содержит сведения об удаленном подключении, такие как номер порта и IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="a570b-148">A file is provided that is named inv32.xml and contains remote connection information, such as the port number and IP address.</span></span> <span data-ttu-id="a570b-149">По умолчанию файл обычно размещается по адресу%windir%\\system32.</span><span class="sxs-lookup"><span data-stu-id="a570b-149">By default, the file is typically located at %windir%\\system32.</span></span>



**<span data-ttu-id="a570b-150">Настройка процесса удаленного подключения</span><span class="sxs-lookup"><span data-stu-id="a570b-150">To customize the Remote Connection process</span></span>**

1. <span data-ttu-id="a570b-151">Вы можете настроить процесс удаленного подключения, изменив файл winpeshl.ini.</span><span class="sxs-lookup"><span data-stu-id="a570b-151">You can customize the Remote Connection process by editing the winpeshl.ini file.</span></span> <span data-ttu-id="a570b-152">Дополнительные сведения о том, как изменить winpeshl.ini файл, можно найти в разделе [Winpeshl.ini файлы](https://go.microsoft.com/fwlink/?LinkId=219413).</span><span class="sxs-lookup"><span data-stu-id="a570b-152">For more information about how to edit the winpeshl.ini file, see [Winpeshl.ini Files](https://go.microsoft.com/fwlink/?LinkId=219413).</span></span>

   <span data-ttu-id="a570b-153">Укажите указанные ниже команды и параметры, чтобы настроить способ установки удаленного подключения для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="a570b-153">Specify the following commands and parameters to customize how a remote connection is established with an end-user computer:</span></span>

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="a570b-154">Команда</span><span class="sxs-lookup"><span data-stu-id="a570b-154">Command</span></span></th>
   <th align="left"><span data-ttu-id="a570b-155">Параметр</span><span class="sxs-lookup"><span data-stu-id="a570b-155">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="a570b-156">Описание</span><span class="sxs-lookup"><span data-stu-id="a570b-156">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="a570b-157">RemoteRecovery.exe</span><span class="sxs-lookup"><span data-stu-id="a570b-157">RemoteRecovery.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a570b-158">-е сообщение</span><span class="sxs-lookup"><span data-stu-id="a570b-158">-nomessage</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a570b-159">Указывает, что запрос подтверждения не отображается.</span><span class="sxs-lookup"><span data-stu-id="a570b-159">Specifies that the confirmation prompt is not displayed.</span></span> <strong><span data-ttu-id="a570b-160">Удаленное соединение </strong> продолжится так, как будто конечный пользователь &quot; ответил &quot; на запрос подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a570b-160">Remote Connection</strong> continues just as if the end user had responded &quot;Yes&quot; to the confirmation prompt.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="a570b-161">WaitForConnection.exe</span><span class="sxs-lookup"><span data-stu-id="a570b-161">WaitForConnection.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="a570b-162">нет</span><span class="sxs-lookup"><span data-stu-id="a570b-162">none</span></span></p></td>
   <td align="left"><p><span data-ttu-id="a570b-163">Предотвращает продолжение настраиваемого сценария, пока <strong> </strong> не будет запущено удаленное подключение или не будет установлено действующее соединение с конечным компьютером пользователя.</span><span class="sxs-lookup"><span data-stu-id="a570b-163">Prevents a custom script from continuing until either <strong>Remote Connection</strong> is not running or a valid connection is established with the end-user computer.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="a570b-164">Важно.</span><span class="sxs-lookup"><span data-stu-id="a570b-164">Important</span></span></strong><br/><p><span data-ttu-id="a570b-165">Эта команда не выполняет никаких функций, если она указана независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="a570b-165">This command serves no function if it is specified independently.</span></span> <span data-ttu-id="a570b-166">Он должен быть указан в сценарии для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="a570b-166">It must be specified in a script to function correctly.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="a570b-167">Ниже приведен пример файла winpeshl.ini, который настроен таким образом, чтобы открыть средство **удаленного подключения** , как только вы попытаетесь загрузить DART:</span><span class="sxs-lookup"><span data-stu-id="a570b-167">The following is an example of a winpeshl.ini file that is customized to open the **Remote Connection** tool as soon as an attempt is made to boot into DaRT:</span></span>

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**<span data-ttu-id="a570b-168">Запуск средства просмотра удаленных подключений из командной строки</span><span class="sxs-lookup"><span data-stu-id="a570b-168">To run the Remote Connection Viewer at the command prompt</span></span>**

1.  <span data-ttu-id="a570b-169">Вы можете запустить **средство просмотра удаленных подключений DART** в командной строке, указав команду **DartRemoteViewer.exe** и используя указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="a570b-169">You can run the **DaRT Remote Connection Viewer** at the command prompt by specifying the **DartRemoteViewer.exe** command and by using the following parameters:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a570b-170">Параметр</span><span class="sxs-lookup"><span data-stu-id="a570b-170">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="a570b-171">Описание</span><span class="sxs-lookup"><span data-stu-id="a570b-171">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a570b-172">-билета = &lt; <em> ticketnumber</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a570b-172">-ticket=&lt;<em>ticketnumber</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a570b-173">Где &lt; <em> ticketnumber </em> &gt; — номер билета, включая тире, которое генерируется удаленным соединением.</span><span class="sxs-lookup"><span data-stu-id="a570b-173">Where &lt;<em>ticketnumber</em>&gt; is the ticket number, including the dashes, that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a570b-174">-IPAddress = &lt; <em> IPAddress</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a570b-174">-ipaddress=&lt;<em>ipaddress</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a570b-175">&lt; <em> </em> &gt; IP-адрес, который генерируется удаленным подключением, где IPAddress.</span><span class="sxs-lookup"><span data-stu-id="a570b-175">Where &lt;<em>ipaddress</em>&gt; is the IP address that is generated by Remote Connection.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a570b-176">-Port = &lt; <em> Port (порт)</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="a570b-176">-port=&lt;<em>port</em>&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a570b-177">Если &lt; <em> Port (порт) </em> &gt; — порт, соответствующий указанному IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="a570b-177">Where &lt;<em>port</em>&gt; is the port that corresponds to the specified IP address.</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. <span data-ttu-id="a570b-178">Если указаны все три параметра и данные являются допустимыми, при запуске программы немедленно исключается соединение.</span><span class="sxs-lookup"><span data-stu-id="a570b-178">If all three parameters are specified and the data is valid, a connection is immediately tried when the program starts.</span></span> <span data-ttu-id="a570b-179">Если какой – либо параметр является недопустимым, программа запускается так, как если бы не были указаны параметры.</span><span class="sxs-lookup"><span data-stu-id="a570b-179">If any parameter is not valid, the program starts as if there were no parameters specified.</span></span>

## <span data-ttu-id="a570b-180">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a570b-180">Related topics</span></span>


[<span data-ttu-id="a570b-181">Восстановление компьютеров с помощью DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="a570b-181">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









