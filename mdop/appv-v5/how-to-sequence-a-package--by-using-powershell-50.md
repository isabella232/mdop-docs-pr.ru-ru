---
title: Упорядочение пакета с помощью PowerShell
description: Упорядочение пакета с помощью PowerShell
author: dansimp
ms.assetid: b41feed9-d1c5-48a3-940c-9a21d594f4f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbb9641ba75eda4d190892fa2bd0043c92ed9006
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813701"
---
# <span data-ttu-id="974b2-103">Упорядочение пакета с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="974b2-103">How to Sequence a Package by Using PowerShell</span></span>


<span data-ttu-id="974b2-104">Чтобы создать новый пакет App-V 5,0 с помощью PowerShell, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="974b2-104">Use the following procedure to create a new App-V 5.0 package using PowerShell.</span></span>

<span data-ttu-id="974b2-105">**Примечание**  Прежде чем использовать эту процедуру, необходимо скопировать соответствующие файлы установщика на компьютер, на котором работает программа Sequencer, и ознакомиться с разделом секвенсор, описанным в разделе [планирование для приложения App-V 5,0 Sequencer и Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="974b2-105">**Note** Before you use this procedure you must copy the associated installer files to the computer running the sequencer and you have read and understand the sequencer section of [Planning for the App-V 5.0 Sequencer and Client Deployment](planning-for-the-app-v-50-sequencer-and-client-deployment.md).</span></span>

 

**<span data-ttu-id="974b2-106">Создание нового виртуального приложения с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="974b2-106">To create a new virtual application using PowerShell</span></span>**

1.  <span data-ttu-id="974b2-107">Установите секвенсор App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="974b2-107">Install the App-V 5.0 sequencer.</span></span> <span data-ttu-id="974b2-108">Дополнительные сведения об установке секвенсора вы узнаете, [как установить секвенсор](how-to-install-the-sequencer-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="974b2-108">For more information about installing the sequencer see [How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md).</span></span>

2.  <span data-ttu-id="974b2-109">Чтобы открыть консоль PowerShell, нажмите кнопку **Пуск** и введите **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="974b2-109">To open a PowerShell console click **Start** and type **PowerShell**.</span></span> <span data-ttu-id="974b2-110">Щелкните правой кнопкой мыши элемент **Windows PowerShell** и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="974b2-110">Right-click **Windows PowerShell** and select **Run as Administrator**.</span></span>

3.  <span data-ttu-id="974b2-111">С помощью консоли PowerShell введите следующую команду: **Import-Module appvsequencer**.</span><span class="sxs-lookup"><span data-stu-id="974b2-111">Using the PowerShell console, type the following: **import-module appvsequencer**.</span></span>

4.  <span data-ttu-id="974b2-112">Чтобы создать пакет, используйте командлет **New-AppvSequencerPackage** .</span><span class="sxs-lookup"><span data-stu-id="974b2-112">To create a package, use the **New-AppvSequencerPackage** cmdlet.</span></span> <span data-ttu-id="974b2-113">Для создания пакета необходимы следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="974b2-113">The following parameters are required to create a package:</span></span>

    -   <span data-ttu-id="974b2-114">**Name (имя** ) — задает имя пакета.</span><span class="sxs-lookup"><span data-stu-id="974b2-114">**Name** - specifies the name of the package.</span></span>

    -   <span data-ttu-id="974b2-115">**PrimaryVirtualApplicationDirectory** — задает путь к каталогу, который будет использоваться для установки приложения.</span><span class="sxs-lookup"><span data-stu-id="974b2-115">**PrimaryVirtualApplicationDirectory** - specifies the path to the directory that will be used to install the application.</span></span> <span data-ttu-id="974b2-116">Этот путь должен существовать.</span><span class="sxs-lookup"><span data-stu-id="974b2-116">This path must exist.</span></span>

    -   <span data-ttu-id="974b2-117">**Installer (установщик** ) — задает путь к соответствующему установщику приложения.</span><span class="sxs-lookup"><span data-stu-id="974b2-117">**Installer** - specifies the path to the associated application installer.</span></span>

    -   <span data-ttu-id="974b2-118">**Path** — задает выходной каталог для пакета.</span><span class="sxs-lookup"><span data-stu-id="974b2-118">**Path** - specifies the output directory for the package.</span></span>

    <span data-ttu-id="974b2-119">Пример</span><span class="sxs-lookup"><span data-stu-id="974b2-119">For example:</span></span>

    **<span data-ttu-id="974b2-120">New-AppvSequencerPackage-Name (имя &lt; пакета &gt; -PrimaryVirtualApplicationDirectory) путь к &lt; корневому &gt; &lt; каталогу пакета — путь к исполняемому файлу установщика &gt; -OutputPath для &lt; пути вывода.&gt;</span><span class="sxs-lookup"><span data-stu-id="974b2-120">New-AppvSequencerPackage –Name &lt;name of Package&gt; -PrimaryVirtualApplicationDirectory &lt;path to the package root&gt; -Installer &lt;path to the installer executable&gt; -OutputPath &lt;directory of the output path&gt;</span></span>**

    <span data-ttu-id="974b2-121">Дождитесь, пока секвенсор создаст пакет.</span><span class="sxs-lookup"><span data-stu-id="974b2-121">Wait for the sequencer to create the package.</span></span> <span data-ttu-id="974b2-122">Создание пакета с помощью PowerShell может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="974b2-122">Creating a package using PowerShell can take time.</span></span> <span data-ttu-id="974b2-123">Если пакет не был создан успешно, будет возвращено сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="974b2-123">If the package was not created successfully an error will be returned.</span></span>

    <span data-ttu-id="974b2-124">В следующем списке приведены дополнительные параметры, которые можно использовать с командлетом **New-AppvSequencerPackage** :</span><span class="sxs-lookup"><span data-stu-id="974b2-124">The following list displays additional optional parameters that can be used with **New-AppvSequencerPackage** cmdlet:</span></span>

    -   <span data-ttu-id="974b2-125">AcceleratorFilePath — задает путь к CAB-файлу ускорителя для создания пакета.</span><span class="sxs-lookup"><span data-stu-id="974b2-125">AcceleratorFilePath – specifies the path to the accelerator .cab file to generate a package.</span></span>

    -   <span data-ttu-id="974b2-126">InstalledFilesPath — задает путь к папке, в которой сохраняются локальные файлы приложения.</span><span class="sxs-lookup"><span data-stu-id="974b2-126">InstalledFilesPath - specifies the path to where the local installed files of the application are saved.</span></span>

    -   <span data-ttu-id="974b2-127">InstallMediaPath — задает путь к установочному носителю.</span><span class="sxs-lookup"><span data-stu-id="974b2-127">InstallMediaPath - specifies the path to where the installation media is</span></span>

    -   <span data-ttu-id="974b2-128">TemplateFilePath — путь к файлу шаблона, если вы хотите настроить процесс упорядочения.</span><span class="sxs-lookup"><span data-stu-id="974b2-128">TemplateFilePath - specifies the path to a template file if you want to customize the sequencing process.</span></span>

    -   <span data-ttu-id="974b2-129">FullLoad — указывает на то, что пакет должен быть полностью загружен на компьютер, на котором запущено приложение App-V 5,0, прежде чем его можно будет открыть.</span><span class="sxs-lookup"><span data-stu-id="974b2-129">FullLoad - specifies that the package must be fully downloaded to the computer running the App-V 5.0 before it can be opened.</span></span>

    <span data-ttu-id="974b2-130">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="974b2-130">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="974b2-131">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="974b2-131">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="974b2-132">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="974b2-132">Got an App-V issue?</span></span>** <span data-ttu-id="974b2-133">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="974b2-133">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="974b2-134">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="974b2-134">Related topics</span></span>


[<span data-ttu-id="974b2-135">Администрирование App-V с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="974b2-135">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)

 

 




