---
title: Создание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))
description: Создание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))
author: dansimp
ms.assetid: 585e692e-cebb-48ac-93ab-b2e7eb7ae7ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eb806ccf04fcd5ae7db87c5de21e85217739fcbc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817639"
---
# <span data-ttu-id="218fc-103">Создание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="218fc-103">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="218fc-104">Вы можете использовать акселераторы пакетов App-V для автоматического создания нового пакета виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="218fc-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="218fc-105">После того как вы успешно создадите ускоритель пакетов, вы можете повторно использовать ускоритель пакетов и предоставить к нему общий доступ.</span><span class="sxs-lookup"><span data-stu-id="218fc-105">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="218fc-106">Дополнительные сведения о ускорителях пакетов смотрите в разделе [ускорители пакетов App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="218fc-106">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span> <span data-ttu-id="218fc-107">Создание ускорителей пакетов App-V является сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="218fc-107">Creating App-V Package Accelerators is an advanced task.</span></span> <span data-ttu-id="218fc-108">Ускорители пакетов могут содержать пароль и сведения для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="218fc-108">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="218fc-109">Поэтому вы должны сохранить ускорители пакетов и соответствующий установочный носитель в безопасном расположении, и вы должны добавить цифровую подпись ускорителя пакетов после его создания, чтобы издатель мог быть проверен при применении ускорителя пакетов App-V.</span><span class="sxs-lookup"><span data-stu-id="218fc-109">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V Package Accelerator is applied.</span></span>

<span data-ttu-id="218fc-110">В некоторых случаях для создания ускорителя пакетов может потребоваться установить локальное приложение на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="218fc-110">In some situations, to create the Package Accelerator, you might have to install the application locally on the computer running the Sequencer.</span></span> <span data-ttu-id="218fc-111">Сначала попытайтесь создать ускоритель пакетов с помощью установочного носителя и, если требуется, нужно установить приложение локально на компьютер под управлением секвенсора, а затем создать ускоритель пакетов.</span><span class="sxs-lookup"><span data-stu-id="218fc-111">First try to create the Package Accelerator by using the installation media, and if there are a number of missing files that are required, install the application locally to the computer running the Sequencer, and then create the Package Accelerator.</span></span>

**<span data-ttu-id="218fc-112">Важно.</span><span class="sxs-lookup"><span data-stu-id="218fc-112">Important</span></span>**  
<span data-ttu-id="218fc-113">Прежде чем приступить к описанной ниже процедуре, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="218fc-113">Before you begin the following procedure, you should do the following:</span></span>

-   <span data-ttu-id="218fc-114">Скопируйте пакет виртуального приложения, который необходимо использовать для локального создания ускорителя пакетов, на компьютере с запущенным секвенсором.</span><span class="sxs-lookup"><span data-stu-id="218fc-114">Copy the virtual application package that you must use to create the Package Accelerator locally to the computer running the Sequencer.</span></span>

-   <span data-ttu-id="218fc-115">Скопируйте все необходимые файлы установки, связанные с виртуальным пакетом приложения, на компьютер, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="218fc-115">Copy all required installation files associated with the virtual application package to the computer running the Sequencer.</span></span>



**<span data-ttu-id="218fc-116">Важно.</span><span class="sxs-lookup"><span data-stu-id="218fc-116">Important</span></span>**  
<span data-ttu-id="218fc-117">Заявление об отказе: Microsoft Application Virtualization Sequencer не предоставляет вам никаких прав на лицензирование программного приложения, которое вы используете для создания ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="218fc-117">Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="218fc-118">Вы обязаны соблюдать все условия лицензии конечных пользователей для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="218fc-118">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="218fc-119">Ответственность за то, что условия лицензионного соглашения на использование программного обеспечения позволяют создать пакетный ускоритель с помощью Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="218fc-119">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="218fc-120">Создание ускорителя пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="218fc-120">To create an App-V Package Accelerator</span></span>**

1.  <span data-ttu-id="218fc-121">Чтобы запустить секвенсор App-v на компьютере, на котором работает секвенсор App-v, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="218fc-121">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="218fc-122">Чтобы запустить мастер **создания ускорителя** работы с приложением App-v, в секвенсоре App-v выберите **инструменты**  /  **Создать ускоритель пакетов**.</span><span class="sxs-lookup"><span data-stu-id="218fc-122">To start the App-V **Create Package Accelerator** wizard, in the App-V Sequencer, click **Tools** / **Create Package Accelerator**.</span></span>

