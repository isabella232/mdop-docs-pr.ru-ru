---
title: Создание виртуализированных приложений App-V 5.0 и управление ими
description: Создание виртуализированных приложений App-V 5.0 и управление ими
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814701"
---
# <span data-ttu-id="455e6-103">Создание виртуализированных приложений App-V 5.0 и управление ими</span><span class="sxs-lookup"><span data-stu-id="455e6-103">Creating and Managing App-V 5.0 Virtualized Applications</span></span>


<span data-ttu-id="455e6-104">После того, как приложение Microsoft Application Virtualization (App-V) 5,0 правильно развернуто, вы можете использовать его для отслеживания и записи процесса установки и настройки приложения, которое должно выполняться как виртуализированное приложение.</span><span class="sxs-lookup"><span data-stu-id="455e6-104">After you have properly deployed the Microsoft Application Virtualization (App-V) 5.0 sequencer, you can use it to monitor and record the installation and setup process for an application to be run as a virtualized application.</span></span>

<span data-ttu-id="455e6-105">**Примечание**  Дополнительные сведения о настройке Microsoft Application Virtualization (App-V) 5,0 Sequencer, рекомендации по планированию приложений и примеры создания и обновления виртуального приложения можно найти в [руководстве упорядочение Microsoft Application virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 Guide.docx).</span><span class="sxs-lookup"><span data-stu-id="455e6-105">**Note** For more information about configuring the Microsoft Application Virtualization (App-V) 5.0 sequencer, sequencing best practices, and an example of creating and updating a virtual application, see the [Microsoft Application Virtualization 5.0 Sequencing Guide](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) (https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx).</span></span>

 

## <span data-ttu-id="455e6-106">Упорядочение приложения</span><span class="sxs-lookup"><span data-stu-id="455e6-106">Sequencing an application</span></span>


<span data-ttu-id="455e6-107">Секвенсор App-V 5,0 можно использовать для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="455e6-107">You can use the App-V 5.0 Sequencer to perform the following tasks:</span></span>

-   <span data-ttu-id="455e6-108">Создавайте виртуальные пакеты, которые можно развертывать на компьютерах, на которых запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-108">Create virtual packages that can be deployed to computers running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="455e6-109">Обновление существующих пакетов.</span><span class="sxs-lookup"><span data-stu-id="455e6-109">Upgrade existing packages.</span></span> <span data-ttu-id="455e6-110">Вы можете развернуть существующий пакет на компьютере с запущенным секвенсором, а затем обновить приложение, чтобы создать новую версию.</span><span class="sxs-lookup"><span data-stu-id="455e6-110">You can expand an existing package onto the computer running the sequencer and then upgrade the application to create a newer version.</span></span>

-   <span data-ttu-id="455e6-111">Изменить параметры конфигурации, связанные с существующим пакетом.</span><span class="sxs-lookup"><span data-stu-id="455e6-111">Edit configuration information associated with an existing package.</span></span> <span data-ttu-id="455e6-112">Например, вы можете добавить ярлык или изменить сопоставление типов файлов.</span><span class="sxs-lookup"><span data-stu-id="455e6-112">For example, you can add a shortcut or modify a file type association.</span></span>

    <span data-ttu-id="455e6-113">**Примечание**  Для обеспечения роуминга необходимо создать ярлыки и сохранить их в доступном месте в сети.</span><span class="sxs-lookup"><span data-stu-id="455e6-113">**Note** You must create shortcuts and save them to an available network location to allow roaming.</span></span> <span data-ttu-id="455e6-114">Если ярлык создан и сохранен в частном расположении, пакет должен быть опубликован локально на компьютере с клиентским приложением App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-114">If a shortcut is created and saved in a private location, the package must be published locally to the computer running the App-V 5.0 client.</span></span>

     

-   <span data-ttu-id="455e6-115">Преобразуйте существующие виртуальные пакеты.</span><span class="sxs-lookup"><span data-stu-id="455e6-115">Convert existing virtual packages.</span></span>

<span data-ttu-id="455e6-116">Секвенсор использует каталог \**% tmp% \** \ или \**% TEMP% \ \** **и временный каталог для** хранения временных файлов в процессе упорядочения.</span><span class="sxs-lookup"><span data-stu-id="455e6-116">The sequencer uses the **%TMP% \\ Scratch** or **%TEMP% \\ Scratch** directory and the **Temp** directory to store temporary files during sequencing.</span></span> <span data-ttu-id="455e6-117">На компьютере, на котором запущена программа Sequencer, необходимо настроить эти каталоги на свободное место на диске, чтобы оценить требования к установке приложения.</span><span class="sxs-lookup"><span data-stu-id="455e6-117">On the computer that runs the sequencer, you should configure these directories with free disk space equivalent to the estimated application installation requirements.</span></span> <span data-ttu-id="455e6-118">Настройка временных папок и временного каталога в разных разделах жесткого диска поможет повысить производительность при выполнении виртуализации.</span><span class="sxs-lookup"><span data-stu-id="455e6-118">Configuring the temp directories and the Temp directory on different hard drive partitions can help improve performance during sequencing.</span></span>

