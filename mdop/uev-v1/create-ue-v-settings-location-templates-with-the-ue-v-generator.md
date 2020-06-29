---
title: Создайте шаблонов расположения параметров UE-V с помощью генератора UE-V
description: Создайте шаблонов расположения параметров UE-V с помощью генератора UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826642"
---
# <span data-ttu-id="ac457-103">Создайте шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="ac457-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="ac457-104">Microsoft User Experience Virtualization (UE-V) использует *шаблоны расположений параметров* для перемещения параметров приложения между компьютерами пользователей.</span><span class="sxs-lookup"><span data-stu-id="ac457-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="ac457-105">Некоторые шаблоны расположений стандартных параметров включены в виртуализацию взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="ac457-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="ac457-106">Вы также можете создавать, изменять и проверять шаблоны расположений настраиваемых параметров с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="ac457-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="ac457-107">Генератор UE-V наблюдает за приложением для выяснения и захвата расположений, в которых приложение сохраняет параметры.</span><span class="sxs-lookup"><span data-stu-id="ac457-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="ac457-108">Отслеживаемое приложение должно быть традиционным приложением.</span><span class="sxs-lookup"><span data-stu-id="ac457-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="ac457-109">Генератор UE-V не может создать шаблон расположения параметров из следующих типов приложений:</span><span class="sxs-lookup"><span data-stu-id="ac457-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="ac457-110">Виртуализированные приложения</span><span class="sxs-lookup"><span data-stu-id="ac457-110">Virtualized applications</span></span>

-   <span data-ttu-id="ac457-111">Приложение, предлагаемое в службах терминалов</span><span class="sxs-lookup"><span data-stu-id="ac457-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="ac457-112">Приложения Java</span><span class="sxs-lookup"><span data-stu-id="ac457-112">Java applications</span></span>

-   <span data-ttu-id="ac457-113">Приложения для Windows 8</span><span class="sxs-lookup"><span data-stu-id="ac457-113">Windows 8 applications</span></span>

<span data-ttu-id="ac457-114">**Примечание**  Шаблоны UE-V нельзя создавать из виртуализированных приложений и приложений служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="ac457-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="ac457-115">Однако параметры, синхронизированные с использованием шаблонов, можно применять к этим приложениям.</span><span class="sxs-lookup"><span data-stu-id="ac457-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="ac457-116">Чтобы создать шаблоны, поддерживающие инфраструктуру виртуальных рабочих столов (VDI) и приложения служб терминалов, откройте файл установщика Windows (MSI) для приложения с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="ac457-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="ac457-117">Исключенные расположения</span><span class="sxs-lookup"><span data-stu-id="ac457-117">Excluded Locations</span></span>**

<span data-ttu-id="ac457-118">В процессе обнаружения не учитываются места, в которых обычно хранятся файлы программного обеспечения приложения, которые не перемещаются между компьютерами или средами пользователей.</span><span class="sxs-lookup"><span data-stu-id="ac457-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="ac457-119">Исключены следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ac457-119">The following are excluded:</span></span>

