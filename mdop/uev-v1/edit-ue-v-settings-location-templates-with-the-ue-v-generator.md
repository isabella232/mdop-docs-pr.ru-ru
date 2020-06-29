---
title: Изменение шаблонов расположения параметров UE-V с помощью генератора UE-V
description: Изменение шаблонов расположения параметров UE-V с помощью генератора UE-V
author: dansimp
ms.assetid: da78f9c8-1624-4111-8c96-79db7224bd0b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7b90cd58761e6ac40c089f3afeade3c445a52ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827112"
---
# <span data-ttu-id="81c7d-103">Изменение шаблонов расположения параметров UE-V с помощью генератора UE-V</span><span class="sxs-lookup"><span data-stu-id="81c7d-103">Edit UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="81c7d-104">Используйте генератор Microsoft User Experience Virtualization (UE-V) для редактирования шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-104">Use the Microsoft User Experience Virtualization (UE-V) Generator to edit settings location templates.</span></span> <span data-ttu-id="81c7d-105">Когда измененные параметры добавляются в шаблоны с помощью генератора UE-V, информация о версии в шаблоне автоматически обновляется, чтобы убедиться, что все существующие шаблоны, развернутые в корпоративной среде, обновлены правильно.</span><span class="sxs-lookup"><span data-stu-id="81c7d-105">When the revised settings are added to the templates using the UE-V Generator, the version information within the template is automatically updated to ensure that any existing templates deployed in the enterprise are updated correctly.</span></span>

**<span data-ttu-id="81c7d-106">Изменение шаблона расположения параметров UE-V с помощью UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="81c7d-106">How to edit a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="81c7d-107">Нажмите кнопку **Пуск**, выберите **все программы**, а затем — **Microsoft User Experience Virtualization**и выберите **генератор Microsoft Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="81c7d-107">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="81c7d-108">Щелкните **изменить шаблон расположения параметров**.</span><span class="sxs-lookup"><span data-stu-id="81c7d-108">Click **Edit a settings location template**.</span></span>

3.  <span data-ttu-id="81c7d-109">В списке последних использованных шаблонов выберите шаблон, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="81c7d-109">In the list of recently used templates, select the template to be edited.</span></span> <span data-ttu-id="81c7d-110">Кроме того, можно **Перейти** к файлу шаблона параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-110">Alternatively, **Browse** to the settings template file.</span></span> <span data-ttu-id="81c7d-111">Чтобы продолжить, нажмите **Далее**.</span><span class="sxs-lookup"><span data-stu-id="81c7d-111">Click **Next** to continue.</span></span>

4.  <span data-ttu-id="81c7d-112">Проверьте **Свойства**, расположения в **реестре** и расположение **файлов** для шаблона параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-112">Review the **Properties**, **Registry** locations, and **Files** locations for the settings template.</span></span> <span data-ttu-id="81c7d-113">Внесите необходимые изменения.</span><span class="sxs-lookup"><span data-stu-id="81c7d-113">Edit as needed.</span></span>

    -   <span data-ttu-id="81c7d-114">Вкладка **Свойства** позволяет просматривать и изменять следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="81c7d-114">The **Properties** tab allows you to view and edit the following properties:</span></span>

        -   <span data-ttu-id="81c7d-115">**Имя приложения**: имя приложения, которое написано в описании свойств файла программы.</span><span class="sxs-lookup"><span data-stu-id="81c7d-115">**Application name**: The application name written in the description of the program file properties.</span></span>

        -   <span data-ttu-id="81c7d-116">**Имя программы**: имя программы, которая берется из свойств файла программы.</span><span class="sxs-lookup"><span data-stu-id="81c7d-116">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="81c7d-117">Обычно это имя имеет расширение EXE.</span><span class="sxs-lookup"><span data-stu-id="81c7d-117">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="81c7d-118">**Версия продукта**: номер версии файла exe приложения.</span><span class="sxs-lookup"><span data-stu-id="81c7d-118">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="81c7d-119">Это свойство вместе с **версией файла**помогает определить, какие приложения предназначены для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-119">This property, together with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="81c7d-120">Это свойство принимает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="81c7d-120">This property accepts a major version number.</span></span> <span data-ttu-id="81c7d-121">Если это свойство не задано, шаблон расположений параметров будет применяться ко всем версиям продукта.</span><span class="sxs-lookup"><span data-stu-id="81c7d-121">If this property is empty, then the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="81c7d-122">**Версия файла**: номер версии файла the.exe приложения.</span><span class="sxs-lookup"><span data-stu-id="81c7d-122">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="81c7d-123">Это свойство вместе с **версией продукта**помогает определить, какие приложения предназначены для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-123">This property, along with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="81c7d-124">Это свойство принимает основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="81c7d-124">This property accepts a major version number.</span></span> <span data-ttu-id="81c7d-125">Если это свойство не задано, шаблон расположений параметров будет применяться ко всем версиям программы.</span><span class="sxs-lookup"><span data-stu-id="81c7d-125">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="81c7d-126">**Имя автора шаблона** (необязательно): имя автора шаблона параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-126">**Template author name** (optional): The name of the settings template author.</span></span>

        -   <span data-ttu-id="81c7d-127">**Электронная почта автора шаблона** (необязательно): адрес электронной почты автора шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-127">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="81c7d-128">На вкладке " **Реестр** " перечислены разделы **реестра и их** **область** , которые включены в шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-128">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="81c7d-129">Вы можете изменить расположение реестра с помощью раскрывающегося меню **Tasks (задачи** ).</span><span class="sxs-lookup"><span data-stu-id="81c7d-129">You can edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="81c7d-130">Задачи включают в себя добавление новых клавиш, изменение имени или области существующих ключей, удаление разделов и Просмотр реестра, в котором находятся ключи.</span><span class="sxs-lookup"><span data-stu-id="81c7d-130">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry in which the keys are located.</span></span> <span data-ttu-id="81c7d-131">Когда вы определяете область для реестра, вы можете использовать область " **все параметры** ", чтобы включить все параметры реестра в указанном разделе.</span><span class="sxs-lookup"><span data-stu-id="81c7d-131">When you define the scope for the registry, you can use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="81c7d-132">Используйте **все параметры** и **подразделы** для включения всех параметров реестра в заданные раздел, подразделы и параметры подраздела.</span><span class="sxs-lookup"><span data-stu-id="81c7d-132">Use **All Settings** and **Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="81c7d-133">На вкладке " **файлы** " перечислены путь к файлу и его маска для расположений файлов, включенных в шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-133">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="81c7d-134">Расположение файлов можно изменить с помощью раскрывающегося меню " **задачи** ".</span><span class="sxs-lookup"><span data-stu-id="81c7d-134">You can edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="81c7d-135">Задачи для расположений файлов включают добавление новых файлов и папок, изменение области существующих файлов и папок, удаление файлов и папок, а также открытие выбранного расположения в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="81c7d-135">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="81c7d-136">Чтобы включить все файлы в указанную папку, оставьте маску файла пустой.</span><span class="sxs-lookup"><span data-stu-id="81c7d-136">To include all files in the specified folder, leave the file mask empty.</span></span>