<span data-ttu-id="455e6-119">При использовании секвенсора для создания нового виртуального приложения создаются указанные ниже файлы.</span><span class="sxs-lookup"><span data-stu-id="455e6-119">When you use the sequencer to create a new virtual application, the following listed files are created.</span></span> <span data-ttu-id="455e6-120">Эти файлы состоят из пакета App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-120">These files comprise the App-V 5.0 package.</span></span>

-   <span data-ttu-id="455e6-121">MSI-файл.</span><span class="sxs-lookup"><span data-stu-id="455e6-121">.msi file.</span></span> <span data-ttu-id="455e6-122">Этот файл установщика Windows (MSI) создается программой Sequencer и используется для установки виртуального пакета на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="455e6-122">This Windows Installer (.msi) file is created by the sequencer and is used to install the virtual package on target computers.</span></span>

-   <span data-ttu-id="455e6-123">Report.xml файл.</span><span class="sxs-lookup"><span data-stu-id="455e6-123">Report.xml file.</span></span> <span data-ttu-id="455e6-124">В этом файле секвенсор сохраняет все проблемы, предупреждения и ошибки, обнаруженные во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="455e6-124">In this file, the sequencer saves all issues, warnings, and errors that were discovered during sequencing.</span></span> <span data-ttu-id="455e6-125">После создания пакета отображаются сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="455e6-125">It displays the information after the package has been created.</span></span> <span data-ttu-id="455e6-126">Вы можете получить этот отчет для диагностики и устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="455e6-126">You can us this report for diagnosing and troubleshooting.</span></span>

-   <span data-ttu-id="455e6-127">файл. AppV.</span><span class="sxs-lookup"><span data-stu-id="455e6-127">.appv file.</span></span> <span data-ttu-id="455e6-128">Это виртуальный файл приложения.</span><span class="sxs-lookup"><span data-stu-id="455e6-128">This is the virtual application file.</span></span>

-   <span data-ttu-id="455e6-129">Файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="455e6-129">Deployment configuration file.</span></span> <span data-ttu-id="455e6-130">Файл конфигурации развертывания определяет, как виртуальное приложение будет развернуто на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="455e6-130">The deployment configuration file determines how the virtual application will be deployed to target computers.</span></span>

-   <span data-ttu-id="455e6-131">Файл конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="455e6-131">User configuration file.</span></span> <span data-ttu-id="455e6-132">Файл конфигурации пользователя определяет, как виртуальное приложение будет выполняться на конечных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="455e6-132">The user configuration file determines how the virtual application will run on target computers.</span></span>

<span data-ttu-id="455e6-133">**Важно!**  Вы должны настроить папки% TMP% и% TEMP%, которые используются преобразователем пакетов, чтобы быть безопасным расположением и каталогом.</span><span class="sxs-lookup"><span data-stu-id="455e6-133">**Important** You must configure the %TMP% and %TEMP% folders that the package converter uses to be a secure location and directory.</span></span> <span data-ttu-id="455e6-134">Безопасное расположение доступно только администратору.</span><span class="sxs-lookup"><span data-stu-id="455e6-134">A secure location is only accessible by an administrator.</span></span> <span data-ttu-id="455e6-135">Кроме того, при последовательном указании пакета необходимо сохранить пакет в безопасном расположении или убедиться в том, что в процессе преобразования и мониторинга никто из пользователей не может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="455e6-135">Additionally, when you sequence the package you should save the package to a location that is secure, or make sure that no other user is allowed to be logged in during the conversion and monitoring process.</span></span>

 

<span data-ttu-id="455e6-136">Диалоговое окно " **Параметры** " на консоли "секвенсор" имеет следующие вкладки:</span><span class="sxs-lookup"><span data-stu-id="455e6-136">The **Options** dialog box in the sequencer console contains the following tabs:</span></span>

-   <span data-ttu-id="455e6-137">**Общие**.</span><span class="sxs-lookup"><span data-stu-id="455e6-137">**General**.</span></span> <span data-ttu-id="455e6-138">На этой вкладке можно включить Запуск обновлений Майкрософт во время виртуализации.</span><span class="sxs-lookup"><span data-stu-id="455e6-138">Use this tab to enable Microsoft Updates to run during sequencing.</span></span> <span data-ttu-id="455e6-139">Выберите команду **Добавить версию пакета в поле имя файла** , чтобы настроить последовательность для добавления номера версии виртуализированному пакету, для которого выполняется упорядочение.</span><span class="sxs-lookup"><span data-stu-id="455e6-139">Select **Append Package Version to Filename** to configure the sequence to add a version number to the virtualized package that is being sequenced.</span></span> <span data-ttu-id="455e6-140">Выберите **всегда доверять источнику ускорителей пакетов** для создания виртуализованных пакетов с помощью ускорителя пакетов без запроса на авторизацию.</span><span class="sxs-lookup"><span data-stu-id="455e6-140">Select **Always trust the source of Package Accelerators** to create virtualized packages using a package accelerator without being prompted for authorization.</span></span>

    <span data-ttu-id="455e6-141">**Важно!**  Акселераторы пакетов, созданные с помощью App-V 4.6, не поддерживаются приложением App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-141">**Important** Package Accelerators created using App-V4.6 are not supported by App-V 5.0.</span></span>

     

