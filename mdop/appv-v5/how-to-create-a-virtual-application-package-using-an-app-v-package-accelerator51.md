---
title: Создание пакета виртуального приложения с помощью ускорителя пакетов App-V
description: Создание пакета виртуального приложения с помощью ускорителя пакетов App-V
author: dansimp
ms.assetid: eae1e4f8-f14f-4bc8-9867-052561c37297
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 15376ae52a19b2d220f9ea0031f3ad5649ca487d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814272"
---
# <span data-ttu-id="f8b1d-103">Создание пакета виртуального приложения с помощью ускорителя пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="f8b1d-103">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>


**<span data-ttu-id="f8b1d-104">Важно.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-104">Important</span></span>**  
<span data-ttu-id="f8b1d-105">Приложение App-V 5,1 не предоставляет никаких прав лицензии на программное обеспечение, которое вы используете для создания ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-105">The App-V 5.1 Sequencer does not grant any license rights to the software application that you use to create the Package Accelerator.</span></span> <span data-ttu-id="f8b1d-106">Вы должны соблюдать все условия лицензионного соглашения конечного пользователя для используемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-106">You must abide by all end user license terms for the application that you use.</span></span> <span data-ttu-id="f8b1d-107">Ответственность за то, что условия лицензионного соглашения на использование программного обеспечения позволяют создать пакетный ускоритель с помощью приложения Application-V 5,1 Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-107">It is your responsibility to make sure that the software application’s license terms allow you to create a Package Accelerator with the App-V 5.1 Sequencer.</span></span>



<span data-ttu-id="f8b1d-108">Чтобы создать пакет виртуального приложения с ускорителем пакетов App-V 5,1, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-108">Use the following procedure to create a virtual application package with the App-V 5.1 Package Accelerator.</span></span>

**<span data-ttu-id="f8b1d-109">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-109">Note</span></span>**  
<span data-ttu-id="f8b1d-110">Прежде чем приступать к этой процедуре, скопируйте необходимый ускоритель пакетов на компьютер, на котором работает секвенсор App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-110">Before you start this procedure, copy the required Package Accelerator locally to the computer that runs the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="f8b1d-111">Кроме того, необходимо скопировать все необходимые файлы установки для пакета в локальный каталог на компьютере, на котором работает секвенсор.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-111">You should also copy all required installation files for the package to a local directory on the computer that runs the Sequencer.</span></span> <span data-ttu-id="f8b1d-112">Это каталог, который нужно задать в действии 5 этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-112">This is the directory that you have to specify in step 5 of this procedure.</span></span>



**<span data-ttu-id="f8b1d-113">Создание виртуального пакета приложения с ускорителем пакетов приложения App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="f8b1d-113">To create a virtual application package with an App-V 5.1 Package Accelerator</span></span>**

1.  <span data-ttu-id="f8b1d-114">Для запуска секвенсора App-v на компьютере, на котором работает секвенсор App-v 5,1, нажмите кнопку **запустить**  /  **все программы**  /  **Microsoft**Application Virtualization  /  **Sequencer Microsoft Applications**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-114">To start the App-V Sequencer, on the computer that runs the App-V 5.1 Sequencer, click **Start** / **All Programs** / **Microsoft Application Virtualization** / **Microsoft Application Virtualization Sequencer**.</span></span>

2.  <span data-ttu-id="f8b1d-115">Чтобы запустить **Мастер создания пакета**, нажмите **создать новый виртуальный пакет приложения**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-115">To start the **Create New Package Wizard**, click **Create a New Virtual Application Package**.</span></span> <span data-ttu-id="f8b1d-116">Чтобы создать пакет, установите флажок **создать пакет с помощью ускорителя пакетов** и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-116">To create the package, select the **Create Package using a Package Accelerator** check box, and then click **Next**.</span></span>

