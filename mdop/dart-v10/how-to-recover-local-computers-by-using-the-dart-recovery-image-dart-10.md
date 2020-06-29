---
title: Восстановление локальных компьютеров с помощью образа для восстановления DaRT
description: Восстановление локальных компьютеров с помощью образа для восстановления DaRT
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822589"
---
# <span data-ttu-id="0a9a6-103">Восстановление локальных компьютеров с помощью образа для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="0a9a6-103">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="0a9a6-104">Воспользуйтесь этими инструкциями, чтобы восстановить компьютер, если вы физически подключены к компьютеру конечного пользователя, на котором возникли проблемы.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-104">Use these instructions to recover a computer when you are physically present at the end-user computer that is experiencing problems.</span></span>

**<span data-ttu-id="0a9a6-105">Восстановление локального компьютера с помощью изображения для восстановления DaRT</span><span class="sxs-lookup"><span data-stu-id="0a9a6-105">How to recover a local computer by using the DaRT recovery image</span></span>**

1.  <span data-ttu-id="0a9a6-106">Загрузите компьютер конечного пользователя с помощью образа восстановления для средства диагностики и восстановления Microsoft (DaRT) 10.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-106">Boot the end-user computer by using the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image.</span></span>

    <span data-ttu-id="0a9a6-107">При загрузке компьютера с помощью изображения DaRT 10 на экране появится диалоговое окно " **NetStart** ".</span><span class="sxs-lookup"><span data-stu-id="0a9a6-107">As the computer is booting into the DaRT 10 recovery image, the **NetStart** dialog box appears.</span></span>

2.  <span data-ttu-id="0a9a6-108">Когда появится вопрос о том, нужно ли инициализировать сетевые службы, выберите один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-108">When you are asked whether you want to initialize network services, select one of the following:</span></span>

    <span data-ttu-id="0a9a6-109">**Да** , предполагается, что в сети есть DHCP-сервер, и делается попытка получить IP-адрес с сервера.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-109">**Yes** - it is assumed that a DHCP server is present on the network, and an attempt is made to obtain an IP address from the server.</span></span> <span data-ttu-id="0a9a6-110">Если в сети вместо DHCP используются статические IP-адреса, вы можете позже воспользоваться средством **настройки TCP/IP** в DART, чтобы указать статический IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-110">If the network uses static IP addresses instead of DHCP, you can later use the **TCP/IP Configuration** tool in DaRT to specify a static IP address.</span></span>

    <span data-ttu-id="0a9a6-111">**Нет** -пропускать процесс инициализации сети.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-111">**No** - skip the network initialization process.</span></span>

3.  <span data-ttu-id="0a9a6-112">Укажите, нужно ли переназначить буквы дисков.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-112">Indicate whether you want to remap the drive letters.</span></span> <span data-ttu-id="0a9a6-113">При запуске Windows Online системный том обычно отображается на диске C. Однако при запуске Windows в автономном режиме в среде WinRE исходный системный том может быть сопоставлен с другим диском, и это может привести к путанице.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-113">When you run Windows online, the system volume is typically mapped to drive C. However, when you run Windows offline under WinRE, the original system volume might be mapped to another drive, and this can cause confusion.</span></span> <span data-ttu-id="0a9a6-114">Если вы решили выполнить повторное сопоставление, DaRT попытается сопоставить буквы для автономного диска с буквами, заданными в сети.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-114">If you decide to remap, DaRT tries to map the offline drive letters to match the online drive letters.</span></span> <span data-ttu-id="0a9a6-115">Повторное сопоставление выполняется только в том случае, если в процессе запуска выбрана автономная операционная система.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-115">Remapping is performed only if an offline operating system is selected later in the startup process.</span></span>

4.  <span data-ttu-id="0a9a6-116">В диалоговом окне " **Параметры восстановления системы** " выберите раскладку клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-116">On the **System Recovery Options** dialog box, select a keyboard layout.</span></span>

5.  <span data-ttu-id="0a9a6-117">Проверьте отображаемый корневой каталог системы, версию операционной системы и размер раздела.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-117">Check the displayed system root directory, the kind of operating system installed, and the partition size.</span></span> <span data-ttu-id="0a9a6-118">Если вы не видите указанную в списке операционную систему и подозреваете, что причиной сбоя является отсутствующий драйвер, нажмите **загрузить драйверы** для загрузки подозрительных драйверов, а затем вставьте установочный носитель для устройства и выберите драйвер.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-118">If you do not see your operating system listed, and suspect that the lack of drivers is a possible cause of the failure, click **Load Drivers** to load the suspect drivers, and then insert the installation media for the device and select the driver.</span></span>