3.  <span data-ttu-id="218fc-123">На странице **Выбор пакета** , чтобы указать существующий виртуальный пакет приложения, который будет использоваться для создания ускорителя пакетов, нажмите кнопку **Обзор**и найдите существующий пакет виртуального приложения (SPRJ-файл).</span><span class="sxs-lookup"><span data-stu-id="218fc-123">On the **Select Package** page, to specify an existing virtual application package to use to create the Package Accelerator, click **Browse**, and locate the existing virtual application package (.sprj file).</span></span>

    **<span data-ttu-id="218fc-124">Совет</span><span class="sxs-lookup"><span data-stu-id="218fc-124">Tip</span></span>**  
    <span data-ttu-id="218fc-125">Скопируйте файлы, связанные с виртуальным пакетом приложений, который вы планируете использовать локально, на компьютере с программой Sequencer.</span><span class="sxs-lookup"><span data-stu-id="218fc-125">Copy the files associated with the virtual application package you plan to use locally to the computer running the Sequencer.</span></span>



~~~
Click **Next**.
~~~

4. <span data-ttu-id="218fc-126">На странице **установочные файлы** , чтобы указать папку, содержащую установочные файлы, которые вы использовали для создания исходного пакета виртуального приложения, нажмите кнопку **Обзор**и выберите каталог, содержащий установочные файлы.</span><span class="sxs-lookup"><span data-stu-id="218fc-126">On the **Installation Files** page, to specify the folder that contains the installation files that you used to create the original virtual application package, click **Browse**, and then select the directory that contains the installation files.</span></span>

   **<span data-ttu-id="218fc-127">Совет</span><span class="sxs-lookup"><span data-stu-id="218fc-127">Tip</span></span>**  
   <span data-ttu-id="218fc-128">Скопируйте папку, содержащую необходимые файлы установки, на компьютер, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="218fc-128">Copy the folder that contains the required installation files to the computer running the Sequencer.</span></span>



~~~
If the application is already installed on the computer running the Sequencer, to specify the installation file, select **Files installed on local system**. To use this option, the application must already be installed in the default installation location.
~~~

5. <span data-ttu-id="218fc-129">На странице **сведения о** собрании проверьте файлы, которые не были найдены в расположении, указанном на странице **установочные файлы** этого мастера.</span><span class="sxs-lookup"><span data-stu-id="218fc-129">On the **Gathering Information** page, review the files that were not found in the location specified on the **Installation Files** page of this wizard.</span></span> <span data-ttu-id="218fc-130">Если отображаемые файлы не требуются, выберите **удалить эти файлы**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="218fc-130">If the files displayed are not required, select **Remove these files**, and then click **Next**.</span></span> <span data-ttu-id="218fc-131">Если нужные файлы, нажмите кнопку **назад** и скопируйте необходимые файлы в каталог, указанный на странице **файлы установки** .</span><span class="sxs-lookup"><span data-stu-id="218fc-131">If the files are required, click **Previous** and copy the required files to the directory specified on the **Installation Files** page.</span></span>

   **<span data-ttu-id="218fc-132">Примечание.</span><span class="sxs-lookup"><span data-stu-id="218fc-132">Note</span></span>**  
   <span data-ttu-id="218fc-133">Чтобы перейти к следующей странице мастера, необходимо удалить ненужные файлы или нажать кнопку **назад** и найти нужные файлы.</span><span class="sxs-lookup"><span data-stu-id="218fc-133">You must either remove the unrequired files, or click **Previous** and locate the required files to advance to the next page of this wizard.</span></span>



6. <span data-ttu-id="218fc-134">На странице **Выбор файлов** внимательно проверьте найденные файлы и удалите все файлы, которые нужно удалить из ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="218fc-134">On the **Select Files** page, carefully review the files that were detected, and clear any file that should be removed from the Package Accelerator.</span></span> <span data-ttu-id="218fc-135">Выберите только файлы, необходимые для успешного запуска приложения, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="218fc-135">Select only files that are required for the application to run successfully, and then click **Next**.</span></span>