-   <span data-ttu-id="ac457-120">Раздел HKEY \ _CURRENT \ _USER разделы реестра и файлы, к которым пользователь, выполнивший вход, не может записать значения</span><span class="sxs-lookup"><span data-stu-id="ac457-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="ac457-121">Раздел HKEY \ _CURRENT \ _USER разделы реестра и файлы, связанные с основными функциями операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="ac457-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="ac457-122">Все разделы реестра, расположенные в кусте HKEY \ _LOCAL \ _MACHINE</span><span class="sxs-lookup"><span data-stu-id="ac457-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="ac457-123">Файлы, расположенные в каталогах программных файлов</span><span class="sxs-lookup"><span data-stu-id="ac457-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="ac457-124">Файлы, находящиеся в списке Пользователи \ \ \ [имя пользователя \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="ac457-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="ac457-125">Файлы операционной системы Windows, расположенные в папке% systemroot%</span><span class="sxs-lookup"><span data-stu-id="ac457-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="ac457-126">Если для перемещения параметров приложения требуются разделы реестра и файлы, хранящиеся в этих исключенных расположениях, администраторы могут вручную добавить их в шаблон расположения параметров в процессе создания шаблона.</span><span class="sxs-lookup"><span data-stu-id="ac457-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="ac457-127">Создание шаблонов UE-V</span><span class="sxs-lookup"><span data-stu-id="ac457-127">Create UE-V templates</span></span>


<span data-ttu-id="ac457-128">Использование генератора UE-V для создания шаблонов расположений параметров для бизнес-приложений или других приложений.</span><span class="sxs-lookup"><span data-stu-id="ac457-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="ac457-129">После создания шаблона для приложения вы можете развернуть его на компьютерах, чтобы пользователи могли перемещать параметры для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="ac457-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="ac457-130">Создание шаблона расположения параметров UE-V с помощью UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="ac457-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="ac457-131">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft User Experience Virtualization**и выберите **генератор Microsoft Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="ac457-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="ac457-132">Нажмите кнопку **создать шаблон расположения параметров**.</span><span class="sxs-lookup"><span data-stu-id="ac457-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="ac457-133">Укажите приложение.</span><span class="sxs-lookup"><span data-stu-id="ac457-133">Specify the application.</span></span> <span data-ttu-id="ac457-134">Перейдите к файлу приложения (exe) или ярлыку приложения (. lnk), для которого вы хотите создать шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="ac457-135">Укажите аргументы командной строки, если таковые имеются, и рабочий каталог, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="ac457-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="ac457-136">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ac457-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="ac457-137">**Примечание**  Перед запуском приложения система отображает запрос на **контроль учетной записи пользователя**.</span><span class="sxs-lookup"><span data-stu-id="ac457-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="ac457-138">Для мониторинга параметров реестра и файлов, используемых приложением, требуется разрешение на их хранение.</span><span class="sxs-lookup"><span data-stu-id="ac457-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="ac457-139">После запуска приложения закройте приложение.</span><span class="sxs-lookup"><span data-stu-id="ac457-139">After the application starts, close the application.</span></span> <span data-ttu-id="ac457-140">Генератор UE-V записывает места, в которых приложение хранит параметры.</span><span class="sxs-lookup"><span data-stu-id="ac457-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="ac457-141">После завершения процесса нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="ac457-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="ac457-142">Просмотрите и установите флажки рядом с соответствующими параметрами реестра и расположениями файлов параметров для перемещения по этому приложению.</span><span class="sxs-lookup"><span data-stu-id="ac457-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="ac457-143">Список содержит две следующие категории для расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="ac457-144">**Стандартные**: параметры приложения, хранящиеся в реестре в разделах hKey \ _CURRENT \ _USER или в папках с файлами в разделе \ \ **Пользователи** \ \ \ [имя пользователя \] \ \ **AppData**  \\  **роуминг**.</span><span class="sxs-lookup"><span data-stu-id="ac457-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="ac457-145">Генератор UE-V включает эти параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac457-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="ac457-146">**Нестандартные**: параметры приложения, которые хранятся за пределами расположений, указанных в разделе Советы и рекомендации по хранению данных параметров (необязательно).</span><span class="sxs-lookup"><span data-stu-id="ac457-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="ac457-147">Сюда входят файлы и папки в разделе **Пользователи** \ \ \ [имя пользователя \] \ \ **AppData**  \\  **Local**.</span><span class="sxs-lookup"><span data-stu-id="ac457-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="ac457-148">Проверьте эти расположения, чтобы определить, нужно ли включать их в шаблон расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="ac457-149">Установите флажки расположения, чтобы включить их.</span><span class="sxs-lookup"><span data-stu-id="ac457-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="ac457-150">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="ac457-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="ac457-151">Просмотр и изменение **свойств**, расположений в **реестре** и расположений **файлов** для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="ac457-152">Измените следующие свойства на вкладке **Свойства** :</span><span class="sxs-lookup"><span data-stu-id="ac457-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="ac457-153">**Имя приложения**: имя приложения, которое написано в описании свойств файлов программы.</span><span class="sxs-lookup"><span data-stu-id="ac457-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="ac457-154">**Имя программы**: имя программы, которая берется из свойств файла программы.</span><span class="sxs-lookup"><span data-stu-id="ac457-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="ac457-155">Обычно это имя имеет расширение EXE.</span><span class="sxs-lookup"><span data-stu-id="ac457-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="ac457-156">**Версия продукта**: номер версии файла exe приложения.</span><span class="sxs-lookup"><span data-stu-id="ac457-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="ac457-157">Это свойство в сочетании с версией файла помогает определить, какие приложения предназначены для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="ac457-158">Это свойство принимает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="ac457-158">This property accepts a major version number.</span></span> <span data-ttu-id="ac457-159">Если это свойство не задано, шаблон расположений параметров будет применяться ко всем версиям продукта.</span><span class="sxs-lookup"><span data-stu-id="ac457-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="ac457-160">**Версия файла**: номер версии файла the.exe приложения.</span><span class="sxs-lookup"><span data-stu-id="ac457-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="ac457-161">Это свойство в сочетании с версией продукта помогает определить, какие приложения предназначены для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="ac457-162">Это свойство принимает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="ac457-162">This property accepts a major version number.</span></span> <span data-ttu-id="ac457-163">Если это свойство не задано, шаблон расположений параметров будет применяться ко всем версиям программы.</span><span class="sxs-lookup"><span data-stu-id="ac457-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="ac457-164">**Имя автора шаблона** (необязательно): имя автора шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="ac457-165">**Электронная почта автора шаблона** (необязательно): адрес электронной почты автора шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="ac457-166">На вкладке " **Реестр** " перечислены разделы **реестра и их** **область** , которые включены в шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="ac457-167">Измените расположение реестра с помощью раскрывающегося меню **Tasks (задачи** ).</span><span class="sxs-lookup"><span data-stu-id="ac457-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="ac457-168">Задачи включают в себя добавление новых клавиш, изменение имени или области существующих ключей, удаление разделов и Просмотр реестра, в котором находятся ключи.</span><span class="sxs-lookup"><span data-stu-id="ac457-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="ac457-169">Используйте область " **все параметры** ", чтобы включить все параметры реестра в указанном разделе.</span><span class="sxs-lookup"><span data-stu-id="ac457-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="ac457-170">Используйте **все параметры и подразделы** для включения всех параметров реестра в заданные раздел, подразделы и параметры подраздела.</span><span class="sxs-lookup"><span data-stu-id="ac457-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="ac457-171">На вкладке " **файлы** " перечислены путь к файлу и его маска для расположений файлов, включенных в шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="ac457-172">Измените расположение файлов с помощью раскрывающегося меню **Tasks (задачи** ).</span><span class="sxs-lookup"><span data-stu-id="ac457-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="ac457-173">Задачи для расположений файлов включают добавление новых файлов и папок, изменение области существующих файлов и папок, удаление файлов и папок, а также открытие выбранного расположения в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="ac457-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="ac457-174">Чтобы включить все файлы в указанную папку, оставьте пустую маску файла.</span><span class="sxs-lookup"><span data-stu-id="ac457-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="ac457-175">Нажмите кнопку **создать** и сохраните шаблон расположения параметров на компьютере.</span><span class="sxs-lookup"><span data-stu-id="ac457-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="ac457-176">Нажмите кнопку **Закрыть** , чтобы закрыть окно мастера шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="ac457-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="ac457-177">Выйдите из приложения генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="ac457-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="ac457-178">После создания шаблона расположения параметров для приложения необходимо протестировать этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="ac457-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="ac457-179">Разверните шаблон в лабораторной среде, прежде чем переводить его в эксплуатацию на предприятии.</span><span class="sxs-lookup"><span data-stu-id="ac457-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="ac457-180">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ac457-180">Related topics</span></span>


[<span data-ttu-id="ac457-181">Работа с пользовательскими шаблонами UE-V и генератором UE-V</span><span class="sxs-lookup"><span data-stu-id="ac457-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="ac457-182">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="ac457-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