-   <span data-ttu-id="455e6-142">**Анализ элементов**.</span><span class="sxs-lookup"><span data-stu-id="455e6-142">**Parse Items**.</span></span> <span data-ttu-id="455e6-143">На этой вкладке отображаются связанные расположения путей к файлам, которые будут анализироваться или размечены в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="455e6-143">This tab displays the associated file path locations that will be parsed or tokenized into in the virtual environment.</span></span> <span data-ttu-id="455e6-144">Маркеры полезны при добавлении файлов с помощью вкладки **файлы пакетов** в режиме **расширенного редактирования**.</span><span class="sxs-lookup"><span data-stu-id="455e6-144">Tokens are useful for adding files using the **Package Files** tab in **Advanced Editing**.</span></span>

-   <span data-ttu-id="455e6-145">**Исключаемые элементы**.</span><span class="sxs-lookup"><span data-stu-id="455e6-145">**Exclusion Items**.</span></span> <span data-ttu-id="455e6-146">На этой вкладке можно указать, в каких папках и каталогах не следует наблюдать при выполнении последовательностей.</span><span class="sxs-lookup"><span data-stu-id="455e6-146">Use this tab to specify which folders and directories should not be monitored during sequencing.</span></span> <span data-ttu-id="455e6-147">Чтобы добавить данные локальных приложений, сохраненных в локальной папке данных приложения в пакете, нажмите **создать** и укажите расположение и связанный **тип сопоставления**.</span><span class="sxs-lookup"><span data-stu-id="455e6-147">To add local application data that is saved in the Local App Data folder in the package, click **New** and specify the location and the associated **Mapping Type**.</span></span> <span data-ttu-id="455e6-148">Этот параметр является обязательным для некоторых пакетов.</span><span class="sxs-lookup"><span data-stu-id="455e6-148">This option is required for some packages.</span></span>

<span data-ttu-id="455e6-149">Приложение App-V 5,0 поддерживает приложения, которые включают службы Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="455e6-149">App-V 5.0 supports applications that include Microsoft Windows Services.</span></span> <span data-ttu-id="455e6-150">Если приложение содержит службу Windows, она будет включена в упорядоченный виртуальный пакет, если он установлен в процессе наблюдения секвенсором.</span><span class="sxs-lookup"><span data-stu-id="455e6-150">If an application includes a Windows service, the Service will be included in the sequenced virtual package as long as it is installed while being monitored by the sequencer.</span></span> <span data-ttu-id="455e6-151">Если виртуальное приложение создает службу Windows при первоначальном запуске, а затем позднее после установки, необходимо запустить приложение, когда секвенсор находится в наблюдении, чтобы служба Windows была добавлена в пакет.</span><span class="sxs-lookup"><span data-stu-id="455e6-151">If a virtual application creates a Windows service when it initially runs, then later, after installation, the application must be run while the sequencer is monitoring so that the Windows Service will be added to the package.</span></span> <span data-ttu-id="455e6-152">Поддерживаются только службы, которые выполняются под учетной записью Local System.</span><span class="sxs-lookup"><span data-stu-id="455e6-152">Only Services that run under the Local System account are supported.</span></span> <span data-ttu-id="455e6-153">Службы, настроенные для автозапуска или отложенного автозапуска, запускаются перед тем, как первое виртуальное приложение в пакете выполняется внутри виртуальной среды пакета.</span><span class="sxs-lookup"><span data-stu-id="455e6-153">Services that are configured for AutoStart or Delayed AutoStart are started before the first virtual application in a package runs inside the package’s Virtual Environment.</span></span> <span data-ttu-id="455e6-154">Службы Windows, настроенные для запуска по запросу приложения, запускаются, когда виртуальное приложение в пакете запускает службу через вызов API.</span><span class="sxs-lookup"><span data-stu-id="455e6-154">Windows Services that are configured to be started on demand by an application are started when the virtual application inside the package starts the Service via API call.</span></span>