7. <span data-ttu-id="218fc-136">На странице **Проверка приложений** убедитесь, что все установочные файлы, необходимые для сборки пакета, отображены.</span><span class="sxs-lookup"><span data-stu-id="218fc-136">On the **Verify Applications** page, confirm that all installation files that are required to build the package are displayed.</span></span> <span data-ttu-id="218fc-137">При использовании ускорителя пакетов для создания нового пакета все файлы установки, отображаемые в области **приложения** , должны быть созданы для создания пакета.</span><span class="sxs-lookup"><span data-stu-id="218fc-137">When the Package Accelerator is used to create a new package, all installation files displayed in the **Applications** pane are required to create the package.</span></span>

   <span data-ttu-id="218fc-138">При необходимости добавьте дополнительные файлы установщика и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="218fc-138">If necessary, to add additional Installer files, click **Add**.</span></span> <span data-ttu-id="218fc-139">Чтобы удалить ненужные файлы установки, выберите файл установщика и нажмите кнопку **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="218fc-139">To remove unnecessary installation files, select the Installer file, and then click **Delete**.</span></span> <span data-ttu-id="218fc-140">Чтобы изменить свойства, связанные с установщиком, нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="218fc-140">To edit the properties associated with an installer, click **Edit**.</span></span> <span data-ttu-id="218fc-141">Файлы установки, указанные в этом шаге, потребуются, когда ускоритель пакетов используется для создания нового виртуального пакета приложений.</span><span class="sxs-lookup"><span data-stu-id="218fc-141">The installation files specified in this step will be required when the Package Accelerator is used to create a new virtual application package.</span></span> <span data-ttu-id="218fc-142">После подтверждения появления данных нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="218fc-142">After you have confirmed the information displayed, click **Next**.</span></span>

8. <span data-ttu-id="218fc-143">На странице **выберите руководство** , чтобы указать файл, содержащий сведения о том, как ускоритель пакетов, нажмите кнопку **Обзор**.</span><span class="sxs-lookup"><span data-stu-id="218fc-143">On the **Select Guidance** page, to specify a file that contains information about how the Package Accelerator, click **Browse**.</span></span> <span data-ttu-id="218fc-144">Например, этот файл может содержать сведения о том, как настроить компьютер, на котором работает программа Sequencer, сведения о предварительной версии приложения для целевых компьютеров и общие заметки.</span><span class="sxs-lookup"><span data-stu-id="218fc-144">For example, this file can contain information about how the computer running the Sequencer should be configured, application prerequisite information for target computers, and general notes.</span></span> <span data-ttu-id="218fc-145">Необходимо предоставить все необходимые сведения о том, что ускоритель пакетов будет успешно применен.</span><span class="sxs-lookup"><span data-stu-id="218fc-145">You should provide all required information for the Package Accelerator to be successfully applied.</span></span> <span data-ttu-id="218fc-146">Выбранный файл должен иметь формат форматированного текста (RTF) или текстовый файл (txt).</span><span class="sxs-lookup"><span data-stu-id="218fc-146">The file you select must be in rich text (.rtf) or text file (.txt) format.</span></span> <span data-ttu-id="218fc-147">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="218fc-147">Click **Next**.</span></span>

9. <span data-ttu-id="218fc-148">На странице " **Создание ускорителя пакетов** ", чтобы указать, где нужно сохранить ускоритель пакетов, нажмите кнопку **Обзор** и выберите каталог.</span><span class="sxs-lookup"><span data-stu-id="218fc-148">On the **Create Package Accelerator** page, to specify where to save the Package Accelerator, click **Browse** and select the directory.</span></span>

10. <span data-ttu-id="218fc-149">На странице **завершения** нажмите кнопку **Закрыть**, чтобы закрыть мастер **создания ускорителя пакетов** .</span><span class="sxs-lookup"><span data-stu-id="218fc-149">On the **Completion** page, to close the **Create Package Accelerator** wizard, click **Close**.</span></span>

   **<span data-ttu-id="218fc-150">Важно.</span><span class="sxs-lookup"><span data-stu-id="218fc-150">Important</span></span>**  
   <span data-ttu-id="218fc-151">Чтобы обеспечить максимально надежную защиту ускорителя пакетов и так, чтобы издатель мог быть проверен при применении ускорителя пакетов, следует всегда ставить цифровую подпись ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="218fc-151">To help ensure that the Package Accelerator is as secure as possible, and so that the publisher can be verified when the Package Accelerator is applied, you should always digitally sign the Package Accelerator.</span></span>



## <span data-ttu-id="218fc-152">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="218fc-152">Related topics</span></span>


<span data-ttu-id="218fc-153">Настройка Application Virtualization Sequencer (App-V 4,6 SP1) [применение ускорителя пакетов для создания виртуального пакета приложения (App-v 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span><span class="sxs-lookup"><span data-stu-id="218fc-153">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1) [How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)</span></span>









