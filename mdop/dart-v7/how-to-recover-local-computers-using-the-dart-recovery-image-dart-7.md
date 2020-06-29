---
title: Восстановление локальных компьютеров с помощью образа для восстановления DaRT
description: Восстановление локальных компьютеров с помощью образа для восстановления DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823762"
---
# <span data-ttu-id="818a6-103">Восстановление локальных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="818a6-103">How to Recover Local Computers Using the DaRT Recovery Image</span></span>


<span data-ttu-id="818a6-104">Чтобы восстановить локальный компьютер с помощью набора средств диагностики и восстановления Microsoft (DaRT) 7, вы должны быть физически представлены на компьютере конечного пользователя, на котором возникают проблемы, требующие DaRT.</span><span class="sxs-lookup"><span data-stu-id="818a6-104">To recover a local computer by using Microsoft Diagnostics and Recovery Toolset (DaRT) 7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span> <span data-ttu-id="818a6-105">Вы также можете выполнить DaRT удаленно, следуя инструкциям, [чтобы восстановить удаленные компьютеры с помощью DaRT](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="818a6-105">You can also run DaRT remotely by following the instructions at [How to Recover Remote Computers Using the DaRT Recovery Image](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).</span></span>

**<span data-ttu-id="818a6-106">Восстановление локального компьютера с помощью DaRT</span><span class="sxs-lookup"><span data-stu-id="818a6-106">To recover a local computer by using DaRT</span></span>**

1.  <span data-ttu-id="818a6-107">При загрузке на изображение для восстановления DaRT на экране появится диалоговое окно " **NetStart** ".</span><span class="sxs-lookup"><span data-stu-id="818a6-107">As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.</span></span> <span data-ttu-id="818a6-108">Вам будет предложено указать, нужно ли инициализировать сетевые службы.</span><span class="sxs-lookup"><span data-stu-id="818a6-108">You are asked whether you want to initialize network services.</span></span> <span data-ttu-id="818a6-109">Если нажать кнопку **Да**, предполагается, что в сети есть DHCP-сервер и сделана попытка получить IP-адрес с сервера.</span><span class="sxs-lookup"><span data-stu-id="818a6-109">If you click **Yes**, it is assumed that a DHCP server is present on the network and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="818a6-110">Если в сети вместо DHCP используются статические IP-адреса, вы можете позже воспользоваться средством **настройки TCP/IP** в DART, чтобы указать статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="818a6-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="818a6-111">Чтобы пропустить процесс инициализации сети, нажмите кнопку **нет**.</span><span class="sxs-lookup"><span data-stu-id="818a6-111">To skip the network initialization process, click **No**.</span></span>

2.  <span data-ttu-id="818a6-112">В диалоговом окне "инициализация сети" появится вопрос о том, нужно ли переназначить буквы дисков.</span><span class="sxs-lookup"><span data-stu-id="818a6-112">Following the network initialization dialog box, you are asked whether you want to remap the drive letters.</span></span> <span data-ttu-id="818a6-113">При запуске Windows Online системный том обычно отображается на диске C. Однако при запуске Windows в автономном режиме в среде WinRE исходный системный том может быть сопоставлен с другим диском, и это может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="818a6-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="818a6-114">Если вы решили выполнить повторное сопоставление, DaRT попытается сопоставить буквы для автономного диска с буквами, заданными в сети.</span><span class="sxs-lookup"><span data-stu-id="818a6-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="818a6-115">Повторное сопоставление выполняется только в том случае, если в процессе запуска выбрана автономная операционная система.</span><span class="sxs-lookup"><span data-stu-id="818a6-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

3.  <span data-ttu-id="818a6-116">В диалоговом окне Изменение сопоставления в диалоговом окне **Параметры восстановления системы** появляется запрос на выбор раскладки клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="818a6-116">Following the remapping dialog box, a **System Recovery Options** dialog box appears and asks you to select a keyboard layout.</span></span> <span data-ttu-id="818a6-117">Затем отображается корневой каталог системы, вариант установленной операционной системы и размер раздела.</span><span class="sxs-lookup"><span data-stu-id="818a6-117">Then it displays the system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="818a6-118">Если вы не видите указанную в списке операционную систему и подозреваете, что причиной сбоя является нехватка драйверов, нажмите **загрузить драйверы** , чтобы загрузить подозрительные драйверы.</span><span class="sxs-lookup"><span data-stu-id="818a6-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers.</span></span> <span data-ttu-id="818a6-119">В этом случае вам будет предложено вставить установочный носитель для устройства и выбрать драйвер.</span><span class="sxs-lookup"><span data-stu-id="818a6-119">This prompts you to insert the installation media for the device and to select the driver.</span></span> <span data-ttu-id="818a6-120">Выберите установку, которую вы хотите восстановить или диагностировать, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="818a6-120">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="818a6-121">Примечание.</span><span class="sxs-lookup"><span data-stu-id="818a6-121">Note</span></span>**  
    <span data-ttu-id="818a6-122">Если среда восстановления Windows (WinRE) обнаруживает или подозреваете, что Windows 7 не запускается надлежащим образом в последний раз, программа **восстановления запуска** может начать выполняться автоматически.</span><span class="sxs-lookup"><span data-stu-id="818a6-122">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 7 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. <span data-ttu-id="818a6-123">В окне " **Параметры восстановления системы** " выберите **набор средств диагностики и восстановления Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="818a6-123">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="818a6-124">Откроется окно **инструментов Диагностика и восстановление** .</span><span class="sxs-lookup"><span data-stu-id="818a6-124">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="818a6-125">Теперь вы можете запускать любые инструменты или мастера, которые были включены при создании изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="818a6-125">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="818a6-126">Вы можете нажать кнопку **Справка** в окне " **набор инструментов диагностики и восстановления** ", чтобы открыть файл справки, который содержит подробные инструкции и сведения, необходимые для запуска отдельных инструментов DaRT.</span><span class="sxs-lookup"><span data-stu-id="818a6-126">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="818a6-127">Вы также можете нажать кнопку **Мастер решений** в окне **инструментов Диагностика и восстановление** , чтобы выбрать оптимальное средство для ситуации на основе короткого собеседования, предоставленного мастером.</span><span class="sxs-lookup"><span data-stu-id="818a6-127">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="818a6-128">Общие сведения о любом из инструментов DaRT можно найти в статье [Обзор инструментов dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md).</span><span class="sxs-lookup"><span data-stu-id="818a6-128">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 7.0](overview-of-the-tools-in-dart-70-new-ia.md).</span></span>

