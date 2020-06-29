---
title: Создание образа Virtual PC для MED-V
description: Создание образа Virtual PC для MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823662"
---
# <span data-ttu-id="80a8e-103">Создание образа Virtual PC для MED-V</span><span class="sxs-lookup"><span data-stu-id="80a8e-103">Creating a Virtual PC Image for MED-V</span></span>


<span data-ttu-id="80a8e-104">Чтобы создать Virtual PC (VPC-образ) для MED – V, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="80a8e-104">To create a Virtual PC (VPC) image for MED-V, you must perform the following:</span></span>

1.  <span data-ttu-id="80a8e-105">[Создайте образ VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="80a8e-105">[Create a VPC image](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).</span></span>

2.  <span data-ttu-id="80a8e-106">[Установите пакет. msi для MED-V Workspace на образ VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).</span><span class="sxs-lookup"><span data-stu-id="80a8e-106">[Install the MED-V workspace .msi package onto the VPC image](#bkmk-howtoinstallthemedvworkspacemsipackage).</span></span>

3.  <span data-ttu-id="80a8e-107">[Запустите средство предварительных требований для виртуальной машины MED-V на образе VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).</span><span class="sxs-lookup"><span data-stu-id="80a8e-107">[Run the MED-V virtual machine prerequisites tool on the VPC image](#bkmk-howtorunthevirtualmachineprerequisitestool).</span></span>

4.  <span data-ttu-id="80a8e-108">[Настройте вручную необходимые виртуальные машины для образа VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span><span class="sxs-lookup"><span data-stu-id="80a8e-108">[Manually configure virtual machine prerequisites on the VPC image](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).</span></span>

5.  <span data-ttu-id="80a8e-109">[Настройте Sysprep для изображений MED-V](#bkmk-howtoconfiguresysprepformedvimages) (необязательно).</span><span class="sxs-lookup"><span data-stu-id="80a8e-109">[Configure Sysprep for MED-V images](#bkmk-howtoconfiguresysprepformedvimages) (optional).</span></span>

6.  <span data-ttu-id="80a8e-110">[Отключите Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span><span class="sxs-lookup"><span data-stu-id="80a8e-110">[Turn off Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).</span></span>

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a><span data-ttu-id="80a8e-111">Создание образа Virtual PC с помощью виртуального компьютера Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80a8e-111">Creating a Virtual PC Image by Using Microsoft Virtual PC</span></span>


<span data-ttu-id="80a8e-112">Чтобы создать образ виртуального компьютера с помощью Microsoft Virtual PC, ознакомьтесь с документацией по Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="80a8e-112">To create a Virtual PC image using Microsoft Virtual PC, refer to the Virtual PC documentation.</span></span>

<span data-ttu-id="80a8e-113">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="80a8e-113">For more information, see the following:</span></span>

-   [<span data-ttu-id="80a8e-114">Справка по Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80a8e-114">Windows Virtual PC Help</span></span>](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [<span data-ttu-id="80a8e-115">Создание виртуальной машины и установка гостевой операционной системы</span><span class="sxs-lookup"><span data-stu-id="80a8e-115">Create a virtual machine and install a guest operating system</span></span>](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a><span data-ttu-id="80a8e-116">Установка пакета "MED-V Workspace" (пакет MSI)</span><span class="sxs-lookup"><span data-stu-id="80a8e-116">How to Install the MED-V Workspace .msi Package</span></span>


<span data-ttu-id="80a8e-117">После создания образа Virtual PC установите на него пакет Windows MED-V Workspace. msi.</span><span class="sxs-lookup"><span data-stu-id="80a8e-117">After the Virtual PC image is created, install the MED-V workspace .msi package onto the image.</span></span>

**<span data-ttu-id="80a8e-118">Установка образа рабочей области для MED-V</span><span class="sxs-lookup"><span data-stu-id="80a8e-118">To install the MED-V workspace image</span></span>**

1.  <span data-ttu-id="80a8e-119">Запустите виртуальную машину и скопируйте пакет MED-V Workspace из рабочей области для Windows Inside.</span><span class="sxs-lookup"><span data-stu-id="80a8e-119">Start the virtual machine, and copy the MED-V workspace .msi package inside.</span></span>

    <span data-ttu-id="80a8e-120">Пакет для рабочей области MED-V называется *MED-V\_workspace\_x.msi*, где *x* — номер версии.</span><span class="sxs-lookup"><span data-stu-id="80a8e-120">The MED-V workspace .msi package is called *MED-V\_workspace\_x.msi*, where *x* is the version number.</span></span>

    <span data-ttu-id="80a8e-121">Например, *MED-V\_workspace\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="80a8e-121">For example, *MED-V\_workspace\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="80a8e-122">Дважды щелкните пакет Office MED-V Workspace и следуйте инструкциям мастера установки.</span><span class="sxs-lookup"><span data-stu-id="80a8e-122">Double-click the MED-V workspace .msi package, and follow the installation wizard instructions.</span></span>

    **<span data-ttu-id="80a8e-123">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80a8e-123">Note</span></span>**  
    <span data-ttu-id="80a8e-124">Если после выпуска новой версии MED-V вы обновите существующий виртуальный компьютер, удалите его, а затем перезагрузите компьютер и установите новый пакет для MED-V Workspace. msi.</span><span class="sxs-lookup"><span data-stu-id="80a8e-124">When a new MED-V version is released, and an existing Virtual PC image is updated, uninstall the existing MED-V workspace .msi package, reboot the computer, and install the new MED-V workspace .msi package.</span></span>



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a><span data-ttu-id="80a8e-125">Выполнение средства предварительных требований для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="80a8e-125">How to Run the Virtual Machine Prerequisites Tool</span></span>


<span data-ttu-id="80a8e-126">Предварительные требования виртуальной машины (VM) — это мастер, который автоматизирует некоторые предварительные условия.</span><span class="sxs-lookup"><span data-stu-id="80a8e-126">The virtual machine (VM) prerequisites tool is a wizard that automates several of the prerequisites.</span></span>

**<span data-ttu-id="80a8e-127">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80a8e-127">Note</span></span>**  
<span data-ttu-id="80a8e-128">Несмотря на то, что в мастере можно настроить многие параметры, свойства, необходимые для правильной работы MED-V, не настраиваются.</span><span class="sxs-lookup"><span data-stu-id="80a8e-128">Although many parameters are configurable in the wizard, the properties required for the proper functioning of MED-V are not configurable.</span></span>



**<span data-ttu-id="80a8e-129">Запуск средства предварительных требований для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="80a8e-129">To run the virtual machine prerequisites tool</span></span>**

1.  <span data-ttu-id="80a8e-130">После установки пакета MED-V Workspace. msi в меню **Пуск** выберите пункт **все программы, необходимые для работы &gt; с &gt; предварительными требованиями к виртуальной машине для MED-v**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-130">After the MED-V workspace .msi package is installed, on the Windows **Start** menu, select **All Programs &gt; MED-V &gt; VM Prerequisites Tool**.</span></span>

    **<span data-ttu-id="80a8e-131">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80a8e-131">Note</span></span>**  
    <span data-ttu-id="80a8e-132">Пользователь, который запускает средство предварительной установки виртуальной машины, должен иметь права локального администратора и должен быть единственным входным пользователем.</span><span class="sxs-lookup"><span data-stu-id="80a8e-132">The user running the virtual machine prerequisites tool must have local administrator rights and must be the only user logged in.</span></span>



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. <span data-ttu-id="80a8e-133">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-133">Click **Next**.</span></span>

3. <span data-ttu-id="80a8e-134">На странице " **Параметры Windows** " из указанных ниже настраиваемых свойств выберите нужные настройки.</span><span class="sxs-lookup"><span data-stu-id="80a8e-134">On the **Windows Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="80a8e-135">Очистка личных данных пользователей</span><span class="sxs-lookup"><span data-stu-id="80a8e-135">Clear users’ personal history information</span></span>**

   -   **<span data-ttu-id="80a8e-136">Очистка папки Temp Local profiles</span><span class="sxs-lookup"><span data-stu-id="80a8e-136">Clear local profiles temp directory</span></span>**

   -   **<span data-ttu-id="80a8e-137">Отключение звуков на следующих событиях Windows: запуск, вход, выход из системы</span><span class="sxs-lookup"><span data-stu-id="80a8e-137">Disable sounds on following Windows events: start, logon, logoff</span></span>**

   **<span data-ttu-id="80a8e-138">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80a8e-138">Note</span></span>**  
   <span data-ttu-id="80a8e-139">Не включайте функцию "Заставка" на странице Windows в групповой политике.</span><span class="sxs-lookup"><span data-stu-id="80a8e-139">Do not enable Windows page saver in a group policy.</span></span>



4. <span data-ttu-id="80a8e-140">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-140">Click **Next**.</span></span>

5. <span data-ttu-id="80a8e-141">На странице **параметры Internet Explorer** в указанных ниже настраиваемых свойствах выберите нужные настройки.</span><span class="sxs-lookup"><span data-stu-id="80a8e-141">On the **Internet Explorer Settings** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="80a8e-142">Не используйте функцию автоматического завершения</span><span class="sxs-lookup"><span data-stu-id="80a8e-142">Don't use auto complete features</span></span>**

   -   **<span data-ttu-id="80a8e-143">Отключение повторного использования окон при запуске сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="80a8e-143">Disable reuse of windows for launching shortcuts</span></span>**

   -   **<span data-ttu-id="80a8e-144">Очистка журнала браузера</span><span class="sxs-lookup"><span data-stu-id="80a8e-144">Clear browsing history</span></span>**

   -   **<span data-ttu-id="80a8e-145">Включение обзора с вкладками в Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="80a8e-145">Enable tabbed browsing in Internet Explorer 7</span></span>**

6. <span data-ttu-id="80a8e-146">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-146">Click **Next**.</span></span>

7. <span data-ttu-id="80a8e-147">На странице " **службы Windows** " выберите нужные настройки из следующих настраиваемых свойств:</span><span class="sxs-lookup"><span data-stu-id="80a8e-147">On the **Windows Services** page, from the following configurable properties, select the ones to be configured:</span></span>

   -   **<span data-ttu-id="80a8e-148">Служба центра обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="80a8e-148">Security center service</span></span>**

   -   **<span data-ttu-id="80a8e-149">Служба планировщика заданий</span><span class="sxs-lookup"><span data-stu-id="80a8e-149">Task scheduler service</span></span>**

   -   **<span data-ttu-id="80a8e-150">Служба автоматических обновлений</span><span class="sxs-lookup"><span data-stu-id="80a8e-150">Automatic updates service</span></span>**

   -   **<span data-ttu-id="80a8e-151">Служба восстановления системы</span><span class="sxs-lookup"><span data-stu-id="80a8e-151">System restore service</span></span>**

   -   **<span data-ttu-id="80a8e-152">Служба индексирования</span><span class="sxs-lookup"><span data-stu-id="80a8e-152">Indexing service</span></span>**

   -   **<span data-ttu-id="80a8e-153">Беспроводная настройка</span><span class="sxs-lookup"><span data-stu-id="80a8e-153">Wireless Zero Configuration</span></span>**

   -   **<span data-ttu-id="80a8e-154">Быстрая совместимость с переключением пользователей</span><span class="sxs-lookup"><span data-stu-id="80a8e-154">Fast User Switching Compatibility</span></span>**

8. <span data-ttu-id="80a8e-155">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-155">Click **Next**.</span></span>

9. <span data-ttu-id="80a8e-156">На странице **автоматического входа в Windows** выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="80a8e-156">On the **Windows Auto Logon** page, do the following:</span></span>

   1.  <span data-ttu-id="80a8e-157">Установите флажок **включить автоматический вход в Windows** .</span><span class="sxs-lookup"><span data-stu-id="80a8e-157">Select the **Enable Windows Auto Logon** check box.</span></span>

   2.  <span data-ttu-id="80a8e-158">Назначение **имени пользователя** и **пароля**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-158">Assign a **User name** and **Password**.</span></span>

10. <span data-ttu-id="80a8e-159">Нажмите кнопку **Применить**, а затем в появившемся диалоговом окне подтверждения нажмите кнопку **Да**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-159">Click **Apply**, and in the confirmation box that appears, click **Yes**.</span></span>

11. <span data-ttu-id="80a8e-160">На странице " **Сводка** " нажмите кнопку **"Готово"** , чтобы завершить работу мастера.</span><span class="sxs-lookup"><span data-stu-id="80a8e-160">On the **Summary** page, click **Finish** to quit the wizard</span></span>

**<span data-ttu-id="80a8e-161">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80a8e-161">Note</span></span>**  
<span data-ttu-id="80a8e-162">Убедитесь, что групповые политики не перезаписывают обязательные параметры, заданные в инструменте "предварительные требования".</span><span class="sxs-lookup"><span data-stu-id="80a8e-162">Verify that group policies do not overwrite the mandatory settings set in the prerequisites tool.</span></span>



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a><span data-ttu-id="80a8e-163">Настройка предварительных требований для установки виртуальной машины на основе MED-V</span><span class="sxs-lookup"><span data-stu-id="80a8e-163">How to Configure MED-V Virtual Machine Manual Installation Prerequisites</span></span>


<span data-ttu-id="80a8e-164">Некоторые из конфигураций нельзя настроить с помощью средства предварительных требований виртуальных машин, которые необходимо выполнить вручную.</span><span class="sxs-lookup"><span data-stu-id="80a8e-164">Several of the configurations cannot be configured through the virtual machine prerequisites tool and must be performed manually.</span></span>

-   <span data-ttu-id="80a8e-165">Параметры виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="80a8e-165">Virtual Machine Settings</span></span>

    <span data-ttu-id="80a8e-166">Рекомендуется настроить следующие параметры виртуальной машины в консоли Microsoft Virtual PC:</span><span class="sxs-lookup"><span data-stu-id="80a8e-166">It is recommended to configure the following virtual machine settings in the Microsoft Virtual PC console:</span></span>

    -   <span data-ttu-id="80a8e-167">Отключите дисководы для гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="80a8e-167">Disable floppy disk drives.</span></span>

    -   <span data-ttu-id="80a8e-168">Отключите функцию отмены — диски **( &gt; Отмена параметров — диски**).</span><span class="sxs-lookup"><span data-stu-id="80a8e-168">Disable undo-disks (**Settings &gt; undo-disks**).</span></span>

    -   <span data-ttu-id="80a8e-169">Убедитесь, что на изображении только один виртуальный ЦП.</span><span class="sxs-lookup"><span data-stu-id="80a8e-169">Ensure that the image has only one virtual CPU.</span></span>

    -   <span data-ttu-id="80a8e-170">Устраните взаимодействие между виртуальной машиной и пользователем, где они не связаны с опубликованными приложениями (например, сообщениями, требующими ввода данных пользователем).</span><span class="sxs-lookup"><span data-stu-id="80a8e-170">Eliminate interactions between the virtual machine and the user, where they are not related to published applications (such as, messages requiring user input).</span></span>

-   <span data-ttu-id="80a8e-171">Параметры изображения</span><span class="sxs-lookup"><span data-stu-id="80a8e-171">Image Settings</span></span>

    <span data-ttu-id="80a8e-172">Настройте следующие параметры вручную в изображении:</span><span class="sxs-lookup"><span data-stu-id="80a8e-172">Configure the following manual settings inside the image:</span></span>

    1.  <span data-ttu-id="80a8e-173">В окне **Свойства: параметры электропитание** отключите режим сна и спящий режим.</span><span class="sxs-lookup"><span data-stu-id="80a8e-173">In the **Power Options Properties** window, disable hibernation and sleep.</span></span>

    2.  <span data-ttu-id="80a8e-174">Установка последних обновлений для Windows.</span><span class="sxs-lookup"><span data-stu-id="80a8e-174">Apply the most recent Windows updates.</span></span>

    3.  <span data-ttu-id="80a8e-175">В диалоговом окне **Загрузка и восстановление Windows** в разделе **системный сбой** снимите флажок **автоматически перезапустить** .</span><span class="sxs-lookup"><span data-stu-id="80a8e-175">In the **Windows Startup and Recovery** dialog box, in the **System Failure** section, clear the **Automatically restart** check box.</span></span>

    4.  <span data-ttu-id="80a8e-176">Убедитесь, что на изображении используется ключ лицензии VLK.</span><span class="sxs-lookup"><span data-stu-id="80a8e-176">Ensure that the image uses a VLK license key.</span></span>

-   <span data-ttu-id="80a8e-177">Установка дополнений VPC</span><span class="sxs-lookup"><span data-stu-id="80a8e-177">Installing VPC Additions</span></span>

    <span data-ttu-id="80a8e-178">В меню **действия** выберите **установить или обновить дополнения для виртуальной машины**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-178">On the **Action** menu, select **Install or Update Virtual Machine Additions**.</span></span>

-   <span data-ttu-id="80a8e-179">Настройка печати</span><span class="sxs-lookup"><span data-stu-id="80a8e-179">Configuring Printing</span></span>

    <span data-ttu-id="80a8e-180">Вы можете настроить печать из рабочей области MED-V одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="80a8e-180">You can configure printing from the MED-V workspace in either of the following ways:</span></span>

    -   <span data-ttu-id="80a8e-181">Добавьте принтер на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="80a8e-181">Add a printer to the virtual machine.</span></span>

    -   <span data-ttu-id="80a8e-182">Разрешить печать с использованием принтеров, настроенных на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="80a8e-182">Allow printing with printers that are configured on the host computer.</span></span>

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a><span data-ttu-id="80a8e-183">Настройка Sysprep для изображений MED-V</span><span class="sxs-lookup"><span data-stu-id="80a8e-183">How to Configure Sysprep for MED-V Images</span></span>


<span data-ttu-id="80a8e-184">В рабочей области MED-V можно настроить Sysprep для присвоения уникального идентификатора безопасности (SID), особенно в том случае, если на одном компьютере работают несколько рабочих областей MED-V.</span><span class="sxs-lookup"><span data-stu-id="80a8e-184">In a MED-V workspace, Sysprep can be configured in order to assign unique security ID (SID), particularly when multiple MED-V workspaces are run on a single computer.</span></span> <span data-ttu-id="80a8e-185">Использовать Sysprep для присоединения к домену не рекомендуется. Вместо этого используйте действие сценария присоединиться к домену MED-V, как описано в разделе [Настройка действий сценария](how-to-set-up-script-actions.md).</span><span class="sxs-lookup"><span data-stu-id="80a8e-185">It is not recommended to use Sysprep to join a domain; instead, use the MED-V join domain script action as described in [How to Set Up Script Actions](how-to-set-up-script-actions.md).</span></span>

**<span data-ttu-id="80a8e-186">Примечание.</span><span class="sxs-lookup"><span data-stu-id="80a8e-186">Note</span></span>**  
<span data-ttu-id="80a8e-187">Sysprep — это программа подготовки системы Microsoft для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="80a8e-187">Sysprep is Microsoft's system preparation utility for the Windows operating system.</span></span>



**<span data-ttu-id="80a8e-188">Настройка Sysprep в рабочей области MED-V</span><span class="sxs-lookup"><span data-stu-id="80a8e-188">To configure Sysprep in a MED-V workspace</span></span>**

1.  <span data-ttu-id="80a8e-189">Создайте каталог в корневом каталоге системного диска с именем *Sysprep*.</span><span class="sxs-lookup"><span data-stu-id="80a8e-189">Create a directory in the root of the system drive named *Sysprep*.</span></span>

2.  <span data-ttu-id="80a8e-190">С установочного компакт-диска Windows извлеките *deploy.cab* в корневой каталог системного диска или скачайте последнюю версию средств развертывания на веб-сайте Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="80a8e-190">From the Windows installation CD, extract *deploy.cab* to the root of the system drive, or download the latest Deployment Tools update from the Microsoft Web site.</span></span>

    -   <span data-ttu-id="80a8e-191">Для Windows 2000 в разделе [Обновление средств развертывания для windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span><span class="sxs-lookup"><span data-stu-id="80a8e-191">For Windows 2000, see [Deployment Tools update for Windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).</span></span>

    -   <span data-ttu-id="80a8e-192">В Windows XP можно найти в разделе [Обновление средств развертывания для Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span><span class="sxs-lookup"><span data-stu-id="80a8e-192">For Windows XP, see [Deployment Tools update for Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).</span></span>

3.  <span data-ttu-id="80a8e-193">Запустите **Диспетчер установки** (setupmgr.exe).</span><span class="sxs-lookup"><span data-stu-id="80a8e-193">Run **Setup Manager** (setupmgr.exe).</span></span>

4.  <span data-ttu-id="80a8e-194">Следуйте указаниям мастера настройки диспетчера установки.</span><span class="sxs-lookup"><span data-stu-id="80a8e-194">Follow the Setup Manager wizard.</span></span>

<span data-ttu-id="80a8e-195">После настройки Sysprep и создания рабочей области для MED-V необходимо выполнить Sysprep.</span><span class="sxs-lookup"><span data-stu-id="80a8e-195">After Sysprep is configured and the MED-V workspace is created, Sysprep must be executed.</span></span>

**<span data-ttu-id="80a8e-196">Запуск программы Sysprep</span><span class="sxs-lookup"><span data-stu-id="80a8e-196">To run Sysprep</span></span>**

1.  <span data-ttu-id="80a8e-197">В папке Sysprep, расположенной в корневом каталоге системного диска, запустите средство подготовки системы (Sysprep.exe).</span><span class="sxs-lookup"><span data-stu-id="80a8e-197">From the Sysprep folder located in the root of the system drive, run the System Preparation Tool (Sysprep.exe).</span></span>

2.  <span data-ttu-id="80a8e-198">В появившемся окне с предупреждением нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-198">In the warning message box that appears, click **OK**.</span></span>

3.  <span data-ttu-id="80a8e-199">В диалоговом окне **Параметры Sysprep** установите флажок **не сбрасывать льготный период для активации** и **Используйте мини-установку** .</span><span class="sxs-lookup"><span data-stu-id="80a8e-199">In the **Sysprep Properties** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes.</span></span>

4.  <span data-ttu-id="80a8e-200">Нажмите кнопку " **запечатать**".</span><span class="sxs-lookup"><span data-stu-id="80a8e-200">Click **Reseal**.</span></span>

5.  <span data-ttu-id="80a8e-201">Если вы не удовлетворены данными, указанными в появившемся диалоговом окне подтверждения, нажмите кнопку **Отмена** и измените параметры.</span><span class="sxs-lookup"><span data-stu-id="80a8e-201">If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and change the selections.</span></span>

6.  <span data-ttu-id="80a8e-202">Нажмите кнопку **ОК** , чтобы завершить процесс подготовки системы.</span><span class="sxs-lookup"><span data-stu-id="80a8e-202">Click **OK** to complete the system preparation process.</span></span>

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a><span data-ttu-id="80a8e-203">Отключение Microsoft Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80a8e-203">Turning Off Microsoft Virtual PC</span></span>


<span data-ttu-id="80a8e-204">После того как все компоненты будут установлены и настроены, закройте Virtual PC (Майкрософт) и выберите **Отключить**.</span><span class="sxs-lookup"><span data-stu-id="80a8e-204">After all the components are installed and configured, close Microsoft Virtual PC and select **Turn Off**.</span></span>

## <span data-ttu-id="80a8e-205">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="80a8e-205">Related topics</span></span>


<span data-ttu-id="80a8e-206">Создание образа MED-V [Настройка действий сценария](how-to-set-up-script-actions.md)</span><span class="sxs-lookup"><span data-stu-id="80a8e-206">Creating a MED-V Image [How to Set Up Script Actions](how-to-set-up-script-actions.md)</span></span>