5.  <span data-ttu-id="81c7d-137">Нажмите кнопку **сохранить** , чтобы сохранить изменения в шаблоне расположение параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-137">Click **Save** to save the changes to the settings location template.</span></span>

6.  <span data-ttu-id="81c7d-138">Нажмите кнопку **Закрыть** , чтобы закрыть окно мастера шаблонов параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-138">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="81c7d-139">Выйдите из приложения генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="81c7d-139">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="81c7d-140">После изменения шаблона расположения параметров для приложения необходимо протестировать этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="81c7d-140">After editing the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="81c7d-141">Разверните пересмотренный шаблон расположений параметров в лабораторной среде, прежде чем переводить его в эксплуатацию на предприятии.</span><span class="sxs-lookup"><span data-stu-id="81c7d-141">Deploy the revised settings location template in a lab environment before putting it into production in the enterprise.</span></span>

**<span data-ttu-id="81c7d-142">Редактирование шаблона расположений параметров вручную</span><span class="sxs-lookup"><span data-stu-id="81c7d-142">How to manually edit a settings location template</span></span>**

1.  <span data-ttu-id="81c7d-143">Создайте локальную копию шаблона расположения параметров (XML-файл).</span><span class="sxs-lookup"><span data-stu-id="81c7d-143">Create a local copy of the settings location template (.xml file).</span></span> <span data-ttu-id="81c7d-144">UE-V Templates Locations — это XML-файлы, указывающие на расположение, в котором значения параметров в магазине приложений.</span><span class="sxs-lookup"><span data-stu-id="81c7d-144">UE-V settings location templates are .xml files identifying the locations where application store settings values.</span></span>

2.  <span data-ttu-id="81c7d-145">Откройте файл шаблона расположения параметров с помощью редактора XML.</span><span class="sxs-lookup"><span data-stu-id="81c7d-145">Open the settings location template file with an XML editor.</span></span>

3.  <span data-ttu-id="81c7d-146">Измените файл шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="81c7d-146">Edit the settings location template file.</span></span> <span data-ttu-id="81c7d-147">Все изменения должны соответствовать файлу схемы UE-V, определенному в SettingsLocationTempate. xsd.</span><span class="sxs-lookup"><span data-stu-id="81c7d-147">All changes must conform to the UE-V schema file defined in SettingsLocationTempate.xsd.</span></span> <span data-ttu-id="81c7d-148">Копия XSD-файла по умолчанию находится в разделе `\ProgramData\Microsoft\UEV\Templates` .</span><span class="sxs-lookup"><span data-stu-id="81c7d-148">A copy of the .xsd file is located in `\ProgramData\Microsoft\UEV\Templates` by default.</span></span>

4.  <span data-ttu-id="81c7d-149">Сохраните файл шаблона расположения параметров и закройте редактор XML.</span><span class="sxs-lookup"><span data-stu-id="81c7d-149">Save the settings location template file and close the XML editor.</span></span>

5.  <span data-ttu-id="81c7d-150">Проверка измененного файла шаблона расположения параметров с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="81c7d-150">Validate the modified settings location template file with the UE-V Generator.</span></span> <span data-ttu-id="81c7d-151">Дополнительные сведения о проверке с помощью генератора UE-V можно найти [в разделе Проверка шаблонов расположений параметров ue-v с помощью генератора UE-v](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span><span class="sxs-lookup"><span data-stu-id="81c7d-151">For more information about validating with the UE-V Generator, see [Validate UE-V Settings Location Templates with UE-V Generator](validate-ue-v-settings-location-templates-with-ue-v-generator.md).</span></span>

## <span data-ttu-id="81c7d-152">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="81c7d-152">Related topics</span></span>


[<span data-ttu-id="81c7d-153">Работа с пользовательскими шаблонами UE-V и генератором UE-V</span><span class="sxs-lookup"><span data-stu-id="81c7d-153">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="81c7d-154">Операции в UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="81c7d-154">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