3.  <span data-ttu-id="f8b1d-117">Чтобы указать ускоритель пакетов, который будет использоваться для создания нового виртуального пакета приложения, нажмите кнопку **Обзор** на странице **Выбор ускорителя пакетов** .</span><span class="sxs-lookup"><span data-stu-id="f8b1d-117">To specify the package accelerator that will be used to create the new virtual application package, click **Browse** on the **Select Package Accelerator** page.</span></span> <span data-ttu-id="f8b1d-118">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-118">Click **Next**.</span></span>

    **<span data-ttu-id="f8b1d-119">Важно.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-119">Important</span></span>**  
    <span data-ttu-id="f8b1d-120">Если издатель ускорителя пакетов не может пройти проверку и не содержит действительной цифровой подписи, перед нажатием кнопки **выполнить**необходимо подтвердить, что вы доверяете источнику ускорителя пакетов.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-120">If the publisher of the package accelerator cannot be verified and does not contain a valid digital signature, then before you click **Run**, you must confirm that you trust the source of the package accelerator.</span></span> <span data-ttu-id="f8b1d-121">Подтвердите выбор в диалоговом окне " **предупреждение системы безопасности** ".</span><span class="sxs-lookup"><span data-stu-id="f8b1d-121">Confirm your choice in the **Security Warning** dialog box.</span></span>



4.  <span data-ttu-id="f8b1d-122">На странице " **руководство** " ознакомьтесь со сведениями о публикации, которые отображаются в области сведений.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-122">On the **Guidance** page, review the publishing guidance information that is displayed in the information pane.</span></span> <span data-ttu-id="f8b1d-123">Эта информация была добавлена при создании ускорителя пакетов и содержит руководство по созданию и публикации пакета.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-123">This information was added when the Package Accelerator was created and it contains guidance about how to create and publish the package.</span></span> <span data-ttu-id="f8b1d-124">Чтобы экспортировать сведения о руководстве в текстовый файл (txt), нажмите кнопку **Экспорт** и укажите расположение, в котором нужно сохранить файл, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-124">To export the guidance information to a text (.txt) file, click **Export** and specify the location where the file should be saved, and then click **Next**.</span></span>

5.  <span data-ttu-id="f8b1d-125">На странице **Выбор установочных файлов** выберите команду создать **папку** , чтобы создать локальную папку, содержащую все необходимые файлы установки пакета, и укажите, где следует сохранить папку.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-125">On the **Select Installation Files** page, click **Make New Folder** to create a local folder that contains all required installation files for the package, and specify where the folder should be saved.</span></span> <span data-ttu-id="f8b1d-126">Кроме того, необходимо указать имя, которое будет назначаться папке.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-126">You must also specify a name to be assigned to the folder.</span></span> <span data-ttu-id="f8b1d-127">Затем необходимо скопировать все необходимые файлы установки в указанное вами расположение.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-127">You must then copy all required installation files to the location that you specified.</span></span> <span data-ttu-id="f8b1d-128">Если папка, содержащая установочные файлы, уже существует на компьютере, на котором работает секвенсор, нажмите кнопку **Обзор** , чтобы выбрать папку.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-128">If the folder that contains the installation files already exists on the computer that runs the Sequencer, click **Browse** to select the folder.</span></span>

    <span data-ttu-id="f8b1d-129">Кроме того, если вы уже скопировали файлы установки в каталог на этом компьютере, щелкните **создать папку**, перейдите в папку, содержащую установочные файлы, и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-129">Alternatively, if you have already copied the installation files to a directory on this computer, click **Make New Folder**, browse to the folder that contains the installation files, and then click **Next**.</span></span>

    **<span data-ttu-id="f8b1d-130">Примечание.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-130">Note</span></span>**  
    <span data-ttu-id="f8b1d-131">Вы можете указать следующие типы файлов, которые поддерживаются при установке:</span><span class="sxs-lookup"><span data-stu-id="f8b1d-131">You can specify the following types of supported installation files:</span></span>

    -   <span data-ttu-id="f8b1d-132">Файлы установщика Windows (**MSI**)</span><span class="sxs-lookup"><span data-stu-id="f8b1d-132">Windows Installer files (**.msi**)</span></span>

    -   <span data-ttu-id="f8b1d-133">САВ-файлы (CAB)</span><span class="sxs-lookup"><span data-stu-id="f8b1d-133">Cabinet files (.cab)</span></span>

    -   <span data-ttu-id="f8b1d-134">Сжатые файлы с расширением имени ZIP-файла</span><span class="sxs-lookup"><span data-stu-id="f8b1d-134">Compressed files with a .zip file name extension</span></span>

    -   <span data-ttu-id="f8b1d-135">Файлы реальных приложений</span><span class="sxs-lookup"><span data-stu-id="f8b1d-135">The actual application files</span></span>

    <span data-ttu-id="f8b1d-136">Следующие типы файлов не поддерживаются: **MSP** и **exe** .</span><span class="sxs-lookup"><span data-stu-id="f8b1d-136">The following file types are not supported: **.msp** and **.exe** files.</span></span> <span data-ttu-id="f8b1d-137">Если указан **exe** – файл, необходимо извлечь установочные файлы вручную.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-137">If you specify an **.exe** file, you must extract the installation files manually.</span></span>



