---
title: Создание ускорителя пакетов с помощью PowerShell
description: Создание ускорителя пакетов с помощью PowerShell
author: dansimp
ms.assetid: 0cb98394-4477-4193-8c5f-1c1773c7263a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 347572343cff058a7494574035464d66c4d61be4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814280"
---
# <span data-ttu-id="85725-103">Создание ускорителя пакетов с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="85725-103">How to Create a Package Accelerator by Using PowerShell</span></span>


<span data-ttu-id="85725-104">Ускорители пакетов приложений для App-V 5,1 автоматически последовательного порядка больших и сложных приложений.</span><span class="sxs-lookup"><span data-stu-id="85725-104">App-V 5.1 package accelerators automatically sequence large, complex applications.</span></span> <span data-ttu-id="85725-105">Кроме того, если вы примените ускоритель пакетов для App-V 5,1, вам не всегда нужно вручную устанавливать приложение, чтобы создать виртуализированный пакет.</span><span class="sxs-lookup"><span data-stu-id="85725-105">Additionally, when you apply an App-V 5.1 package accelerator, you are not always required to manually install an application to create the virtualized package.</span></span>

**<span data-ttu-id="85725-106">Создание ускорителя пакетов</span><span class="sxs-lookup"><span data-stu-id="85725-106">To create a package accelerator</span></span>**

1.  <span data-ttu-id="85725-107">Установите секвенсор App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="85725-107">Install the App-V 5.1 sequencer.</span></span> <span data-ttu-id="85725-108">Дополнительные сведения об установке секвенсора вы узнаете, [как установить секвенсор](how-to-install-the-sequencer-51beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="85725-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md).</span></span>

2.  <span data-ttu-id="85725-109">Чтобы открыть консоль PowerShell, нажмите кнопку **Пуск** и введите **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="85725-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="85725-110">Щелкните правой кнопкой мыши элемент **Windows PowerShell** и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="85725-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span> <span data-ttu-id="85725-111">Используйте командлет **New-AppvPackageAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="85725-111">Use the **New-AppvPackageAccelerator** cmdlet.</span></span>

3.  <span data-ttu-id="85725-112">Чтобы создать ускоритель пакетов, убедитесь, что у вас есть пакет. AppV для создания ускорителя с установочного носителя или установочных файлов и, при необходимости, файла сведений о прочтении для потребителей используемого ускорителя.</span><span class="sxs-lookup"><span data-stu-id="85725-112">To create a package accelerator, make sure that you have the .appv package to create an accelerator from, the installation media or installation files, and optionally a read me file for consumers of the accelerator to use.</span></span> <span data-ttu-id="85725-113">Для использования командлета ускорителя пакетов требуются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="85725-113">The following parameters are required to use the package accelerator cmdlet:</span></span>

    -   <span data-ttu-id="85725-114">**InstalledFilesPath** — задает путь установки приложения.</span><span class="sxs-lookup"><span data-stu-id="85725-114">**InstalledFilesPath** - specifies the application installation path.</span></span>

    -   <span data-ttu-id="85725-115">**Установщик** — задает путь к носителю установщика приложения.</span><span class="sxs-lookup"><span data-stu-id="85725-115">**Installer** – specifies the path to the application installer media</span></span>

    -   <span data-ttu-id="85725-116">**InputPackagePath** — задает путь к AppV-пакету.</span><span class="sxs-lookup"><span data-stu-id="85725-116">**InputPackagePath** – specifies the path to the .appv package</span></span>

    -   <span data-ttu-id="85725-117">**Path** — задает выходной каталог для пакета.</span><span class="sxs-lookup"><span data-stu-id="85725-117">**Path** – specifies the output directory for the package.</span></span>

    <span data-ttu-id="85725-118">В следующем примере показано, как создать ускоритель пакетов с помощью AppV-пакета и установочного носителя.</span><span class="sxs-lookup"><span data-stu-id="85725-118">The following example displays how you can create a package accelerator with an .appv package and the installation media:</span></span>

    **<span data-ttu-id="85725-119">Путь New-AppvPackageAccelerator-InputPackagePath &lt; к файлу. AppV — путь к &gt; &lt; исполняемому файлу Installer &gt; — путь к &lt; каталогу выходных данных&gt;</span><span class="sxs-lookup"><span data-stu-id="85725-119">New-AppvPackageAccelerator -InputPackagePath &lt;path to the .appv file&gt; -Installer &lt;path to the installer executable&gt; -Path &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="85725-120">Дополнительные параметры, которые можно использовать с командлетом **New-AppvPackageAccelerator** , отображаются в следующем списке:</span><span class="sxs-lookup"><span data-stu-id="85725-120">Additional optional parameters that can be used with the **New-AppvPackageAccelerator** cmdlet are displayed in the following list:</span></span>

    -   <span data-ttu-id="85725-121">**AcceleratorDescriptionFile** — задает путь к инструкции ускорителя пакетов, созданным пользователем.</span><span class="sxs-lookup"><span data-stu-id="85725-121">**AcceleratorDescriptionFile** - specifies the path to user created package accelerator instructions.</span></span> <span data-ttu-id="85725-122">Инструкции ускорителя пакетов — это файлы с описаниями **txt** или **RTF** , которые будут упакованы вместе с пакетом, созданным с помощью ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="85725-122">The package accelerator instructions are **.txt** or **.rtf** description files that will be packaged with the package created using the package accelerator.</span></span>

    <span data-ttu-id="85725-123">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="85725-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="85725-124">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="85725-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="85725-125">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="85725-125">Got an App-V issue?</span></span>** <span data-ttu-id="85725-126">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="85725-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="85725-127">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="85725-127">Related topics</span></span>


[<span data-ttu-id="85725-128">Администрирование App-V 5.1 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="85725-128">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)

 

 





