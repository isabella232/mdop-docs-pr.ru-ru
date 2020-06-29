---
title: Настройка образа Windows Virtual PC для MED-V
description: Настройка образа Windows Virtual PC для MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826819"
---
# <span data-ttu-id="2f325-103">Настройка образа Windows Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="2f325-103">Configuring a Windows Virtual PC Image for MED-V</span></span>


<span data-ttu-id="2f325-104">После установки всех элементов, которые вы хотите включить в образ MED-V, вы можете настроить его для использования в Microsoft Enterprise Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f325-104">After you have installed everything that you want to include in your MED-V image, you can configure the image for use in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span> <span data-ttu-id="2f325-105">В этом разделе приведены рекомендации по настройке образа MED-V для запуска программы установки в первый раз перед созданием пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="2f325-105">The topics in this section provide guidance for configuring your MED-V image to run first time setup before you create your MED-V workspace package.</span></span>

<span data-ttu-id="2f325-106">При первом запуске программы установки будет выполнена подготовка рабочей области MED-V для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f325-106">First time setup prepares the MED-V workspace for an end user.</span></span> <span data-ttu-id="2f325-107">Процесс создает виртуальную машину из образа, упакованного в рабочую область MED-V, и затем запускает мини-настройку Windows на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2f325-107">The process creates a virtual machine from the image packaged in the MED-V workspace and then runs Windows Mini-Setup on the virtual machine.</span></span> <span data-ttu-id="2f325-108">Это включает в себя выполнение как настраиваемых сценариев настройки, так и первого приложения завершения настройки FtsCompletion.exe.</span><span class="sxs-lookup"><span data-stu-id="2f325-108">This includes the running of both custom setup scripts and the first time setup completion application, FtsCompletion.exe.</span></span>

<span data-ttu-id="2f325-109">Выполните указанные ниже действия, чтобы настроить изображение MED-V для первого запуска программы установки.</span><span class="sxs-lookup"><span data-stu-id="2f325-109">Follow these steps to configure your MED-V image for running first time setup:</span></span>