6.  <span data-ttu-id="0a9a6-119">Выберите установку, которую вы хотите восстановить или диагностировать, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-119">Select the installation that you want to repair or diagnose, and then click **Next**.</span></span>

    **<span data-ttu-id="0a9a6-120">Примечание.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-120">Note</span></span>**  
    <span data-ttu-id="0a9a6-121">Если среда восстановления Windows (WinRE) обнаруживает или подозреваете, что Windows 10 не запускается надлежащим образом в прошлый раз, программа **восстановления запуска** может начать выполняться автоматически.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-121">If the Windows Recovery Environment (WinRE) detects or suspects that Windows 10 did not start correctly the last time that it was tried, **Startup Repair** might start to run automatically.</span></span>



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. <span data-ttu-id="0a9a6-122">В окне " **Параметры восстановления системы** " выберите **набор средств диагностики и восстановления Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-122">On the **System Recovery Options** window, click **Microsoft Diagnostics and Recovery Toolset**.</span></span>

   <span data-ttu-id="0a9a6-123">Откроется окно **инструментов Диагностика и восстановление** .</span><span class="sxs-lookup"><span data-stu-id="0a9a6-123">The **Diagnostics and Recovery Toolset** window opens.</span></span> <span data-ttu-id="0a9a6-124">Теперь вы можете запускать любые инструменты или мастера, которые были включены при создании изображения для восстановления DaRT.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-124">You can now run any of the individual tools or wizards that were included when the DaRT recovery image was created.</span></span>

<span data-ttu-id="0a9a6-125">Вы можете нажать кнопку **Справка** в окне " **набор инструментов диагностики и восстановления** ", чтобы открыть файл справки, который содержит подробные инструкции и сведения, необходимые для запуска отдельных инструментов DaRT.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-125">You can click **Help** on the **Diagnostics and Recovery Toolset** window to open the client Help file that provides detailed instruction and information needed to run the individual DaRT tools.</span></span> <span data-ttu-id="0a9a6-126">Вы также можете нажать кнопку **Мастер решений** в окне **инструментов Диагностика и восстановление** , чтобы выбрать оптимальное средство для ситуации на основе короткого собеседования, предоставленного мастером.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-126">You can also click the **Solution Wizard** on the **Diagnostics and Recovery Toolset** window to choose the best tool for the situation, based on a brief interview that the wizard provides.</span></span>

<span data-ttu-id="0a9a6-127">Общие сведения о любом из инструментов DaRT можно найти в статье [Обзор средств на DART 10](overview-of-the-tools-in-dart-10.md).</span><span class="sxs-lookup"><span data-stu-id="0a9a6-127">For general information about any of the DaRT tools, see [Overview of the Tools in DaRT 10](overview-of-the-tools-in-dart-10.md).</span></span>

**<span data-ttu-id="0a9a6-128">Запуск DaRT из командной строки</span><span class="sxs-lookup"><span data-stu-id="0a9a6-128">How to run DaRT at the command prompt</span></span>**

- <span data-ttu-id="0a9a6-129">Чтобы запустить DaRT в командной строке, укажите команду **netstart.exe** , а затем используйте любые из указанных ниже параметров.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-129">To run DaRT at the command prompt, specify the **netstart.exe** command then use any of the following parameters:</span></span>

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong><span data-ttu-id="0a9a6-130">Параметр</span><span class="sxs-lookup"><span data-stu-id="0a9a6-130">Parameter</span></span></strong></p></td>
  <td align="left"><p><strong><span data-ttu-id="0a9a6-131">Описание</span><span class="sxs-lookup"><span data-stu-id="0a9a6-131">Description</span></span></strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="0a9a6-132">-Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="0a9a6-132">-network</span></span></p></td>
  <td align="left"><p><span data-ttu-id="0a9a6-133">Инициализирует сетевые службы.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-133">Initializes the network services.</span></span></p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p><span data-ttu-id="0a9a6-134">-Повторное подключение</span><span class="sxs-lookup"><span data-stu-id="0a9a6-134">-remount</span></span></p></td>
  <td align="left"><p><span data-ttu-id="0a9a6-135">Повторное сопоставление букв дисков.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-135">Remaps the drive letters.</span></span></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p><span data-ttu-id="0a9a6-136">-Prompt</span><span class="sxs-lookup"><span data-stu-id="0a9a6-136">-prompt</span></span></p></td>
  <td align="left"><p><span data-ttu-id="0a9a6-137">Выводит сообщения, в которых пользователь должен указать, следует ли инициализировать сеть и переназначить диски.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-137">Displays messages that ask the end user to specify whether to initialize the network and remap the drives.</span></span></p>
  <div class="alert">
  <strong><span data-ttu-id="0a9a6-138">Warning</span><span class="sxs-lookup"><span data-stu-id="0a9a6-138">Warning</span></span></strong><br/><p><span data-ttu-id="0a9a6-139">Ответ конечного пользователя на запрос переопределяет переключатели – сеть и – повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="0a9a6-139">The end user’s response to the prompt overrides the –network and –remount switches.</span></span></p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## <span data-ttu-id="0a9a6-140">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="0a9a6-140">Related topics</span></span>


[<span data-ttu-id="0a9a6-141">Операции DaRT 10</span><span class="sxs-lookup"><span data-stu-id="0a9a6-141">Operations for DaRT 10</span></span>](operations-for-dart-10.md)

[<span data-ttu-id="0a9a6-142">Восстановление компьютеров с помощью DaRT 10</span><span class="sxs-lookup"><span data-stu-id="0a9a6-142">Recovering Computers Using DaRT 10</span></span>](recovering-computers-using-dart-10.md)