~~~
If the package accelerator requires an application to be installed before you apply the Package Accelerator, and if you have already installed the required application, select **I have installed all applications**, and then click **Next** on the **Local Installation** page.
~~~

6. <span data-ttu-id="f8b1d-138">На странице **имя пакета** укажите имя, которое будет сопоставлено с пакетом.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-138">On the **Package Name** page, specify a name that will be associated with the package.</span></span> <span data-ttu-id="f8b1d-139">Указанное имя определяет пакет в консоли управления App-V.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-139">The name that you specify identifies the package in the App-V Management Console.</span></span> <span data-ttu-id="f8b1d-140">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-140">Click **Next**.</span></span>

7. <span data-ttu-id="f8b1d-141">На странице " **Создание пакета** " Введите примечания, которые будут связаны с пакетом.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-141">On the **Create Package** page, provide comments that will be associated with the package.</span></span> <span data-ttu-id="f8b1d-142">Примечания должны содержать идентификационные данные о создаваемом пакете.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-142">The comments should contain identifying information about the package that you are creating.</span></span> <span data-ttu-id="f8b1d-143">Для подтверждения места создания пакета ознакомьтесь со сведениями, которые отображаются в **папке для сохранения**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-143">To confirm the location where the package is created, review the information that is displayed in **Save Location**.</span></span> <span data-ttu-id="f8b1d-144">Чтобы сжать пакет, выберите пункт **сжать пакет**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-144">To compress the package, select **Compress Package**.</span></span> <span data-ttu-id="f8b1d-145">Установите флажок **сжимать пакет** , если пакет будет передаваться по сети или если размер пакета ПРЕВЫШАЕТ 4 ГБ.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-145">Select the **Compress Package** check box if the package will be streamed across the network, or when the package size exceeds 4 GB.</span></span>

   <span data-ttu-id="f8b1d-146">Чтобы создать пакет, нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-146">To create the package, click **Create**.</span></span> <span data-ttu-id="f8b1d-147">После создания пакета нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-147">After the package is created, click **Next**.</span></span>