1. <span data-ttu-id="2f325-110">В качестве варианта вы можете сжать виртуальный жесткий диск (VHD), чтобы освободить пустое место на диске, а затем уменьшить размер виртуального жесткого диска, прежде чем продолжить настройку образа Virtual PC для Windows.</span><span class="sxs-lookup"><span data-stu-id="2f325-110">As an option, you can compact the virtual hard disk (VHD) to reclaim empty disk space and reduce the size of the VHD before you continue with configuring the Windows Virtual PC image.</span></span> <span data-ttu-id="2f325-111">Дополнительные сведения можно найти [в разделе Сжатие виртуального жесткого диска MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="2f325-111">For more information, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

2. <span data-ttu-id="2f325-112">Настройте процесс настройки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f325-112">Customize the virtual machine setup process.</span></span>

3. <span data-ttu-id="2f325-113">Запечатайте образ MED-V с помощью Sysprep.</span><span class="sxs-lookup"><span data-stu-id="2f325-113">Seal the MED-V image by using Sysprep.</span></span>

   **<span data-ttu-id="2f325-114">Настройка процесса настройки виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2f325-114">Customizing the Virtual Machine Setup Process</span></span>**

4. <span data-ttu-id="2f325-115">В процессе подготовки образа для использования с MED-V вы можете настраивать различные параметры на виртуальной машине, например задавать параметры для запуска центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="2f325-115">As part of preparing your image for use with MED-V, you can configure various settings on the virtual machine, such as specifying the settings for running Windows Update.</span></span> <span data-ttu-id="2f325-116">Укажите все необходимые параметры виртуальной машины перед созданием пакета рабочей области для MED-V.</span><span class="sxs-lookup"><span data-stu-id="2f325-116">Specify all the necessary virtual machine settings before you create the MED-V workspace package.</span></span>

5. <span data-ttu-id="2f325-117">Перед созданием пакета рабочей области для MED-V мы рекомендуем отключить точки восстановления на виртуальной машине, чтобы не допустить неограниченного увеличения разностного диска.</span><span class="sxs-lookup"><span data-stu-id="2f325-117">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="2f325-118">Дополнительные сведения можно найти в разделе Отключение [и включение восстановления системы в Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="2f325-118">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

   **<span data-ttu-id="2f325-119">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2f325-119">Note</span></span>**  
   <span data-ttu-id="2f325-120">Вы можете настроить файл Sysprep. INF, чтобы отключить точки восстановления при первом запуске программы установки.</span><span class="sxs-lookup"><span data-stu-id="2f325-120">You can set up your Sysprep.inf file to disable restore points when first time setup is run.</span></span> <span data-ttu-id="2f325-121">Пример настройки этого ключа GuiRunOnce можно найти в разделе Пример файла Sysprep. inf ниже.</span><span class="sxs-lookup"><span data-stu-id="2f325-121">For an example of setting this GuiRunOnce key, see the sample Sysprep.inf file later in this section.</span></span>



6. <span data-ttu-id="2f325-122">Настройте процесс настройки так, чтобы вместо экрана приветствия Windows по умолчанию выполнялась мини-установка.</span><span class="sxs-lookup"><span data-stu-id="2f325-122">Configure the setup process to run Mini-Setup instead of the default Windows Welcome.</span></span> <span data-ttu-id="2f325-123">Вы должны запустить средство Sysprep с помощью переключателя **-Mini** или установить флажок **MiniSetup** в графическом интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="2f325-123">You must either run the Sysprep tool by using the **-mini** switch, or select the **MiniSetup** check box in the graphical user interface.</span></span> <span data-ttu-id="2f325-124">Дополнительные сведения [можно найти в разделе как запечатать изображение с помощью Sysprep](#bkmk-seal).</span><span class="sxs-lookup"><span data-stu-id="2f325-124">For more information, see [How to Seal the Image with Sysprep](#bkmk-seal).</span></span>

   **<span data-ttu-id="2f325-125">Вызов файла завершения настройки в первый раз</span><span class="sxs-lookup"><span data-stu-id="2f325-125">Calling the First time setup Completion File</span></span>**

   1.  <span data-ttu-id="2f325-126">Исполняемый файл, именуемый FtsCompletion.exe, входит в состав установки гостевого агента MED-V.</span><span class="sxs-lookup"><span data-stu-id="2f325-126">An executable called FtsCompletion.exe is included as part of the installation of the MED-V Guest Agent.</span></span> <span data-ttu-id="2f325-127">По умолчанию он находится на системном диске вашего образа MED-V в разделе **файлы программ — виртуализация классической версии Microsoft Enterprise**.</span><span class="sxs-lookup"><span data-stu-id="2f325-127">By default, it is located in the system drive of your MED-V image under **Program Files – Microsoft Enterprise Desktop Virtualization**.</span></span>

       **<span data-ttu-id="2f325-128">Важно.</span><span class="sxs-lookup"><span data-stu-id="2f325-128">Important</span></span>**  
       <span data-ttu-id="2f325-129">На последнем этапе при первом запуске программы установки необходимо запустить эту программу.</span><span class="sxs-lookup"><span data-stu-id="2f325-129">As the final step in the first time setup process, you must run this executable program.</span></span> <span data-ttu-id="2f325-130">Пользователь, для которого вызывается исполняемая программа, должен быть членом локальной группы администраторов гостя.</span><span class="sxs-lookup"><span data-stu-id="2f325-130">The user for whom the executable program is being called must be a member of the guest’s local administrator group.</span></span>



   2.  <span data-ttu-id="2f325-131">Вы можете выбрать способ вызова этой исполняемой программы, например, с помощью сценария, развернутого вместе с рабочей областью MED-V.</span><span class="sxs-lookup"><span data-stu-id="2f325-131">You can decide how you want to call this executable program, for example, through a script that is deployed with the MED-V workspace.</span></span> <span data-ttu-id="2f325-132">Вы можете вызвать этот исполняемый файл в последней строке файла Sysprep. INF.</span><span class="sxs-lookup"><span data-stu-id="2f325-132">You can call this executable as the last line of your Sysprep.inf file.</span></span> <span data-ttu-id="2f325-133">Пример вызова этой исполняемой программы в файле Sysprep. inf можно найти в файле примера ниже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="2f325-133">For an example of how to call this executable program in your Sysprep.inf file, see the sample file later in this section.</span></span>

<span data-ttu-id="2f325-134">После завершения настройки изображения MED-V вы можете запечатать его с помощью Sysprep.</span><span class="sxs-lookup"><span data-stu-id="2f325-134">After you have completed customization of your MED-V image, you are ready to seal the image by using Sysprep.</span></span>

<a href="" id="bkmk-seal"></a>**<span data-ttu-id="2f325-135">Запечатывание образа MED-V с помощью программы Sysprep</span><span class="sxs-lookup"><span data-stu-id="2f325-135">Sealing the MED-V Image by Using Sysprep</span></span>**

1.  <span data-ttu-id="2f325-136">Программа подготовки системы (Sysprep) — это технология, которую можно использовать для выполнения установок на основе изображений во всей сети с минимальным вмешательством администратора или специалистами по ИТ-профессионалам.</span><span class="sxs-lookup"><span data-stu-id="2f325-136">The System Preparation tool (Sysprep) is a technology that you can use to perform image-based installations throughout the network with minimal intervention by an administrator or IT-Professional.</span></span>

2.  <span data-ttu-id="2f325-137">В среде MED-V вы можете использовать Sysprep для присвоения уникальных идентификаторов безопасности (SID) и других параметров для каждой рабочей области MED-V при первом запуске.</span><span class="sxs-lookup"><span data-stu-id="2f325-137">In a MED-V environment, you can use Sysprep to assign unique security IDs (SID) and other settings to each MED-V workspace the first time that they are started.</span></span>

    **<span data-ttu-id="2f325-138">Примечание.</span><span class="sxs-lookup"><span data-stu-id="2f325-138">Note</span></span>**  
    <span data-ttu-id="2f325-139">Дополнительные сведения об использовании Sysprep можно найти в [техническом справочнике по Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .</span><span class="sxs-lookup"><span data-stu-id="2f325-139">For more information about how to use Sysprep, see [Sysprep Technical Reference](https://go.microsoft.com/fwlink/?LinkId=195930) (https://go.microsoft.com/fwlink/?LinkId=195930).</span></span>



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## <span data-ttu-id="2f325-140">Пример.</span><span class="sxs-lookup"><span data-stu-id="2f325-140">Example</span></span>


<span data-ttu-id="2f325-141">Ниже приведен пример файла Sysprep. INF.</span><span class="sxs-lookup"><span data-stu-id="2f325-141">Here is an example of a Sysprep.inf file.</span></span>

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## <span data-ttu-id="2f325-142">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="2f325-142">Related topics</span></span>


[<span data-ttu-id="2f325-143">Создание пакета рабочих областей MED-V</span><span class="sxs-lookup"><span data-stu-id="2f325-143">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

[<span data-ttu-id="2f325-144">Подготовка образа MED-V</span><span class="sxs-lookup"><span data-stu-id="2f325-144">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