**<span data-ttu-id="818a6-129">Запуск DaRT в командной строке</span><span class="sxs-lookup"><span data-stu-id="818a6-129">To run DaRT at the command prompt</span></span>**

1. <span data-ttu-id="818a6-130">Вы можете запустить DaRT из командной строки, указав команду **netstart.exe** и используя любые из указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="818a6-130">You can run DaRT at the command prompt by specifying the **netstart.exe** command and by using any of the following parameters:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="818a6-131">Параметр</span><span class="sxs-lookup"><span data-stu-id="818a6-131">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="818a6-132">Описание</span><span class="sxs-lookup"><span data-stu-id="818a6-132">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="818a6-133">-Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="818a6-133">-network</span></span></p></td>
   <td align="left"><p><span data-ttu-id="818a6-134">Инициализирует сетевые службы.</span><span class="sxs-lookup"><span data-stu-id="818a6-134">Initializes the network services.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="818a6-135">-Повторное подключение</span><span class="sxs-lookup"><span data-stu-id="818a6-135">-remount</span></span></p></td>
   <td align="left"><p><span data-ttu-id="818a6-136">Повторное сопоставление букв дисков.</span><span class="sxs-lookup"><span data-stu-id="818a6-136">Remaps the drive letters.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="818a6-137">-Prompt</span><span class="sxs-lookup"><span data-stu-id="818a6-137">-prompt</span></span></p></td>
   <td align="left"><p><span data-ttu-id="818a6-138">Отображение сообщений с просьбой подтвердить, инициализировать ли сеть и переназначить диски.</span><span class="sxs-lookup"><span data-stu-id="818a6-138">Displays messages asking the end user to specify whether to initialize the network and remap the drives.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="818a6-139">Важно.</span><span class="sxs-lookup"><span data-stu-id="818a6-139">Important</span></span></strong><br/><p><span data-ttu-id="818a6-140">Ответ конечного пользователя на запросы переопределяет параметры-сетевой и-повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="818a6-140">The end user’s response to the prompts overrides the -network and -remount switches.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="818a6-141">Вы можете настроить DaRT так, чтобы на компьютере с функцией DaRT автоматически открывалось средство **удаленного подключения** , которое используется для подключения к службе поддержки.</span><span class="sxs-lookup"><span data-stu-id="818a6-141">You can customize DaRT so that a computer that boots into DaRT automatically opens the **Remote Connection** tool that is used to establish a remote connection with the help desk.</span></span>

## <span data-ttu-id="818a6-142">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="818a6-142">Related topics</span></span>


[<span data-ttu-id="818a6-143">Восстановление компьютеров с помощью DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="818a6-143">Recovering Computers Using DaRT 7.0</span></span>](recovering-computers-using-dart-70-dart-7.md)









