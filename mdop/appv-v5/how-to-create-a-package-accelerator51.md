---
title: Как создать акселератор пакетов
description: Как создать акселератор пакетов
author: dansimp
ms.assetid: b61f3581-7933-443e-b872-a96bed9ff8d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6893f2e9bb9db473d285026015c3399fb0074015
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814264"
---
# <span data-ttu-id="e141e-103">Как создать акселератор пакетов</span><span class="sxs-lookup"><span data-stu-id="e141e-103">How to Create a Package Accelerator</span></span>


<span data-ttu-id="e141e-104">Ускорители пакетов приложений для App-V 5,1 автоматически создают новые пакеты виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="e141e-104">App-V 5.1 package accelerators automatically generate new virtual application packages.</span></span>

**<span data-ttu-id="e141e-105">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e141e-105">Note</span></span>**  
<span data-ttu-id="e141e-106">Вы можете использовать PowerShell для создания ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="e141e-106">You can use PowerShell to create a package accelerator.</span></span> <span data-ttu-id="e141e-107">Дополнительные сведения можно найти [в разделе Создание ускорителя пакетов с помощью PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).</span><span class="sxs-lookup"><span data-stu-id="e141e-107">For more information see [How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md).</span></span>



<span data-ttu-id="e141e-108">Для создания ускорителя пакетов выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e141e-108">Use the following procedure to create a package accelerator.</span></span>

**<span data-ttu-id="e141e-109">Важно.</span><span class="sxs-lookup"><span data-stu-id="e141e-109">Important</span></span>**  
<span data-ttu-id="e141e-110">Ускорители пакетов могут содержать пароль и сведения для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="e141e-110">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="e141e-111">Поэтому вы должны сохранить ускорители пакетов и связанный установочный носитель в безопасном расположении, и вы должны добавить цифровую подпись ускорителя пакетов после его создания, чтобы издатель мог быть проверен при применении ускорителя приложений App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="e141e-111">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.1 Package Accelerator is applied.</span></span>



**<span data-ttu-id="e141e-112">Важно.</span><span class="sxs-lookup"><span data-stu-id="e141e-112">Important</span></span>**  
<span data-ttu-id="e141e-113">Прежде чем приступить к описанной ниже процедуре, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e141e-113">Before you begin the following procedure, you should perform the following:</span></span>

-   <span data-ttu-id="e141e-114">Скопируйте виртуальный пакет приложения, который будет использоваться для создания ускорителя пакетов на компьютере с программой Sequencer.</span><span class="sxs-lookup"><span data-stu-id="e141e-114">Copy the virtual application package that you will use to create the package accelerator locally to the computer running the sequencer.</span></span>

-   <span data-ttu-id="e141e-115">Скопируйте все необходимые файлы установки, связанные с виртуальным пакетом приложения, на компьютер, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="e141e-115">Copy all required installation files associated with the virtual application package to the computer running the sequencer.</span></span>



**<span data-ttu-id="e141e-116">Создание ускорителя пакетов</span><span class="sxs-lookup"><span data-stu-id="e141e-116">To create a package accelerator</span></span>**

1.  **<span data-ttu-id="e141e-117">Важно.</span><span class="sxs-lookup"><span data-stu-id="e141e-117">Important</span></span>**  
    <span data-ttu-id="e141e-118">Приложение App-V 5,1 не предоставляет никаких прав лицензии на программное обеспечение, которое вы используете для создания ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="e141e-118">The App-V 5.1 Sequencer does not grant any license rights to the software application you are using to create the Package Accelerator.</span></span> <span data-ttu-id="e141e-119">Вы должны соблюдать все условия лицензионного соглашения конечного пользователя для используемой программы.</span><span class="sxs-lookup"><span data-stu-id="e141e-119">You must abide by all end user license terms for the application you are using.</span></span> <span data-ttu-id="e141e-120">Ответственность за то, что условия лицензионного соглашения на использование программного обеспечения позволяют создать пакетный ускоритель с помощью приложения Application-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="e141e-120">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using App-V 5.1 Sequencer.</span></span>



~~~
To start the App-V 5.1 sequencer, on the computer that is running the sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.
~~~

2. <span data-ttu-id="e141e-121">Чтобы запустить мастер **создания ускорителя** приложений для App-v 5,1, в консоли App-v 5,1 выберите пункт **инструменты**  /  **Создать ускоритель**.</span><span class="sxs-lookup"><span data-stu-id="e141e-121">To start the App-V 5.1 **Create Package Accelerator** wizard, in the App-V 5.1 sequencer console, click **Tools** / **Create Accelerator**.</span></span>

3. <span data-ttu-id="e141e-122">На странице **Выбор пакета** , чтобы указать существующий виртуальный пакет приложения, который будет использоваться для создания ускорителя пакетов, нажмите кнопку **Обзор**и найдите существующий пакет виртуального приложения (файл. AppV).</span><span class="sxs-lookup"><span data-stu-id="e141e-122">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.appv file).</span></span>

   **<span data-ttu-id="e141e-123">Совет</span><span class="sxs-lookup"><span data-stu-id="e141e-123">Tip</span></span>**  
   <span data-ttu-id="e141e-124">Скопируйте файлы, связанные с виртуальным пакетом приложений, который вы планируете использовать локально, на компьютере с программой Sequencer.</span><span class="sxs-lookup"><span data-stu-id="e141e-124">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="e141e-125">На странице **установочные файлы** , чтобы указать папку, содержащую установочные файлы, которые вы использовали для создания исходного пакета виртуального приложения, нажмите кнопку **Обзор**и выберите каталог, содержащий установочные файлы.</span><span class="sxs-lookup"><span data-stu-id="e141e-125">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="e141e-126">Совет</span><span class="sxs-lookup"><span data-stu-id="e141e-126">Tip</span></span>**  
   <span data-ttu-id="e141e-127">Скопируйте папку, содержащую необходимые файлы установки, на компьютер, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="e141e-127">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



