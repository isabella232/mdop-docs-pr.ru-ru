---
title: Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)
description: Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)
author: dansimp
ms.assetid: ca0bd514-2bbf-4130-8c77-98d991cbe016
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce6960fb95cce7f5e0eeb111412f27f945b0c1a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821382"
---
# <span data-ttu-id="bf908-103">Применение ускорителя пакетов для создания виртуального пакета приложения (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="bf908-103">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>


<span data-ttu-id="bf908-104">Вы можете использовать акселераторы пакетов App-V для автоматического создания нового пакета виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="bf908-104">You can use App-V Package Accelerators to automatically generate a new virtual application package.</span></span> <span data-ttu-id="bf908-105">Дополнительные сведения о ускорителях пакетов смотрите в разделе [ускорители пакетов App-v (App-v 4,6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="bf908-105">For more information about Package Accelerators, see [About App-V Package Accelerators (App-V 4.6 SP1)](about-app-v-package-accelerators--app-v-46-sp1-.md).</span></span>

**<span data-ttu-id="bf908-106">Важно.</span><span class="sxs-lookup"><span data-stu-id="bf908-106">Important</span></span>**  
<span data-ttu-id="bf908-107">Заявление об отказе: Программа Application Virtualization Sequencer не предоставляет вам никаких прав лицензии на программное приложение, которое вы используете для создания ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="bf908-107">Disclaimer: The Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="bf908-108">Вы обязаны соблюдать все условия лицензии конечных пользователей для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="bf908-108">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="bf908-109">Ответственность за то, что условия лицензионного соглашения на использование программного обеспечения позволяют создать пакетный ускоритель с помощью Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="bf908-109">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>



**<span data-ttu-id="bf908-110">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bf908-110">Note</span></span>**  
<span data-ttu-id="bf908-111">Прежде чем приступать к этой процедуре, скопируйте требуемый ускоритель пакетов локально на компьютер с секвенсором App-V.</span><span class="sxs-lookup"><span data-stu-id="bf908-111">Before starting this procedure, copy the required Package Accelerator locally to the computer running the App-V Sequencer.</span></span> <span data-ttu-id="bf908-112">Кроме того, необходимо скопировать все необходимые файлы установки для пакета в локальный каталог на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="bf908-112">You should also copy all required installation files for the package to a local directory on the computer running the Sequencer.</span></span> <span data-ttu-id="bf908-113">Это каталог, который нужно задать в действии 5 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="bf908-113">This is the directory that you have to specify in step 5 of this procedure.</span></span>



<span data-ttu-id="bf908-114">Чтобы создать виртуальный пакет приложения с помощью ускорителя пакетов, выполните описанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="bf908-114">Use the following procedure to create a virtual application package by using a Package Accelerator.</span></span>

**<span data-ttu-id="bf908-115">Создание виртуального пакета приложения с помощью ускорителя пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="bf908-115">To create a virtual application package by using an App-V Package Accelerator</span></span>**

1. <span data-ttu-id="bf908-116">Чтобы запустить секвенсор App-v на компьютере, на котором работает секвенсор App-v, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft**Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="bf908-116">To start the App-V Sequencer, on the computer that is running the App-V Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2. <span data-ttu-id="bf908-117">Чтобы запустить **Мастер создания пакета**, нажмите **создать новый виртуальный пакет приложения**.</span><span class="sxs-lookup"><span data-stu-id="bf908-117">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="bf908-118">Чтобы создать пакет, установите флажок **создать пакет с помощью ускорителя пакетов** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-118">To create the package, select the **Create Package using a Package Accelerator** check box, and then click **Next**.</span></span>

3. <span data-ttu-id="bf908-119">На странице **Выбор ускорителя пакетов** , чтобы указать ускоритель пакетов, который будет использоваться для создания нового виртуального пакета приложений, нажмите кнопку **Обзор** , чтобы найти ускоритель пакетов, который вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="bf908-119">On the **Select Package Accelerator** page, to specify the Package Accelerator that will be used to create the new virtual application package, click **Browse** to locate the Package Accelerator that you want to use.</span></span> <span data-ttu-id="bf908-120">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-120">Click **Next**.</span></span>

   **<span data-ttu-id="bf908-121">Важно.</span><span class="sxs-lookup"><span data-stu-id="bf908-121">Important</span></span>**  
   <span data-ttu-id="bf908-122">Если издатель ускорителя пакетов не может пройти проверку и не содержит действительной цифровой подписи, в диалоговом окне **предупреждение системы безопасности** перед нажатием кнопки **выполнить**необходимо подтвердить, что вы доверяете источнику ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="bf908-122">If the publisher of the Package Accelerator cannot be verified and does not contain a valid digital signature, in the **Security Warning** dialog box, you must confirm that you trust the source of the Package Accelerator before you click **Run**.</span></span>



4. <span data-ttu-id="bf908-123">На странице " **руководство** " Проверьте сведения о публикации, отображаемые в области сведений.</span><span class="sxs-lookup"><span data-stu-id="bf908-123">On the **Guidance** page, review the publishing guidance information displayed in the information pane.</span></span> <span data-ttu-id="bf908-124">Отображаемые сведения были добавлены при создании ускорителя пакетов и содержат сведения о создании и публикации пакета.</span><span class="sxs-lookup"><span data-stu-id="bf908-124">The information displayed was added when the Package Accelerator was created and contains information about creating and publishing the package.</span></span> <span data-ttu-id="bf908-125">Чтобы экспортировать сведения о руководстве в текстовый файл (txt), нажмите кнопку **Экспорт** и укажите расположение, в котором нужно сохранить файл, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-125">To export the guidance information to a text (.txt) file, click **Export** and specify the location where the file should be saved, and then click **Next**.</span></span>

5. <span data-ttu-id="bf908-126">На странице " **Выбор установочных файлов** ", чтобы создать локальную папку, которая включает все необходимые файлы для установки пакета, щелкните **создать папку** и укажите, где следует сохранить папку.</span><span class="sxs-lookup"><span data-stu-id="bf908-126">On the **Select Installation Files** page, to create a local folder that contains all required installation files for the package, click **Make New Folder** and specify where the folder should be saved.</span></span> <span data-ttu-id="bf908-127">Кроме того, необходимо указать имя, которое будет назначаться папке.</span><span class="sxs-lookup"><span data-stu-id="bf908-127">You must also specify a name to be assigned to the folder.</span></span> <span data-ttu-id="bf908-128">Затем необходимо скопировать все необходимые файлы установки в указанное вами расположение.</span><span class="sxs-lookup"><span data-stu-id="bf908-128">You must then copy all required installation files to the location that you specified.</span></span> <span data-ttu-id="bf908-129">Если папка, содержащая установочные файлы, уже есть на компьютере с секвенсором, нажмите кнопку **Обзор** , чтобы выбрать папку.</span><span class="sxs-lookup"><span data-stu-id="bf908-129">If the folder that contains the installation files already exists on the computer running the Sequencer, click **Browse** to select the folder.</span></span>

   <span data-ttu-id="bf908-130">Кроме того, если вы уже скопировали файлы установки в каталог на этом компьютере, щелкните **создать папку**, перейдите в папку, содержащую установочные файлы, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-130">Alternatively, if you have already copied the installation files to a directory on this computer, click **Make New Folder**, browse to the folder that contains the installation files, and then click **Next**.</span></span>

   **<span data-ttu-id="bf908-131">Примечание.</span><span class="sxs-lookup"><span data-stu-id="bf908-131">Note</span></span>**  
   <span data-ttu-id="bf908-132">Вы можете указать следующие типы файлов, которые поддерживаются при установке:</span><span class="sxs-lookup"><span data-stu-id="bf908-132">You can specify the following types of supported installation files:</span></span>

   -   <span data-ttu-id="bf908-133">Файлы установщика Windows (**MSI** -файл)</span><span class="sxs-lookup"><span data-stu-id="bf908-133">Windows Installer files(**.msi**</span></span>

   -   <span data-ttu-id="bf908-134">файлы. cab</span><span class="sxs-lookup"><span data-stu-id="bf908-134">.cab files</span></span>

   -   <span data-ttu-id="bf908-135">Сжатые файлы с расширением имени ZIP-файла</span><span class="sxs-lookup"><span data-stu-id="bf908-135">Compressed files with a .zip file name extension</span></span>

   -   <span data-ttu-id="bf908-136">Файлы реальных приложений</span><span class="sxs-lookup"><span data-stu-id="bf908-136">The actual application files</span></span>

   <span data-ttu-id="bf908-137">Следующие типы файлов не поддерживаются: **MSP** и <strong> exe </strong> .</span><span class="sxs-lookup"><span data-stu-id="bf908-137">The following file types are not supported: **.msp** and<strong>.exe</strong> files.</span></span> <span data-ttu-id="bf908-138">Если указан **exe** файл, необходимо извлечь установочные файлы вручную.</span><span class="sxs-lookup"><span data-stu-id="bf908-138">If you specify an **.exe** file you must extract the installation files manually.</span></span>



~~~
If the Package Accelerator requires an application be installed prior to applying the Package Accelerator and you have installed the application, on the **Local Installation** page, select the check box **I have installed all applications**, and then click **Next**.
~~~

6. <span data-ttu-id="bf908-139">На странице **имя пакета** укажите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="bf908-139">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="bf908-140">Указанное имя идентифицирует пакет в консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="bf908-140">The name specified identifies the package in the App-V Management Console.</span></span> <span data-ttu-id="bf908-141">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-141">Click **Next**.</span></span>

7. <span data-ttu-id="bf908-142">На странице " **Создание пакета** " Введите примечания, которые будут связаны с пакетом.</span><span class="sxs-lookup"><span data-stu-id="bf908-142">On the **Create Package** page, provide comments that will be associated with the package.</span></span> <span data-ttu-id="bf908-143">Примечания должны содержать идентификационные данные о создаваемом пакете.</span><span class="sxs-lookup"><span data-stu-id="bf908-143">The comments should contain identifying information about the package you are creating.</span></span> <span data-ttu-id="bf908-144">Для подтверждения места создания пакета ознакомьтесь со сведениями, которые отображаются в папке для **сохранения**.</span><span class="sxs-lookup"><span data-stu-id="bf908-144">To confirm the location where the package is created, review the information displayed in **Save Location**.</span></span> <span data-ttu-id="bf908-145">Чтобы сжать пакет, выберите пункт **сжать пакет**.</span><span class="sxs-lookup"><span data-stu-id="bf908-145">To compress the package, select **Compress Package**.</span></span> <span data-ttu-id="bf908-146">Установите флажок **сжимать пакет** , если пакет будет передаваться по сети или если размер пакета ПРЕВЫШАЕТ 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="bf908-146">Select the **Compress Package** check box if the package will be streamed across the network, or when the package size exceeds 4 GB.</span></span>

   <span data-ttu-id="bf908-147">Чтобы создать пакет, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="bf908-147">To create the package, click **Create**.</span></span> <span data-ttu-id="bf908-148">После создания пакета нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-148">After the package has been created, click **Next**.</span></span>

8. <span data-ttu-id="bf908-149">На странице " **Настройка программного обеспечения** " для включения секвенсора для настройки приложений, содержащихся в пакете, выберите пункт " **Настройка программного обеспечения**".</span><span class="sxs-lookup"><span data-stu-id="bf908-149">On the **Configure Software** page, to enable the Sequencer to configure the applications contained in the package, select **Configure Software**.</span></span> <span data-ttu-id="bf908-150">Этот шаг полезен для настройки связанных задач, которые должны быть выполнены для запуска приложения на конечных компьютерах, например для настройки каких – либо связанных лицензионных соглашений.</span><span class="sxs-lookup"><span data-stu-id="bf908-150">This step is useful for configuring any associated tasks that must be completed to run the application on target computers, such as configuring any associated license agreements.</span></span>

   <span data-ttu-id="bf908-151">Если выбрать параметр **настроить программное обеспечение**, то следующие элементы будут сконфигурированы секвенсором в рамках этого этапа:</span><span class="sxs-lookup"><span data-stu-id="bf908-151">If you select **Configure Software**, the following items are configured by the Sequencer as part of this step:</span></span>

   -   <span data-ttu-id="bf908-152">**Загрузить пакет**.</span><span class="sxs-lookup"><span data-stu-id="bf908-152">**Load Package**.</span></span> <span data-ttu-id="bf908-153">Программа Sequencer загружает файлы, связанные с пакетом.</span><span class="sxs-lookup"><span data-stu-id="bf908-153">The Sequencer loads the files associated with the package.</span></span> <span data-ttu-id="bf908-154">Декодирование пакета может занять от нескольких секунд до часа.</span><span class="sxs-lookup"><span data-stu-id="bf908-154">It can take several seconds to up to an hour to decode the package.</span></span>

   -   <span data-ttu-id="bf908-155">**Запустите каждую программу**.</span><span class="sxs-lookup"><span data-stu-id="bf908-155">**Run Each Program**.</span></span> <span data-ttu-id="bf908-156">При необходимости запустите программы, содержащиеся в пакете.</span><span class="sxs-lookup"><span data-stu-id="bf908-156">Optionally run the programs contained in the package.</span></span> <span data-ttu-id="bf908-157">Этот шаг полезен для завершения задач, связанных с лицензией или конфигурацией, которые необходимы для запуска приложения перед развертыванием и запуском пакета на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="bf908-157">This step is helpful for completing any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="bf908-158">Чтобы запустить все программы за один раз, выберите хотя бы одну программу, а затем нажмите кнопку **выполнить все**.</span><span class="sxs-lookup"><span data-stu-id="bf908-158">To run all the programs at one time, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="bf908-159">Чтобы запустить определенные программы, выберите программу или программы, которые вы хотите запустить, и нажмите кнопку **выполнить выбрано**.</span><span class="sxs-lookup"><span data-stu-id="bf908-159">To run specific programs, select the program or programs you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="bf908-160">Заполните необходимые задачи настройки, а затем закройте приложения.</span><span class="sxs-lookup"><span data-stu-id="bf908-160">Complete the required configuration tasks, and then close the applications.</span></span> <span data-ttu-id="bf908-161">Для запуска всех программ может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="bf908-161">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="bf908-162">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-162">Click **Next**.</span></span>

   -   <span data-ttu-id="bf908-163">**Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="bf908-163">**Save Package**.</span></span> <span data-ttu-id="bf908-164">Секвенсор сохраняет пакет.</span><span class="sxs-lookup"><span data-stu-id="bf908-164">The Sequencer saves the package.</span></span>

   -   <span data-ttu-id="bf908-165">**Основной блок функций**.</span><span class="sxs-lookup"><span data-stu-id="bf908-165">**Primary Feature Block**.</span></span> <span data-ttu-id="bf908-166">Секвенсор оптимизирует пакет для потоковой передачи, перестраивая основной блок функций.</span><span class="sxs-lookup"><span data-stu-id="bf908-166">The Sequencer optimizes the package for streaming by rebuilding the primary feature block.</span></span>

   <span data-ttu-id="bf908-167">Если вы не хотите настраивать приложения, нажмите **пропустить этот шаг**и перейдите к действию 9, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="bf908-167">If you do not want to configure the applications, click **Skip this step**, and to go to step 9 of this procedure, and then click **Next**.</span></span>

9. <span data-ttu-id="bf908-168">На странице **завершения** после просмотра данных, отображаемых в области **отчета "виртуальный пакет приложения** ", нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="bf908-168">On the **Completion** page, after you have reviewed the information displayed in the **Virtual Application Package Report** pane, click **Close**.</span></span>

   <span data-ttu-id="bf908-169">Пакет теперь доступен в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="bf908-169">The package is now available in the Sequencer.</span></span> <span data-ttu-id="bf908-170">Чтобы изменить свойства пакета, нажмите **изменить \ [имя пакета \]**.</span><span class="sxs-lookup"><span data-stu-id="bf908-170">To edit the package properties, click **Edit \[Package Name\]**.</span></span> <span data-ttu-id="bf908-171">Дополнительные сведения об изменении пакета можно найти в разделе [как изменить существующий пакет виртуального приложения (App-V 4,6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).</span><span class="sxs-lookup"><span data-stu-id="bf908-171">For more information about modifying a package, see [How to Modify an Existing Virtual Application Package (App-V 4.6 SP1)](how-to-modify-an-existing-virtual-application-package--app-v-46-sp1-.md).</span></span>

## <span data-ttu-id="bf908-172">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="bf908-172">Related topics</span></span>


[<span data-ttu-id="bf908-173">Настройка Application Virtualization Sequencer (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="bf908-173">Configuring the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)

[<span data-ttu-id="bf908-174">Создание ускорителей пакетов App-V (App-V 4.6 с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="bf908-174">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)