8. <span data-ttu-id="f8b1d-148">На странице " **Настройка программного обеспечения** " для включения секвенсора для настройки приложений, входящих в пакет, выберите пункт " **Настройка программного обеспечения**".</span><span class="sxs-lookup"><span data-stu-id="f8b1d-148">On the **Configure Software** page, to enable the Sequencer to configure the applications that are contained in the package, select **Configure Software**.</span></span> <span data-ttu-id="f8b1d-149">На этом этапе можно настроить все связанные задачи, которые необходимо выполнить, чтобы запустить приложение на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-149">In this step you can configure any associated tasks that must be completed in order to run the application on the target computers.</span></span> <span data-ttu-id="f8b1d-150">Например, вы можете настроить любые связанные лицензионные соглашения.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-150">For example, you can configure any associated license agreements.</span></span>

   <span data-ttu-id="f8b1d-151">Если выбрать параметр **настроить программное обеспечение**, можно настроить следующие элементы с помощью секвенсора в рамках этого этапа:</span><span class="sxs-lookup"><span data-stu-id="f8b1d-151">If you select **Configure Software**, the following items can be configured using the Sequencer as part of this step:</span></span>

   -   <span data-ttu-id="f8b1d-152">**Загрузить пакет**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-152">**Load Package**.</span></span> <span data-ttu-id="f8b1d-153">Программа Sequencer загружает файлы, связанные с пакетом.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-153">The Sequencer loads the files that are associated with the package.</span></span> <span data-ttu-id="f8b1d-154">Декодирование пакета может занять от нескольких секунд до часа.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-154">It can take several seconds to an hour to decode the package.</span></span>

   -   <span data-ttu-id="f8b1d-155">**Запустите каждую программу**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-155">**Run Each Program**.</span></span> <span data-ttu-id="f8b1d-156">При необходимости запустите программы, содержащиеся в пакете.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-156">Optionally run the programs that are contained in the package.</span></span> <span data-ttu-id="f8b1d-157">Этот этап полезен для выполнения связанных с ним лицензий или задач настройки, которые необходимы для запуска приложения перед развертыванием и запуском пакета на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-157">This step is helpful to complete any associated license or configuration tasks that are required to run the application before you deploy and run the package on target computers.</span></span> <span data-ttu-id="f8b1d-158">Чтобы запустить сразу все программы, выберите по крайней мере одну программу, а затем нажмите кнопку **выполнить все**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-158">To run all the programs at once, select at least one program, and then click **Run All**.</span></span> <span data-ttu-id="f8b1d-159">Чтобы запустить определенные программы, выберите программу или программы, которые вы хотите запустить, и нажмите кнопку **выполнить выбрано**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-159">To run specific programs, select the program or programs that you want to run, and then click **Run Selected**.</span></span> <span data-ttu-id="f8b1d-160">Заполните необходимые задачи настройки, а затем закройте приложения.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-160">Complete the required configuration tasks, and then close the applications.</span></span> <span data-ttu-id="f8b1d-161">Для запуска всех программ может потребоваться несколько минут.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-161">It can take several minutes for all programs to run.</span></span> <span data-ttu-id="f8b1d-162">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-162">Click **Next**.</span></span>

   -   <span data-ttu-id="f8b1d-163">**Сохранить пакет**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-163">**Save Package**.</span></span> <span data-ttu-id="f8b1d-164">Секвенсор сохраняет пакет.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-164">The Sequencer saves the package.</span></span>

   -   <span data-ttu-id="f8b1d-165">**Основной блок функций**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-165">**Primary Feature Block**.</span></span> <span data-ttu-id="f8b1d-166">Секвенсор оптимизирует пакет для потоковой передачи, перестраивая основной блок функций.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-166">The Sequencer optimizes the package for streaming by rebuilding the primary feature block.</span></span>

   <span data-ttu-id="f8b1d-167">Если вы не хотите настраивать приложения, нажмите **пропустить этот шаг**и перейдите к действию 9, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-167">If you do not want to configure the applications, click **Skip this step**, and to go to step 9 of this procedure, and then click **Next**.</span></span>

9. <span data-ttu-id="f8b1d-168">На странице **завершения** после просмотра данных, отображаемых в области **отчета о пакетах виртуальных приложений** , нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-168">On the **Completion** page, after you review the information that is displayed in the **Virtual Application Package Report** pane, click **Close**.</span></span>

   <span data-ttu-id="f8b1d-169">Пакет теперь доступен в секвенсоре.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-169">The package is now available in the Sequencer.</span></span> <span data-ttu-id="f8b1d-170">Чтобы изменить свойства пакета, нажмите **изменить \ [имя пакета \]**.</span><span class="sxs-lookup"><span data-stu-id="f8b1d-170">To edit the package properties, click **Edit \[Package Name\]**.</span></span> <span data-ttu-id="f8b1d-171">Дополнительные сведения о том, как изменить пакет, приведены [в разделе Изменение существующего виртуального пакета приложения](how-to-modify-an-existing-virtual-application-package-beta.md).</span><span class="sxs-lookup"><span data-stu-id="f8b1d-171">For more information about how to modify a package, see [How to Modify an Existing Virtual Application Package](how-to-modify-an-existing-virtual-application-package-beta.md).</span></span>

   <span data-ttu-id="f8b1d-172">**У вас есть предложение App-V**?</span><span class="sxs-lookup"><span data-stu-id="f8b1d-172">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f8b1d-173">Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f8b1d-173">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f8b1d-174">У вас возникла ошибка App-V?</span><span class="sxs-lookup"><span data-stu-id="f8b1d-174">Got an App-V issue?</span></span>** <span data-ttu-id="f8b1d-175">Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f8b1d-175">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f8b1d-176">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f8b1d-176">Related topics</span></span>


[<span data-ttu-id="f8b1d-177">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f8b1d-177">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