5. <span data-ttu-id="e141e-128">Если приложение уже установлено на компьютере, на котором запущен секвенсор, чтобы указать установочный файл, выберите пункт **файлы, установленные на локальном компьютере**.</span><span class="sxs-lookup"><span data-stu-id="e141e-128">If the application is already installed on the computer running the sequencer, to specify the installation file, select **Files installed on local system**.</span></span> <span data-ttu-id="e141e-129">Чтобы использовать этот параметр, приложение должно быть уже установлено в папке, используемой по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e141e-129">To use this option, the application must already be installed in the default installation location.</span></span>

6. <span data-ttu-id="e141e-130">На странице **сведения о** собрании проверьте файлы, которые не были найдены в расположении, указанном на странице **установочные файлы** этого мастера.</span><span class="sxs-lookup"><span data-stu-id="e141e-130">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="e141e-131">Если отображаемые файлы не требуются, выберите **удалить эти файлы**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e141e-131">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="e141e-132">Если нужные файлы, нажмите кнопку **назад** и скопируйте необходимые файлы в каталог, указанный на странице **файлы установки** .</span><span class="sxs-lookup"><span data-stu-id="e141e-132">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="e141e-133">Примечание.</span><span class="sxs-lookup"><span data-stu-id="e141e-133">Note</span></span>**  
   <span data-ttu-id="e141e-134">Чтобы перейти к следующей странице мастера, необходимо удалить ненужные файлы или нажать кнопку **назад** и найти нужные файлы.</span><span class="sxs-lookup"><span data-stu-id="e141e-134">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



7. <span data-ttu-id="e141e-135">На странице **Выбор файлов** внимательно проверьте найденные файлы и удалите все файлы, которые нужно удалить из ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="e141e-135">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the package accelerator.</span></span> <span data-ttu-id="e141e-136">Выберите только файлы, необходимые для успешного запуска приложения, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e141e-136">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

8. <span data-ttu-id="e141e-137">На странице **Проверка приложений** убедитесь, что все установочные файлы, необходимые для сборки пакета, отображены.</span><span class="sxs-lookup"><span data-stu-id="e141e-137">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="e141e-138">При использовании ускорителя пакетов для создания нового пакета все файлы установки, отображаемые в области **приложения** , должны быть созданы для создания пакета.</span><span class="sxs-lookup"><span data-stu-id="e141e-138">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="e141e-139">При необходимости добавьте дополнительные файлы установщика и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="e141e-139">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="e141e-140">Чтобы удалить ненужные файлы установки, выберите файл установщика и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="e141e-140">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="e141e-141">Чтобы изменить свойства, связанные с установщиком, нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="e141e-141">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="e141e-142">Файлы установки, указанные в этом шаге, потребуются, когда ускоритель пакетов используется для создания нового виртуального пакета приложений.</span><span class="sxs-lookup"><span data-stu-id="e141e-142">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="e141e-143">После подтверждения появления данных нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e141e-143">After you have confirmed the information displayed, click **Next**.</span></span>

9. <span data-ttu-id="e141e-144">На странице **выберите руководство** , чтобы указать файл, содержащий сведения о том, как ускоритель пакетов, нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="e141e-144">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="e141e-145">Например, этот файл может содержать сведения о том, как настроить компьютер, на котором работает программа Sequencer, сведения о предварительной версии приложения для целевых компьютеров и общие заметки.</span><span class="sxs-lookup"><span data-stu-id="e141e-145">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="e141e-146">Необходимо предоставить все необходимые сведения о том, что ускоритель пакетов будет успешно применен.</span><span class="sxs-lookup"><span data-stu-id="e141e-146">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="e141e-147">Выбранный файл должен иметь формат форматированного текста (RTF) или текстовый файл (txt).</span><span class="sxs-lookup"><span data-stu-id="e141e-147">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="e141e-148">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e141e-148">Click **Next**.</span></span>

10. <span data-ttu-id="e141e-149">На странице " **Создание ускорителя пакетов** ", чтобы указать, где нужно сохранить ускоритель пакетов, нажмите кнопку **Обзор** и выберите каталог.</span><span class="sxs-lookup"><span data-stu-id="e141e-149">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

11. <span data-ttu-id="e141e-150">На странице **завершения** нажмите кнопку **Закрыть**, чтобы закрыть мастер **создания ускорителя пакетов** .</span><span class="sxs-lookup"><span data-stu-id="e141e-150">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="e141e-151">Важно.</span><span class="sxs-lookup"><span data-stu-id="e141e-151">Important</span></span>**  
   <span data-ttu-id="e141e-152">Чтобы обеспечить максимально надежную защиту ускорителя пакетов и так, чтобы издатель мог быть проверен при применении ускорителя пакетов, следует всегда ставить цифровую подпись ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="e141e-152">To help ensure that the package accelerator is as secure as possible, and so that the publisher can be verified when the package accelerator is applied, you should always digitally sign the package accelerator.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="e141e-153">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e141e-153">Related topics</span></span>


[<span data-ttu-id="e141e-154">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e141e-154">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="e141e-155">Создание пакета виртуального приложения с помощью ускорителя пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="e141e-155">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md)









