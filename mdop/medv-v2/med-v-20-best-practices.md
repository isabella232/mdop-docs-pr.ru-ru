---
title: Советы и рекомендации по MED-V 2.0
description: Советы и рекомендации по MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826112"
---
# <span data-ttu-id="62c1c-103">Советы и рекомендации по MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="62c1c-103">MED-V 2.0 Best Practices</span></span>


<span data-ttu-id="62c1c-104">При планировании, развертывании и управлении MED-V на предприятии Вы можете найти рекомендации по лучшим рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="62c1c-104">When you are planning, deploying, and managing MED-V in your enterprise, you may find the best practice recommendations to be useful.</span></span>

### <span data-ttu-id="62c1c-105">Настройка первого запуска программы установки в автоматическом режиме</span><span class="sxs-lookup"><span data-stu-id="62c1c-105">Configure first time setup to run unattended</span></span>

<span data-ttu-id="62c1c-106">Несмотря на то что вы можете задать любые предпочтительные параметры, лучше всего создать файл Sysprep. INF, чтобы при первом запуске программы установки в **автоматическом** режиме вы могли выполнить настройку.</span><span class="sxs-lookup"><span data-stu-id="62c1c-106">Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode.</span></span> <span data-ttu-id="62c1c-107">Для этого вам потребуется предоставить все необходимые сведения о параметрах, как только вы просматриваете мастер **настройки диспетчера установки** .</span><span class="sxs-lookup"><span data-stu-id="62c1c-107">This requires you to provide all the required settings information as you continue through the **Setup Manager** wizard.</span></span> <span data-ttu-id="62c1c-108">Дополнительные сведения о том, как настроить образ MED-V, приведены в разделе [Настройка образа ВИРТУАЛЬНЫХ компьютеров Windows для MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="62c1c-108">For more information about how to configure the MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="62c1c-109">Отключение точек восстановления на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="62c1c-109">Disable restore points on the virtual machine</span></span>

<span data-ttu-id="62c1c-110">Перед созданием пакета рабочей области для MED-V мы рекомендуем отключить точки восстановления на виртуальной машине, чтобы не допустить неограниченного увеличения разностного диска.</span><span class="sxs-lookup"><span data-stu-id="62c1c-110">Before you create the MED-V workspace package, we recommend that you disable restore points on the virtual machine to prevent the differencing disk from growing unbounded.</span></span> <span data-ttu-id="62c1c-111">Дополнительные сведения можно найти в разделе Отключение [и включение восстановления системы в Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .</span><span class="sxs-lookup"><span data-stu-id="62c1c-111">For more information, see [How to turn off and turn on System Restore in Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) (https://go.microsoft.com/fwlink/?LinkId=195927).</span></span>

### <span data-ttu-id="62c1c-112">Настройка изображения MED-V для использования локальных профилей</span><span class="sxs-lookup"><span data-stu-id="62c1c-112">Configure MED-V image to use local profiles</span></span>

<span data-ttu-id="62c1c-113">Рекомендуется применять только те политики, которые имеют смысл в среде совместимости приложений для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="62c1c-113">We recommend that you apply only those policies that make sense in an application compatibility environment for Windows XP.</span></span> <span data-ttu-id="62c1c-114">Например, политики настройки рабочего стола обычно не нужно применять и должны быть отключены.</span><span class="sxs-lookup"><span data-stu-id="62c1c-114">For example, desktop customization policies do not typically have to be applied and should be disabled.</span></span> <span data-ttu-id="62c1c-115">Дополнительные сведения о том, как разрешить только локальные профили, можно найти в разделе [Параметры групповой политики для перемещаемых профилей пользователей](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .</span><span class="sxs-lookup"><span data-stu-id="62c1c-115">For more information about how to allow only local profiles, see [Group Policy Settings for Roaming User Profiles](https://go.microsoft.com/fwlink/?LinkId=205072) (https://go.microsoft.com/fwlink/?LinkId=205072).</span></span>

### <span data-ttu-id="62c1c-116">Настройка обновления производительности групповой политики</span><span class="sxs-lookup"><span data-stu-id="62c1c-116">Configure a Group Policy performance update</span></span>

<span data-ttu-id="62c1c-117">По умолчанию групповая политика загружается на компьютер по одному байту за раз.</span><span class="sxs-lookup"><span data-stu-id="62c1c-117">By default, Group Policy is downloaded to a computer one byte at a time.</span></span> <span data-ttu-id="62c1c-118">Это приводит к задержке при присоединении MED-V к домену.</span><span class="sxs-lookup"><span data-stu-id="62c1c-118">This causes delays when MED-V is being joined to the domain.</span></span> <span data-ttu-id="62c1c-119">Для повышения производительности групповой политики рекомендуется присвоить реестру значение следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="62c1c-119">To increase the performance of Group Policy, we recommend that you set the following registry key value to the registry:</span></span>

<span data-ttu-id="62c1c-120">Подраздел реестра: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span><span class="sxs-lookup"><span data-stu-id="62c1c-120">Registry subkey: HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon</span></span>

<span data-ttu-id="62c1c-121">Entry (запись): BufferPolicyReads</span><span class="sxs-lookup"><span data-stu-id="62c1c-121">Entry: BufferPolicyReads</span></span>

<span data-ttu-id="62c1c-122">Type (тип): DWORD</span><span class="sxs-lookup"><span data-stu-id="62c1c-122">Type: DWORD</span></span>

<span data-ttu-id="62c1c-123">Значение: 1</span><span class="sxs-lookup"><span data-stu-id="62c1c-123">Value: 1</span></span>

### <span data-ttu-id="62c1c-124">Распространение юридической уведомления с помощью групповой политики вместо изображения MED-V</span><span class="sxs-lookup"><span data-stu-id="62c1c-124">Distribute legal notice through Group Policy instead of in the MED-V image</span></span>

<span data-ttu-id="62c1c-125">Если вы хотите, чтобы конечные пользователи выработали соглашение об уровне обслуживания (SLA) до того, как они смогут получить доступ к MED-V, мы рекомендуем принудительно применить SLA с помощью групповой политики, чтобы после первой настройки было видно, что это соглашение будет отображаться для конечного пользователя.</span><span class="sxs-lookup"><span data-stu-id="62c1c-125">If you want end users to see a service level agreement (SLA) before they access MED-V, we recommend that you enforce the SLA through Group Policy later so that the SLA is displayed to the end user after the first time setup is finished.</span></span>

<span data-ttu-id="62c1c-126">**Внимание!**  Несмотря на то, что при первом запуске программы установки в **автоматическом** режиме вы решите, что в качестве локальной политики или записи в реестре требуется включить SLA (виртуальный жесткий диск), необходимо также указать, **что при первом** запуске программы установки может произойти сбой.</span><span class="sxs-lookup"><span data-stu-id="62c1c-126">**Caution** Even though a best practice is to run first time setup in **Unattended** mode, if you decide to set the local policy or registry entry to include an SLA in your image (virtual hard disk), you must also specify that first time setup is run in **Attended** mode, or first time setup can fail.</span></span>

 

### <span data-ttu-id="62c1c-127">Сжатие виртуального жесткого диска</span><span class="sxs-lookup"><span data-stu-id="62c1c-127">Compact the virtual hard disk</span></span>

<span data-ttu-id="62c1c-128">Рекомендуется сжать виртуальный жесткий диск, чтобы освободить пустое место на диске, и уменьшить размер виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="62c1c-128">We recommend that you compact your virtual hard disk to reclaim empty disk space and reduce the size of the virtual hard disk.</span></span> <span data-ttu-id="62c1c-129">Дополнительные сведения о сжатии виртуального жесткого диска можно найти [в разделе Сжатие виртуального жесткого диска MED-V](compacting-the-med-v-virtual-hard-disk.md).</span><span class="sxs-lookup"><span data-stu-id="62c1c-129">For more information about how to compact your virtual hard disk, see [Compacting the MED-V Virtual Hard Disk](compacting-the-med-v-virtual-hard-disk.md).</span></span>

### <span data-ttu-id="62c1c-130">Настройка виртуальной машины для перезапуска при сбое синего экрана</span><span class="sxs-lookup"><span data-stu-id="62c1c-130">Configure virtual machine to restart on blue screen crash</span></span>

<span data-ttu-id="62c1c-131">Рекомендуется настроить виртуальную машину рабочей области для MED-V так, чтобы она автоматически перезаработала при возникновении синего сбоя экрана.</span><span class="sxs-lookup"><span data-stu-id="62c1c-131">We recommend that you configure the MED-V workspace virtual machine to automatically restart when it encounters a blue screen crash.</span></span> <span data-ttu-id="62c1c-132">Чтобы настроить этот параметр в гостевой учетной записью, установите для параметра "Автозагрузка" в разделе HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl ("1").</span><span class="sxs-lookup"><span data-stu-id="62c1c-132">To configure this setting in the guest, set the AutoReboot value in the HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\CrashControl key to “1”.</span></span>

<span data-ttu-id="62c1c-133">Вы также можете настроить этот параметр, нажав кнопку **Пуск**и выбрав пункт **Панель управления**, а затем — пункт **система**.</span><span class="sxs-lookup"><span data-stu-id="62c1c-133">You can also configure this setting by clicking **Start**, clicking **Control Panel**, and then clicking **System**.</span></span> <span data-ttu-id="62c1c-134">Затем в разделе " **Загрузка и восстановление** " на вкладке " **Дополнительно** " нажмите кнопку " **Параметры**".</span><span class="sxs-lookup"><span data-stu-id="62c1c-134">Then, in the **Startup and Recovery** area of the **Advanced** tab, click **Settings**.</span></span> <span data-ttu-id="62c1c-135">Установите флажок **Автоматический перезапуск** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="62c1c-135">Select the **Automatically restart** check box and click **OK**.</span></span>

### <span data-ttu-id="62c1c-136">Создание резервной копии образа MED-V перед запечатыванием</span><span class="sxs-lookup"><span data-stu-id="62c1c-136">Back up MED-V image before sealing it</span></span>

<span data-ttu-id="62c1c-137">Рекомендуется создать резервную копию изображения MED-V перед запечатыванием.</span><span class="sxs-lookup"><span data-stu-id="62c1c-137">We recommend that you create a backup copy of the MED-V image before you seal it.</span></span> <span data-ttu-id="62c1c-138">Дополнительные сведения о запечатывании изображений в MED-V можно найти [в разделе Настройка образа Windows Virtual PC для MED-v](configuring-a-windows-virtual-pc-image-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="62c1c-138">For more information about sealing your MED-V image, see [Configuring a Windows Virtual PC Image for MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).</span></span>

### <span data-ttu-id="62c1c-139">Установка Windows Virtual PC в последнюю очередь при установке из пакетного файла</span><span class="sxs-lookup"><span data-stu-id="62c1c-139">Install Windows Virtual PC last when installing from a batch file</span></span>

<span data-ttu-id="62c1c-140">При установке компонентов MED-V с помощью пакетного файла укажите, что Windows Virtual PC и Windows Virtual PC Hotfix устанавливаются после агента узла MED-V и файлов пакета MED-V Workspace.</span><span class="sxs-lookup"><span data-stu-id="62c1c-140">When you install the MED-V components by using a batch file, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="62c1c-141">Это гарантирует, что при установке центра обновления Windows не будет вмешательство в процесс установки, требующего перезапуска.</span><span class="sxs-lookup"><span data-stu-id="62c1c-141">This ensures that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

### <span data-ttu-id="62c1c-142">Установка рабочей области MED-V из локальной папки</span><span class="sxs-lookup"><span data-stu-id="62c1c-142">Install MED-V workspace from local folder</span></span>

<span data-ttu-id="62c1c-143">Из-за проблем, которые могут возникнуть при установке MED-V из сетевого расположения, рекомендуется скопировать файлы настройки рабочей области для MED-V на локальном компьютере, а затем запустить setup.exe.</span><span class="sxs-lookup"><span data-stu-id="62c1c-143">Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a><span data-ttu-id="62c1c-144">Управление перенаправлением принтеров только одним способом</span><span class="sxs-lookup"><span data-stu-id="62c1c-144">Manage printer redirection in one manner only</span></span>

<span data-ttu-id="62c1c-145">Если принтер установлен вручную на гостевой виртуальной машине MED-V и этот же принтер позже установлен на главном компьютере, результат будет установлен дважды на гостевой машине.</span><span class="sxs-lookup"><span data-stu-id="62c1c-145">If a printer is manually installed on the MED-V guest virtual machine, and the same printer is later installed on the host computer, the result is that it is installed two times in the guest.</span></span> <span data-ttu-id="62c1c-146">Чтобы избежать такой ситуации, рекомендуется использовать функцию MED-V для управления перенаправлением принтеров одним способом: отключите перенаправление и установите принтеры вручную на гостевой или включите перенаправление и не устанавливайте принтеры вручную на гостевой машине.</span><span class="sxs-lookup"><span data-stu-id="62c1c-146">To avoid this situation, we recommend as MED-V best practice that you manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a><span data-ttu-id="62c1c-147">Настройка параметров гостевой установки для системы MED-V</span><span class="sxs-lookup"><span data-stu-id="62c1c-147">Configure settings for MED-V guest patching</span></span>

<span data-ttu-id="62c1c-148">Вы можете управлять тем, когда и в течение какого времени виртуальная машина MED-V может получать автоматические обновления, определяя необходимые значения конфигурации в реестре.</span><span class="sxs-lookup"><span data-stu-id="62c1c-148">You can control when and for how long the MED-V virtual machine awakens to receive automatic updates by defining the relevant configuration values in the registry.</span></span> <span data-ttu-id="62c1c-149">Для работы с помощью MED-V рекомендуется настроить интервал пробуждения таким образом, чтобы он соответствовал времени запланированных регулярных обновлений для виртуальных машин на основе MED-V.</span><span class="sxs-lookup"><span data-stu-id="62c1c-149">A MED-V best practice is to set your wake-up interval to match the time when you have scheduled regular updates for MED-V virtual machines.</span></span> <span data-ttu-id="62c1c-150">Кроме того, рекомендуется настроить эти параметры таким образом, чтобы они соответствовали поведению хост-компьютера.</span><span class="sxs-lookup"><span data-stu-id="62c1c-150">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

<span data-ttu-id="62c1c-151">Дополнительные сведения о том, как настроить параметры гостевой системы MED-V, приведены в разделе [Управление автоматическим обновлением для рабочих областей med-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="62c1c-151">For more information about how to configure settings for MED-V guest patching, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

### <span data-ttu-id="62c1c-152">Настройка программного обеспечения для защиты от вирусов и резервного копирования</span><span class="sxs-lookup"><span data-stu-id="62c1c-152">Configure antivirus/backup software</span></span>

<span data-ttu-id="62c1c-153">Чтобы предотвратить влияние антивирусной программы на производительность виртуального рабочего стола, мы рекомендуем вам по возможности исключить следующие типы файлов виртуальных машин из антивирусной программы или процесса резервного копирования, запущенного на компьютере с операционной системой MED-V:</span><span class="sxs-lookup"><span data-stu-id="62c1c-153">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend that when you can, you exclude the following virtual machine file types from any antivirus or backup process that is running on the MED-V host computer:</span></span>

-   <span data-ttu-id="62c1c-154">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="62c1c-154">\*.VMC</span></span>

-   <span data-ttu-id="62c1c-155">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="62c1c-155">\*.VUD</span></span>

-   <span data-ttu-id="62c1c-156">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="62c1c-156">\*.VSV</span></span>

-   <span data-ttu-id="62c1c-157">\*. VHD</span><span class="sxs-lookup"><span data-stu-id="62c1c-157">\*.VHD</span></span>

## <span data-ttu-id="62c1c-158">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="62c1c-158">Related topics</span></span>


[<span data-ttu-id="62c1c-159">Безопасность и защита MED-V</span><span class="sxs-lookup"><span data-stu-id="62c1c-159">Security and Protection for MED-V</span></span>](security-and-protection-for-med-v.md)

 

 