[<span data-ttu-id="455e6-155">Виртуализация нового приложения с помощью App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="455e6-155">How to Sequence a New Application with App-V 5.0</span></span>](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> <span data-ttu-id="455e6-156">Поддержка расширения оболочки App-V 5.0 SP2</span><span class="sxs-lookup"><span data-stu-id="455e6-156">App-V 5.0SP2 shell extension support</span></span>


<span data-ttu-id="455e6-157">App-V 5.0 SP2 поддерживает расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="455e6-157">App-V 5.0SP2 supports shell extensions.</span></span> <span data-ttu-id="455e6-158">Расширения оболочки будут обнаружены и внедрены в пакет во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="455e6-158">Shell extensions will be detected and embedded in the package during sequencing.</span></span>

<span data-ttu-id="455e6-159">Расширения оболочки встраиваются в пакет автоматически в процессе упорядочивания.</span><span class="sxs-lookup"><span data-stu-id="455e6-159">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="455e6-160">При публикации пакета расширение оболочки предоставляет пользователям те же функциональные возможности, что и при локальном установлении приложения.</span><span class="sxs-lookup"><span data-stu-id="455e6-160">When the package is published, the shell extension gives users the same functionality as if the application were locally installed.</span></span>

**<span data-ttu-id="455e6-161">Требования для использования расширений оболочки:</span><span class="sxs-lookup"><span data-stu-id="455e6-161">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="455e6-162">Пакеты, содержащие внедренные расширения оболочки, должны быть опубликованы глобально.</span><span class="sxs-lookup"><span data-stu-id="455e6-162">Packages that contain embedded shell extensions must be published globally.</span></span> <span data-ttu-id="455e6-163">Для включения функций расширения оболочки приложению не требуется дополнительная настройка или Настройка клиента.</span><span class="sxs-lookup"><span data-stu-id="455e6-163">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

-   <span data-ttu-id="455e6-164">"Разрядность" приложения, секвенсора и клиента App-V должны совпадать, или расширения оболочки не работают.</span><span class="sxs-lookup"><span data-stu-id="455e6-164">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="455e6-165">Пример</span><span class="sxs-lookup"><span data-stu-id="455e6-165">For example:</span></span>

    -   <span data-ttu-id="455e6-166">Версия приложения — 64-разр.</span><span class="sxs-lookup"><span data-stu-id="455e6-166">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="455e6-167">Секвенсор выполняется на 64-разрядном компьютере.</span><span class="sxs-lookup"><span data-stu-id="455e6-167">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="455e6-168">Пакет доставляется на клиентский компьютер App-V 64-bit.</span><span class="sxs-lookup"><span data-stu-id="455e6-168">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="455e6-169">В таблице ниже перечислены поддерживаемые расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="455e6-169">The following table lists the supported shell extensions:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="455e6-170">Обработчик</span><span class="sxs-lookup"><span data-stu-id="455e6-170">Handler</span></span></th>
<th align="left"><span data-ttu-id="455e6-171">Описание</span><span class="sxs-lookup"><span data-stu-id="455e6-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="455e6-172">Обработчик контекстного меню</span><span class="sxs-lookup"><span data-stu-id="455e6-172">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-173">Добавляет элементы меню в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="455e6-173">Adds menu items to the context menu.</span></span> <span data-ttu-id="455e6-174">Вызывается перед отображением контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="455e6-174">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="455e6-175">Обработчик перетаскивания</span><span class="sxs-lookup"><span data-stu-id="455e6-175">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-176">Управляет действием, которое можно щелкнуть правой кнопкой мыши, перетащить и изменить появившееся контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="455e6-176">Controls the action where right-click, drag and drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="455e6-177">Целевой обработчик перетаскивания</span><span class="sxs-lookup"><span data-stu-id="455e6-177">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-178">Управляет действием после того, как объект данных перетаскивается и отбрасывается по направлению перетаскивания, например файлу.</span><span class="sxs-lookup"><span data-stu-id="455e6-178">Controls the action after a data object is dragged and dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="455e6-179">Обработчик объектов данных</span><span class="sxs-lookup"><span data-stu-id="455e6-179">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-180">Управляет действием после того, как файл копируется в буфер обмена или перетаскивается и удаляется по направлению перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="455e6-180">Controls the action after a file is copied to the clipboard or dragged and dropped over a drop target.</span></span> <span data-ttu-id="455e6-181">Он может предоставлять дополнительные форматы буфера обмена для целевого объекта перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="455e6-181">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="455e6-182">Обработчик страницы свойств</span><span class="sxs-lookup"><span data-stu-id="455e6-182">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-183">Заменяет или добавляет страницы в диалоговое окно "страница свойств" объекта.</span><span class="sxs-lookup"><span data-stu-id="455e6-183">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="455e6-184">Обработчик всплывающих подсказк</span><span class="sxs-lookup"><span data-stu-id="455e6-184">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-185">Позволяет получать сведения о флагах и всплывающих подсказках для элемента и отображать их в всплывающей подсказке при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="455e6-185">Allows retrieving flags and infotip information for an item and displaying it inside a pop-up tooltip upon mouse hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="455e6-186">Обработчик столбцов</span><span class="sxs-lookup"><span data-stu-id="455e6-186">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-187">Позволяет создавать и отображать пользовательские столбцы в <strong> представлении "сведения" в проводнике Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="455e6-187">Allows creating and displaying custom columns in <strong>Windows Explorer Details view</strong>.</span></span> <span data-ttu-id="455e6-188">Его можно использовать для расширенной сортировки и группировки.</span><span class="sxs-lookup"><span data-stu-id="455e6-188">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="455e6-189">Обработчик просмотра</span><span class="sxs-lookup"><span data-stu-id="455e6-189">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="455e6-190">Обеспечивает предварительный просмотр файла, который будет отображаться в области предварительного просмотра в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="455e6-190">Enables a preview of a file to be displayed in the Windows Explorer Preview pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="455e6-191">Поддержка добавочных копий файлов при записи (CoW)</span><span class="sxs-lookup"><span data-stu-id="455e6-191">Copy on Write (CoW) file extension support</span></span>


<span data-ttu-id="455e6-192">Файлы в расширениях CoW позволяют App-V 5,0 динамически вносить записи в определенные расположения, содержащиеся в виртуальном пакете во время использования.</span><span class="sxs-lookup"><span data-stu-id="455e6-192">Copy on write (CoW) file extensions allow App-V 5.0 to dynamically write to specific locations contained in the virtual package while it is being used.</span></span>

<span data-ttu-id="455e6-193">В следующей таблице показаны типы файлов, которые могут существовать в виртуальном пакете в каталоге VFS, но их невозможно обновить на компьютере, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-193">The following table displays the file types that can exist in a virtual package under the VFS directory, but cannot be updated on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="455e6-194">Любые другие файлы и каталоги можно изменить.</span><span class="sxs-lookup"><span data-stu-id="455e6-194">All other files and directories can be modified.</span></span>

<span data-ttu-id="455e6-195">. ACM</span><span class="sxs-lookup"><span data-stu-id="455e6-195">.acm</span></span>

<span data-ttu-id="455e6-196">. ASA</span><span class="sxs-lookup"><span data-stu-id="455e6-196">.asa</span></span>

<span data-ttu-id="455e6-197">.asp</span><span class="sxs-lookup"><span data-stu-id="455e6-197">.asp</span></span>

<span data-ttu-id="455e6-198">. aspx</span><span class="sxs-lookup"><span data-stu-id="455e6-198">.aspx</span></span>

<span data-ttu-id="455e6-199">. AX</span><span class="sxs-lookup"><span data-stu-id="455e6-199">.ax</span></span>

<span data-ttu-id="455e6-200">.bat</span><span class="sxs-lookup"><span data-stu-id="455e6-200">.bat</span></span>

<span data-ttu-id="455e6-201">.cer</span><span class="sxs-lookup"><span data-stu-id="455e6-201">.cer</span></span>

<span data-ttu-id="455e6-202">.chm</span><span class="sxs-lookup"><span data-stu-id="455e6-202">.chm</span></span>

<span data-ttu-id="455e6-203">. распределения загрузки</span><span class="sxs-lookup"><span data-stu-id="455e6-203">.clb</span></span>

<span data-ttu-id="455e6-204">.cmd</span><span class="sxs-lookup"><span data-stu-id="455e6-204">.cmd</span></span>

<span data-ttu-id="455e6-205">.cnt</span><span class="sxs-lookup"><span data-stu-id="455e6-205">.cnt</span></span>

<span data-ttu-id="455e6-206">.cnv</span><span class="sxs-lookup"><span data-stu-id="455e6-206">.cnv</span></span>

<span data-ttu-id="455e6-207">.com</span><span class="sxs-lookup"><span data-stu-id="455e6-207">.com</span></span>

<span data-ttu-id="455e6-208">.cpl</span><span class="sxs-lookup"><span data-stu-id="455e6-208">.cpl</span></span>

<span data-ttu-id="455e6-209">.cpx</span><span class="sxs-lookup"><span data-stu-id="455e6-209">.cpx</span></span>

<span data-ttu-id="455e6-210">.crt</span><span class="sxs-lookup"><span data-stu-id="455e6-210">.crt</span></span>

<span data-ttu-id="455e6-211">.dll</span><span class="sxs-lookup"><span data-stu-id="455e6-211">.dll</span></span>

<span data-ttu-id="455e6-212">.drv</span><span class="sxs-lookup"><span data-stu-id="455e6-212">.drv</span></span>

<span data-ttu-id="455e6-213">.exe</span><span class="sxs-lookup"><span data-stu-id="455e6-213">.exe</span></span>

<span data-ttu-id="455e6-214">.fon</span><span class="sxs-lookup"><span data-stu-id="455e6-214">.fon</span></span>

<span data-ttu-id="455e6-215">.grp</span><span class="sxs-lookup"><span data-stu-id="455e6-215">.grp</span></span>

<span data-ttu-id="455e6-216">.hlp</span><span class="sxs-lookup"><span data-stu-id="455e6-216">.hlp</span></span>

<span data-ttu-id="455e6-217">.hta</span><span class="sxs-lookup"><span data-stu-id="455e6-217">.hta</span></span>

<span data-ttu-id="455e6-218">. IME</span><span class="sxs-lookup"><span data-stu-id="455e6-218">.ime</span></span>

<span data-ttu-id="455e6-219">INF</span><span class="sxs-lookup"><span data-stu-id="455e6-219">.inf</span></span>

<span data-ttu-id="455e6-220">INS</span><span class="sxs-lookup"><span data-stu-id="455e6-220">.ins</span></span>

<span data-ttu-id="455e6-221">.isp</span><span class="sxs-lookup"><span data-stu-id="455e6-221">.isp</span></span>

<span data-ttu-id="455e6-222">. его</span><span class="sxs-lookup"><span data-stu-id="455e6-222">.its</span></span>

<span data-ttu-id="455e6-223">.js</span><span class="sxs-lookup"><span data-stu-id="455e6-223">.js</span></span>

<span data-ttu-id="455e6-224">.jse</span><span class="sxs-lookup"><span data-stu-id="455e6-224">.jse</span></span>

<span data-ttu-id="455e6-225">.lnk</span><span class="sxs-lookup"><span data-stu-id="455e6-225">.lnk</span></span>

<span data-ttu-id="455e6-226">.msc</span><span class="sxs-lookup"><span data-stu-id="455e6-226">.msc</span></span>

<span data-ttu-id="455e6-227">.msi</span><span class="sxs-lookup"><span data-stu-id="455e6-227">.msi</span></span>

<span data-ttu-id="455e6-228">.msp</span><span class="sxs-lookup"><span data-stu-id="455e6-228">.msp</span></span>

<span data-ttu-id="455e6-229">.mst</span><span class="sxs-lookup"><span data-stu-id="455e6-229">.mst</span></span>

<span data-ttu-id="455e6-230">MUI</span><span class="sxs-lookup"><span data-stu-id="455e6-230">.mui</span></span>

<span data-ttu-id="455e6-231">. NLS</span><span class="sxs-lookup"><span data-stu-id="455e6-231">.nls</span></span>

<span data-ttu-id="455e6-232">.ocx</span><span class="sxs-lookup"><span data-stu-id="455e6-232">.ocx</span></span>

<span data-ttu-id="455e6-233">PAL</span><span class="sxs-lookup"><span data-stu-id="455e6-233">.pal</span></span>

<span data-ttu-id="455e6-234">.pcd</span><span class="sxs-lookup"><span data-stu-id="455e6-234">.pcd</span></span>

<span data-ttu-id="455e6-235">.pif</span><span class="sxs-lookup"><span data-stu-id="455e6-235">.pif</span></span>

<span data-ttu-id="455e6-236">.reg</span><span class="sxs-lookup"><span data-stu-id="455e6-236">.reg</span></span>

<span data-ttu-id="455e6-237">.scf</span><span class="sxs-lookup"><span data-stu-id="455e6-237">.scf</span></span>

<span data-ttu-id="455e6-238">.scr</span><span class="sxs-lookup"><span data-stu-id="455e6-238">.scr</span></span>

<span data-ttu-id="455e6-239">.sct</span><span class="sxs-lookup"><span data-stu-id="455e6-239">.sct</span></span>

<span data-ttu-id="455e6-240">.shb</span><span class="sxs-lookup"><span data-stu-id="455e6-240">.shb</span></span>

<span data-ttu-id="455e6-241">.shs</span><span class="sxs-lookup"><span data-stu-id="455e6-241">.shs</span></span>

<span data-ttu-id="455e6-242">.sys</span><span class="sxs-lookup"><span data-stu-id="455e6-242">.sys</span></span>

<span data-ttu-id="455e6-243">TLB</span><span class="sxs-lookup"><span data-stu-id="455e6-243">.tlb</span></span>

<span data-ttu-id="455e6-244">. TSP</span><span class="sxs-lookup"><span data-stu-id="455e6-244">.tsp</span></span>

<span data-ttu-id="455e6-245">.url</span><span class="sxs-lookup"><span data-stu-id="455e6-245">.url</span></span>

<span data-ttu-id="455e6-246">.vb</span><span class="sxs-lookup"><span data-stu-id="455e6-246">.vb</span></span>

<span data-ttu-id="455e6-247">.vbe</span><span class="sxs-lookup"><span data-stu-id="455e6-247">.vbe</span></span>

<span data-ttu-id="455e6-248">.vbs</span><span class="sxs-lookup"><span data-stu-id="455e6-248">.vbs</span></span>

<span data-ttu-id="455e6-249">.vsmacros</span><span class="sxs-lookup"><span data-stu-id="455e6-249">.vsmacros</span></span>

<span data-ttu-id="455e6-250">.ws</span><span class="sxs-lookup"><span data-stu-id="455e6-250">.ws</span></span>

<span data-ttu-id="455e6-251">. ESC</span><span class="sxs-lookup"><span data-stu-id="455e6-251">.esc</span></span>

<span data-ttu-id="455e6-252">.wsf</span><span class="sxs-lookup"><span data-stu-id="455e6-252">.wsf</span></span>

<span data-ttu-id="455e6-253">.wsh</span><span class="sxs-lookup"><span data-stu-id="455e6-253">.wsh</span></span>

 

## <span data-ttu-id="455e6-254">Изменение существующего пакета виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="455e6-254">Modifying an existing virtual application package</span></span>


<span data-ttu-id="455e6-255">С помощью секвенсора можно изменить существующий пакет.</span><span class="sxs-lookup"><span data-stu-id="455e6-255">You can use the sequencer to modify an existing package.</span></span> <span data-ttu-id="455e6-256">Компьютер, на котором вы выполняете это действие, должен соответствовать архитектуре микросхемы компьютера, который использовался для создания приложения.</span><span class="sxs-lookup"><span data-stu-id="455e6-256">The computer on which you do this should match the chip architecture of the computer you used to create the application.</span></span> <span data-ttu-id="455e6-257">Например, при первоначальном упорядочении пакета с помощью компьютера, работающего под управлением 64-разрядной операционной системы, необходимо изменить пакет с помощью компьютера, работающего под управлением 64-разрядной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="455e6-257">For example, if you initially sequenced a package using a computer running a 64-bit operating system, you should modify the package using a computer running a 64-bit operating system.</span></span>

[<span data-ttu-id="455e6-258">Изменение существующего пакета виртуального приложения</span><span class="sxs-lookup"><span data-stu-id="455e6-258">How to Modify an Existing Virtual Application Package</span></span>](how-to-modify-an-existing-virtual-application-package-beta.md)

## <span data-ttu-id="455e6-259">Создание шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="455e6-259">Creating a project template</span></span>


<span data-ttu-id="455e6-260">Appvt-файл — это шаблон проекта, который можно использовать для сохранения часто применяемых, настраиваемых параметров.</span><span class="sxs-lookup"><span data-stu-id="455e6-260">A .appvt file is a project template that can be used to save commonly applied, customized settings.</span></span> <span data-ttu-id="455e6-261">Вы можете использовать эти параметры для будущих последовательностей.</span><span class="sxs-lookup"><span data-stu-id="455e6-261">You can then more easily use these settings for future sequencings.</span></span>

<span data-ttu-id="455e6-262">Шаблоны проектов App-V 5,0 отличаются от ускорителей приложений App-V 5,0, так как для App-V 5,0 акселераторы приложений и шаблоны проектов App-V 5,0 можно применять к нескольким приложениям.</span><span class="sxs-lookup"><span data-stu-id="455e6-262">App-V 5.0 project templates differ from App-V 5.0 Application Accelerators because App-V 5.0 Application Accelerators are application-specific, and App-V 5.0 project templates can be applied to multiple applications.</span></span> <span data-ttu-id="455e6-263">Кроме того, шаблон проекта нельзя использовать для создания виртуального пакета приложения, если вы используете ускоритель пакетов.</span><span class="sxs-lookup"><span data-stu-id="455e6-263">Additionally, you cannot use a project template when you use a Package Accelerator to create a virtual application package.</span></span> <span data-ttu-id="455e6-264">Следующие общие параметры сохраняются в шаблоне проекта App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="455e6-264">The following general settings are saved with an App-V 5.0 project template:</span></span>

<span data-ttu-id="455e6-265">В шаблоне можно указать и сохранить несколько параметров, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="455e6-265">A template can specify and store multiple settings as follows:</span></span>

-   <span data-ttu-id="455e6-266">**Дополнительные параметры наблюдения**.</span><span class="sxs-lookup"><span data-stu-id="455e6-266">**Advanced Monitoring Options**.</span></span> <span data-ttu-id="455e6-267">Включение функции центра обновления Майкрософт во время наблюдения.</span><span class="sxs-lookup"><span data-stu-id="455e6-267">Enables Microsoft Update to run during monitoring.</span></span> <span data-ttu-id="455e6-268">Сохранение разрешающей локальной настройки параметров взаимодействия</span><span class="sxs-lookup"><span data-stu-id="455e6-268">Saves allow local interaction option settings</span></span>

-   <span data-ttu-id="455e6-269">**Общие параметры**.</span><span class="sxs-lookup"><span data-stu-id="455e6-269">**General Options**.</span></span> <span data-ttu-id="455e6-270">Позволяет использовать **установщик Windows**, **добавлять версию пакета в имя файла**.</span><span class="sxs-lookup"><span data-stu-id="455e6-270">Enables the use of **Windows Installer**, **Append Package Version to Filename**.</span></span>

-   **<span data-ttu-id="455e6-271">Исключаемые элементы.</span><span class="sxs-lookup"><span data-stu-id="455e6-271">Exclusion Items.</span></span>** <span data-ttu-id="455e6-272">Содержащий список шаблонов исключений.</span><span class="sxs-lookup"><span data-stu-id="455e6-272">Contains the Exclusion pattern list.</span></span>

[<span data-ttu-id="455e6-273">Создание и использование шаблона проекта</span><span class="sxs-lookup"><span data-stu-id="455e6-273">How to Create and Use a Project Template</span></span>](how-to-create-and-use-a-project-template.md)

## <span data-ttu-id="455e6-274">Создание ускорителя пакетов</span><span class="sxs-lookup"><span data-stu-id="455e6-274">Creating a package accelerator</span></span>


<span data-ttu-id="455e6-275">**Примечание**  Ускорители пакетов, созданные с помощью более ранней версии App-V, должны быть созданы повторно с помощью App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-275">**Note** Package accelerators created using a previous version of App-V must be recreated using App-V 5.0.</span></span>

 

<span data-ttu-id="455e6-276">Вы можете использовать ускорители пакетов App-V 5,0 для автоматического создания новых пакетов виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="455e6-276">You can use App-V 5.0 package accelerators to automatically generate a new virtual application packages.</span></span> <span data-ttu-id="455e6-277">После того как вы успешно создадите ускоритель пакетов, вы можете повторно использовать ускоритель пакетов и предоставить к нему общий доступ.</span><span class="sxs-lookup"><span data-stu-id="455e6-277">After you have successfully created a package accelerator, you can reuse and share the package accelerator.</span></span>

<span data-ttu-id="455e6-278">В некоторых случаях для создания ускорителя пакетов может потребоваться установить локальное приложение на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="455e6-278">In some situations, to create the package accelerator, you might have to install the application locally on the computer that runs the sequencer.</span></span> <span data-ttu-id="455e6-279">В таких случаях следует сначала попытаться создать ускоритель пакетов с помощью установочного носителя.</span><span class="sxs-lookup"><span data-stu-id="455e6-279">In such cases, you should first try to create the package accelerator with the installation media.</span></span> <span data-ttu-id="455e6-280">Если требуется несколько отсутствующих файлов, необходимо установить приложение локально на компьютер, на котором работает секвенсор, а затем создать ускоритель пакетов.</span><span class="sxs-lookup"><span data-stu-id="455e6-280">If multiple missing files are required, you should install the application locally to the computer that runs the sequencer, and then create the package accelerator.</span></span>

<span data-ttu-id="455e6-281">После того как вы успешно создадите ускоритель пакетов, вы можете повторно использовать ускоритель пакетов и предоставить к нему общий доступ.</span><span class="sxs-lookup"><span data-stu-id="455e6-281">After you have successfully created a Package Accelerator, you can reuse and share the Package Accelerator.</span></span> <span data-ttu-id="455e6-282">Создание ускорителей пакетов для App-V 5,0 является сложной задачей.</span><span class="sxs-lookup"><span data-stu-id="455e6-282">Creating App-V 5.0 Package Accelerators is an advanced task.</span></span> <span data-ttu-id="455e6-283">Ускорители пакетов могут содержать пароль и сведения для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="455e6-283">Package Accelerators can contain password and user-specific information.</span></span> <span data-ttu-id="455e6-284">Поэтому вы должны сохранить ускорители пакетов и связанный установочный носитель в безопасном расположении, и вы должны добавить цифровую подпись ускорителя пакетов после его создания, чтобы издатель мог быть проверен при применении ускорителя приложений App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="455e6-284">Therefore you must save Package Accelerators and the associated installation media in a secure location, and you should digitally sign the Package Accelerator after you create it so that the publisher can be verified when the App-V 5.0 Package Accelerator is applied.</span></span>

[<span data-ttu-id="455e6-285">Как создать акселератор пакетов</span><span class="sxs-lookup"><span data-stu-id="455e6-285">How to Create a Package Accelerator</span></span>](how-to-create-a-package-accelerator.md)

[<span data-ttu-id="455e6-286">Создание пакета виртуального приложения с помощью ускорителя пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="455e6-286">How to Create a Virtual Application Package Using an App-V Package Accelerator</span></span>](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## <span data-ttu-id="455e6-287">Отчеты об ошибках секвенсора</span><span class="sxs-lookup"><span data-stu-id="455e6-287">Sequencer error reporting</span></span>


<span data-ttu-id="455e6-288">Программа Sequencer App-V 5,0 может определять распространенные проблемы, связанные с упорядочиванием, в процессе выполнения последовательности.</span><span class="sxs-lookup"><span data-stu-id="455e6-288">The App-V 5.0 Sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="455e6-289">На странице **отчета об установке** в конце мастера последовательностей отображаются диагностические сообщения, отнесенные на **ошибки**, **предупреждения**и **сведения** в зависимости от серьезности проблемы.</span><span class="sxs-lookup"><span data-stu-id="455e6-289">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="455e6-290">Кроме того, вы можете найти дополнительные сведения об ошибках, связанные с последовательностью, с помощью средства просмотра событий Windows.</span><span class="sxs-lookup"><span data-stu-id="455e6-290">You can also find additional information about sequencing errors using the Windows Event Viewer.</span></span>






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a><span data-ttu-id="455e6-291">Другие ресурсы для секвенсора App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="455e6-291">Other resources for the App-V 5.0 sequencer</span></span>


-   [<span data-ttu-id="455e6-292">Операции, связанные с администрированием и использованием App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="455e6-292">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





