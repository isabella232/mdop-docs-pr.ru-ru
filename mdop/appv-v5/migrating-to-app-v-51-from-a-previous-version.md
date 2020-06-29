---
title: Миграция на App-V 5.1 с предыдущей версии
description: Миграция на App-V 5.1 с предыдущей версии
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813552"
---
# <span data-ttu-id="9dcd2-103">Миграция на App-V 5.1 с предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="9dcd2-103">Migrating to App-V 5.1 from a Previous Version</span></span>


<span data-ttu-id="9dcd2-104">С помощью Microsoft Application Virtualization (App-V) 5,1 вы можете перенести существующую инфраструктуру App-V 4,6 или App-V 5,0 в более гибкую, интегрированную и удобную для управления инфраструктурой App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-104">With Microsoft Application Virtualization (App-V) 5.1, you can migrate your existing App-V 4.6 or App-V 5.0 infrastructure to the more flexible, integrated, and easier to manage App-V 5.1 infrastructure.</span></span>
<span data-ttu-id="9dcd2-105">Однако вы не можете выполнить миграцию непосредственно из App-V 4. x в App-V 5,1, поэтому сначала необходимо выполнить миграцию в App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-105">However, you cannot migrate directly from App-V 4.x to App-V 5.1, you must migrate to App-V 5.0 first.</span></span> <span data-ttu-id="9dcd2-106">Дополнительные сведения о переходе с App-V 4. x на App-V 5,0 можно найти в разделе [Переход с предыдущей версии](migrating-from-a-previous-version-app-v-50.md)</span><span class="sxs-lookup"><span data-stu-id="9dcd2-106">For more information on migrating from App-V 4.x to App-V 5.0, see [Migrating from a Previous Version](migrating-from-a-previous-version-app-v-50.md)</span></span>  

<span data-ttu-id="9dcd2-107">**Примечание**  Пакеты App-V 5,1 точно так же, как пакеты App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-107">**Note** App-V 5.1 packages are exactly the same as App-V 5.0 packages.</span></span> <span data-ttu-id="9dcd2-108">В разных версиях пакетов не было изменений, поэтому нет необходимости преобразовывать пакеты 5,0 App-V в пакеты App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-108">There has been no change in the package format between the versions and therefore, there is no need to convert App-V 5.0 packages to App-V 5.1 packages.</span></span>

<span data-ttu-id="9dcd2-109">Дополнительные сведения о различиях между App-V 4,6 и App-V 5,1 приведены в **разделе различия между разделом App-v 4,6 и App-v 5,0** [о приложении app-v 5,0](about-app-v-50.md).</span><span class="sxs-lookup"><span data-stu-id="9dcd2-109">For more information about the differences between App-V 4.6 and App-V 5.1, see the **Differences between App-V 4.6 and App-V 5.0 section** of [About App-V 5.0](about-app-v-50.md).</span></span>

 

## <a href="" id="bkmk-pkgconvimprove"></a><span data-ttu-id="9dcd2-110">Улучшенные возможности преобразователя пакетов для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="9dcd2-110">Improvements to the App-V 5.1 Package Converter</span></span>


<span data-ttu-id="9dcd2-111">Теперь можно использовать конвертер пакетов для преобразования пакетов приложений App-V 4,6, содержащих сценарии, а также сведений реестра и сценариев из исходного OSD-файлов, которые теперь включены в выходные данные преобразователя пакетов.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-111">You can now use the package converter to convert App-V 4.6 packages that contain scripts, and registry information and scripts from source .osd files are now included in package converter output.</span></span>

<span data-ttu-id="9dcd2-112">Вы также можете использовать `–OSDsToIncludeInPackage` параметр с `ConvertFrom-AppvLegacyPackage` командлетом, чтобы указать, какие сведения о OSD – файлах будут преобразованы и помещены в новый пакет.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-112">You can also use the `–OSDsToIncludeInPackage` parameter with the `ConvertFrom-AppvLegacyPackage` cmdlet to specify which .osd files’ information is converted and placed within the new package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dcd2-113">Новые возможности App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="9dcd2-113">New in App-V 5.1</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-114">До версии App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="9dcd2-114">Prior to App-V 5.1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-115">Новые XML-файлы создаются в соответствии с файлами OSD, связанными с пакетом. Эти файлы содержат следующие данные:</span><span class="sxs-lookup"><span data-stu-id="9dcd2-115">New .xml files are created corresponding to the .osd files associated with a package; these files include the following information:</span></span></p>
<ul>
<li><p><span data-ttu-id="9dcd2-116">переменные среды</span><span class="sxs-lookup"><span data-stu-id="9dcd2-116">environment variables</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-117">Горячие</span><span class="sxs-lookup"><span data-stu-id="9dcd2-117">shortcuts</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-118">сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="9dcd2-118">file type associations</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-119">сведения в реестре</span><span class="sxs-lookup"><span data-stu-id="9dcd2-119">registry information</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-120">сценарии</span><span class="sxs-lookup"><span data-stu-id="9dcd2-120">scripts</span></span></p></li>
</ul>
<p><span data-ttu-id="9dcd2-121">Теперь вы можете добавлять данные из подмножества OSD-файлов из исходного каталога в пакет с помощью <code>-OSDsToIncludeInPackage</code> параметра.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-121">You can now choose to add information from a subset of the .osd files in the source directory to the package using the <code>-OSDsToIncludeInPackage</code> parameter.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dcd2-122">Данные в реестре и сценарии, включенные в OSD-файлы, связанные с пакетом, не включены в выходные данные преобразователя пакетов.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-122">Registry information and scripts included in .osd files associated with a package were not included in package converter output.</span></span></p>
<p><span data-ttu-id="9dcd2-123">Преобразователь пакетов выполнит заполнение нового пакета данными из всех OSD файлов в исходном каталоге.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-123">The package converter would populate the new package with information from all of the .osd files in the source directory.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="9dcd2-124">Пример оператора преобразования</span><span class="sxs-lookup"><span data-stu-id="9dcd2-124">Example conversion statement</span></span>

<span data-ttu-id="9dcd2-125">Чтобы понять, как создан новый процесс, ознакомьтесь с приведенным ниже примером `ConvertFrom-AppvLegacyPackage` инструкции преобразователя пакетов.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-125">To understand the new process, review the following example `ConvertFrom-AppvLegacyPackage` package converter statement.</span></span>

**<span data-ttu-id="9dcd2-126">Если исходный каталог (\\\\OldPkgStore\\ContosoApp) включает следующее:</span><span class="sxs-lookup"><span data-stu-id="9dcd2-126">If the source directory (\\\\OldPkgStore\\ContosoApp) includes the following:</span></span>**

-   <span data-ttu-id="9dcd2-127">ContosoApp. SFT</span><span class="sxs-lookup"><span data-stu-id="9dcd2-127">ContosoApp.sft</span></span>

-   <span data-ttu-id="9dcd2-128">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="9dcd2-128">ContosoApp.msi</span></span>

-   <span data-ttu-id="9dcd2-129">ContosoApp.sprj</span><span class="sxs-lookup"><span data-stu-id="9dcd2-129">ContosoApp.sprj</span></span>

-   <span data-ttu-id="9dcd2-130">ContosoApp\_manifest.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-130">ContosoApp\_manifest.xml</span></span>

-   <span data-ttu-id="9dcd2-131">X. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-131">X.osd</span></span>

-   <span data-ttu-id="9dcd2-132">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-132">Y.osd</span></span>

-   <span data-ttu-id="9dcd2-133">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-133">Z.osd</span></span>

**<span data-ttu-id="9dcd2-134">И выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9dcd2-134">And you run this command:</span></span>**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**<span data-ttu-id="9dcd2-135">В целевом каталоге (\\\\NewPkgStore\\ContosoApp) будет создано следующее:</span><span class="sxs-lookup"><span data-stu-id="9dcd2-135">The following is created in the destination directory (\\\\NewPkgStore\\ContosoApp):</span></span>**

-   <span data-ttu-id="9dcd2-136">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="9dcd2-136">ContosoApp.appv</span></span>

-   <span data-ttu-id="9dcd2-137">ContosoApp.msi</span><span class="sxs-lookup"><span data-stu-id="9dcd2-137">ContosoApp.msi</span></span>

-   <span data-ttu-id="9dcd2-138">ContosoApp\_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-138">ContosoApp\_DeploymentConfig.xml</span></span>

-   <span data-ttu-id="9dcd2-139">ContosoApp\_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-139">ContosoApp\_UserConfig.xml</span></span>

-   <span data-ttu-id="9dcd2-140">X\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-140">X\_Config.xml</span></span>

-   <span data-ttu-id="9dcd2-141">Y\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-141">Y\_Config.xml</span></span>

-   <span data-ttu-id="9dcd2-142">Z\_Config.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-142">Z\_Config.xml</span></span>

**<span data-ttu-id="9dcd2-143">В приведенном выше примере:</span><span class="sxs-lookup"><span data-stu-id="9dcd2-143">In the above example:</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dcd2-144">Эти файлы исходного каталога...</span><span class="sxs-lookup"><span data-stu-id="9dcd2-144">These Source directory files…</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-145">... преобразуются в указанные конечные файлы каталогов...</span><span class="sxs-lookup"><span data-stu-id="9dcd2-145">…are converted to these Destination directory files…</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-146">... и будут содержать эти элементы</span><span class="sxs-lookup"><span data-stu-id="9dcd2-146">…and will contain these items</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-147">Описание</span><span class="sxs-lookup"><span data-stu-id="9dcd2-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p><span data-ttu-id="9dcd2-148">X. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-148">X.osd</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-149">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-149">Y.osd</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-150">Z. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-150">Z.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9dcd2-151">X_Config.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-151">X_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-152">Y_Config.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-152">Y_Config.xml</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-153">Z_Config.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-153">Z_Config.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9dcd2-154">Переменные среды</span><span class="sxs-lookup"><span data-stu-id="9dcd2-154">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-155">Горячие</span><span class="sxs-lookup"><span data-stu-id="9dcd2-155">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-156">Сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="9dcd2-156">File type associations</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-157">Сведения в реестре</span><span class="sxs-lookup"><span data-stu-id="9dcd2-157">Registry information</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-158">Скрипты</span><span class="sxs-lookup"><span data-stu-id="9dcd2-158">Scripts</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="9dcd2-159">Каждый файл. OSD преобразуется в отдельный соответствующий XML-файл, который содержит указанные здесь элементы в формате конфигурации развертывания App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-159">Each .osd file is converted to a separate, corresponding .xml file that contains the items listed here in App-V 5.1 deployment configuration format.</span></span> <span data-ttu-id="9dcd2-160">Эти элементы затем можно скопировать из этих XML-файлов и поместить в конфигурацию развертывания или файлы конфигурации пользователя по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-160">These items can then be copied from these .xml files and placed in the deployment configuration or user configuration files as desired.</span></span></p>
<p><span data-ttu-id="9dcd2-161">В этом примере три XML-файла, соответствующие трем файлам OSD, находятся в исходном каталоге.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-161">In this example, there are three .xml files, corresponding with the three .osd files in the source directory.</span></span> <span data-ttu-id="9dcd2-162">Каждый XML-файл состоит из переменных среды, ярлыков, сопоставлений типов файлов, данных реестра и сценариев в соответствующем ей файле. OSD.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-162">Each .xml file contains the environment variables, shortcuts, file type associations, registry information, and scripts in its corresponding .osd file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p><span data-ttu-id="9dcd2-163">X. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-163">X.osd</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-164">Y. OSD</span><span class="sxs-lookup"><span data-stu-id="9dcd2-164">Y.osd</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9dcd2-165">ContosoApp. AppV</span><span class="sxs-lookup"><span data-stu-id="9dcd2-165">ContosoApp.appv</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-166">ContosoApp_DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-166">ContosoApp_DeploymentConfig.xml</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-167">ContosoApp_UserConfig.xml</span><span class="sxs-lookup"><span data-stu-id="9dcd2-167">ContosoApp_UserConfig.xml</span></span></p></li>
</ul></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9dcd2-168">Переменные среды</span><span class="sxs-lookup"><span data-stu-id="9dcd2-168">Environment variables</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-169">Горячие</span><span class="sxs-lookup"><span data-stu-id="9dcd2-169">Shortcuts</span></span></p></li>
<li><p><span data-ttu-id="9dcd2-170">Сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="9dcd2-170">File type associations</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="9dcd2-171">Сведения из OSD файлов, указанных в <code>-OSDsToIncludeInPackage</code> параметре, преобразуются в пакет и размещаются в нем.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-171">The information from the .osd files specified in the <code>-OSDsToIncludeInPackage</code> parameter are converted and placed inside the package.</span></span> <span data-ttu-id="9dcd2-172">Затем преобразователь заполняет файл конфигурации развертывания и файл конфигурации пользователя содержимым пакета, так же как программа Sequencer App-V выполняет виртуализацию нового пакета.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-172">The converter then populates the deployment configuration file and the user configuration file with the contents of the package, just as App-V Sequencer does when sequencing a new package.</span></span></p>
<p><span data-ttu-id="9dcd2-173">В этом примере переменные среды, сочетания клавиш и сопоставления типов файлов, включенные в X. OSD и Y. OSD, были преобразованы и помещены в пакет App-V, а некоторые из этих сведений также включены в конфигурацию развертывания и файлы конфигурации пользователя.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-173">In this example, environment variables, shortcuts, and file type associations included in X.osd and Y.osd were converted and placed in the App-V package, and some of this information was also included in the deployment configuration and user configuration files.</span></span> <span data-ttu-id="9dcd2-174">Используются X. OSD и Y. OSD, так как они были включены в параметр в качестве аргументов <code>-OSDsToIncludeInPackage</code> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-174">X.osd and Y.osd were used because they were included as arguments to the <code>-OSDsToIncludeInPackage</code> parameter.</span></span> <span data-ttu-id="9dcd2-175">Информация из Z. OSD не включена в пакет, так как она не указана как один из этих аргументов.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-175">No information from Z.osd was included in the package, because it was not included as one of these arguments.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9dcd2-176">Преобразование пакетов, созданных с помощью более ранней версии App-V</span><span class="sxs-lookup"><span data-stu-id="9dcd2-176">Converting packages created using a prior version of App-V</span></span>


<span data-ttu-id="9dcd2-177">Используйте служебную программу преобразователя пакетов для обновления пакетов виртуальных приложений, созданных с помощью версий App-V, предшествующих приложению App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-177">Use the package converter utility to upgrade virtual application packages created using versions of App-V prior to App-V 5.0.</span></span> <span data-ttu-id="9dcd2-178">Преобразователь пакетов использует PowerShell для преобразования пакетов и может помочь автоматизировать процесс, если у вас много пакетов, требующих преобразования.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-178">The package converter uses PowerShell to convert packages and can help automate the process if you have many packages that require conversion.</span></span>

<span data-ttu-id="9dcd2-179">**Важно!**  После преобразования существующего пакета необходимо протестировать его перед развертыванием пакета, чтобы убедиться, что процесс преобразования прошел успешно.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-179">**Important** After you convert an existing package you should test the package prior to deploying the package to ensure the conversion process was successful.</span></span>

 

**<span data-ttu-id="9dcd2-180">Что нужно знать перед преобразованием существующих пакетов</span><span class="sxs-lookup"><span data-stu-id="9dcd2-180">What to know before you convert existing packages</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dcd2-181">Проблема</span><span class="sxs-lookup"><span data-stu-id="9dcd2-181">Issue</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-182">Обходной путь</span><span class="sxs-lookup"><span data-stu-id="9dcd2-182">Workaround</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-183">Виртуальные пакеты с использованием DSC не связаны после преобразования.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-183">Virtual packages using DSC are not linked after conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dcd2-184">Свяжите пакеты с помощью групп подключений.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-184">Link the packages using connection groups.</span></span> <span data-ttu-id="9dcd2-185">См <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> .: Управление группами подключений </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-185">See <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)">Managing Connection Groups</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dcd2-186">Конфликты переменных среды обнаружены во время преобразования.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-186">Environment variable conflicts are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dcd2-187">Устраните конфликты в связанном <strong> OSD </strong> файле.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-187">Resolve any conflicts in the associated <strong>.osd</strong> file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-188">При преобразовании обнаруживаются жестко запрограммированные пути.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-188">Hard-coded paths are detected during conversion.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dcd2-189">Жестко закодированные пути очень сложны для правильного преобразования.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-189">Hard-coded paths are difficult to convert correctly.</span></span> <span data-ttu-id="9dcd2-190">Преобразователь пакетов обнаружит и вернет пакеты с файлами, которые содержат жестко запрограммированные пути.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-190">The package converter will detect and return packages with files that contain hard-coded paths.</span></span> <span data-ttu-id="9dcd2-191">Просмотрите файл с жестко заданным путем и определите, требуется ли для него файл.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-191">View the file with the hard-coded path, and determine whether the package requires the file.</span></span> <span data-ttu-id="9dcd2-192">Если это так, рекомендуется повторно выполнить повторную последовательность пакета.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-192">If so, it is recommended to re-sequence the package.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9dcd2-193">При преобразовании проверки пакета на наличие неудачных файлов или ярлыков.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-193">When converting a package check for failing files or shortcuts.</span></span> <span data-ttu-id="9dcd2-194">Найдите элемент в пакете App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-194">Locate the item in App-V 4.6 package.</span></span> <span data-ttu-id="9dcd2-195">Возможно, он является жестко запрограммированным путем.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-195">It could possibly be a hard-coded path.</span></span> <span data-ttu-id="9dcd2-196">Преобразуйте путь.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-196">Convert the path.</span></span>

<span data-ttu-id="9dcd2-197">**Примечание**  Рекомендуется использовать секвенсор App-V 5,1 для преобразования критических приложений или приложений, которые должны использовать преимущества функций.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-197">**Note** It is recommended that you use the App-V 5.1 sequencer for converting critical applications or applications that need to take advantage of features.</span></span> <span data-ttu-id="9dcd2-198">Посмотрите, [как последовательное создание нового приложения с помощью App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="9dcd2-198">See, [How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).</span></span>

<span data-ttu-id="9dcd2-199">Если преобразованный пакет не открывается после его преобразования, рекомендуется также выполнить повторную последовательное индексирование приложения с помощью секвенсора App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-199">If a converted package does not open after you convert it, it is also recommended that you re-sequence the application using the App-V 5.1 sequencer.</span></span>

 

[<span data-ttu-id="9dcd2-200">Преобразование пакета, созданного в предыдущей версии App-V</span><span class="sxs-lookup"><span data-stu-id="9dcd2-200">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## <span data-ttu-id="9dcd2-201">Миграция клиентов</span><span class="sxs-lookup"><span data-stu-id="9dcd2-201">Migrating Clients</span></span>


<span data-ttu-id="9dcd2-202">В приведенной ниже таблице показан рекомендуемый метод обновления клиентов.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-202">The following table displays the recommended method for upgrading clients.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dcd2-203">Задача</span><span class="sxs-lookup"><span data-stu-id="9dcd2-203">Task</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-204">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="9dcd2-204">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-205">Обновите среду до последней версии App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="9dcd2-205">Upgrade your environment to the latest version of App-V4.6</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="9dcd2-206">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-206">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dcd2-207">Установите клиент App-V 5,1 с включенным параметром совместного существования.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-207">Install the App-V 5.1 client with co-existence enabled.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)"><span data-ttu-id="9dcd2-208">Развертывание приложения App-V 4,6 и клиента App-V 5,1 на том же компьютере </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-208">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-209">Последовательное и развертывание пакетов приложения App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-209">Sequence and roll out App-V 5.1 packages.</span></span> <span data-ttu-id="9dcd2-210">При необходимости можно отменить публикацию пакетов App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-210">As needed, unpublish App-V 4.6 packages.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)"><span data-ttu-id="9dcd2-211">Последовательность создания нового приложения с помощью App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-211">How to Sequence a New Application with App-V 5.1</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="9dcd2-212">**Важно!**  Для использования режима совместного существования должна быть установлена новейшая версия App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-212">**Important** You must be running the latest version of App-V4.6 to use coexistence mode.</span></span> <span data-ttu-id="9dcd2-213">Кроме того, при упорядочении пакета необходимо настроить параметр управления полномочиями, который находится в **конфигурации пользователя** , в разделе **Конфигурация пользователя** .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-213">Additionally, when you sequence a package, you must configure the Managing Authority setting, which is in the **User Configuration** is located in the **User Configuration** section.</span></span>

 

## <span data-ttu-id="9dcd2-214">Миграция полной инфраструктуры на сервер App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="9dcd2-214">Migrating the App-V 5.1 Server Full Infrastructure</span></span>


<span data-ttu-id="9dcd2-215">Прямой метод для обновления до полной инфраструктуры App-V 5,1 не существует.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-215">There is no direct method to upgrade to a full App-V 5.1 infrastructure.</span></span> <span data-ttu-id="9dcd2-216">Сведения об обновлении сервера App-V можно получить, используя сведения из следующего раздела.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-216">Use the information in the following section for information about upgrading the App-V server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9dcd2-217">Задача</span><span class="sxs-lookup"><span data-stu-id="9dcd2-217">Task</span></span></th>
<th align="left"><span data-ttu-id="9dcd2-218">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="9dcd2-218">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-219">Обновите среду до последней версии App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-219">Upgrade your environment to the latest version of App-V4.6.</span></span></p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)"><span data-ttu-id="9dcd2-220">Рекомендации по развертыванию и обновлению Application Virtualization </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-220">Application Virtualization Deployment and Upgrade Considerations</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dcd2-221">Развертывание версии приложения-V 5,1 клиента.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-221">Deploy App-V 5.1 version of the client.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="9dcd2-222">Развертывание клиента App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-222">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9dcd2-223">Установите приложение App-V 5,1 Server.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-223">Install App-V 5.1 server.</span></span></p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="9dcd2-224">Развертывание сервера App-V 5,1 </a> .</span><span class="sxs-lookup"><span data-stu-id="9dcd2-224">How to Deploy the App-V 5.1 Server</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9dcd2-225">Миграция существующих пакетов.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-225">Migrate existing packages.</span></span></p></td>
<td align="left"><p><span data-ttu-id="9dcd2-226">Ознакомьтесь с <strong> пакетами преобразования, созданными в более ранней версии раздела App-V </strong> этой статьи.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-226">See the <strong>Converting packages created using a prior version of App-V</strong> section of this article.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9dcd2-227">Дополнительные задачи миграции</span><span class="sxs-lookup"><span data-stu-id="9dcd2-227">Additional Migration tasks</span></span>


<span data-ttu-id="9dcd2-228">Вы также можете выполнить дополнительные задачи миграции, например повторно настроить конечные точки, а также открыть пакет, созданный с помощью более ранней версии на компьютере с клиентом App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-228">You can also perform additional migration tasks such as reconfiguring end points as well as opening a package created using a prior version on a computer running the App-V 5.1 client.</span></span> <span data-ttu-id="9dcd2-229">Ниже приведены ссылки на дополнительные сведения о выполнении этих задач.</span><span class="sxs-lookup"><span data-stu-id="9dcd2-229">The following links provide more information about performing these tasks.</span></span>

[<span data-ttu-id="9dcd2-230">Перенос точек расширения из пакета App-V 4.6 в преобразованный пакет App-V 5.1 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="9dcd2-230">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="9dcd2-231">Перенос точек расширения из пакета App-V 4.6 в App-V 5.1 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="9dcd2-231">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[<span data-ttu-id="9dcd2-232">Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для всех пользователей на указанном компьютере</span><span class="sxs-lookup"><span data-stu-id="9dcd2-232">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="9dcd2-233">Возврат точек расширения из пакета App-V 5.1 в пакет App-V 4.6 для конкретного пользователя</span><span class="sxs-lookup"><span data-stu-id="9dcd2-233">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## <span data-ttu-id="9dcd2-234">Другие ресурсы для выполнения задач миграции App-V</span><span class="sxs-lookup"><span data-stu-id="9dcd2-234">Other resources for performing App-V migration tasks</span></span>


[<span data-ttu-id="9dcd2-235">Операции, связанные с администрированием и использованием App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="9dcd2-235">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

[<span data-ttu-id="9dcd2-236">Упрощенная процедура обновления сервера управления для Microsoft App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="9dcd2-236">A simplified Microsoft App-V 5.1 Management Server upgrade procedure</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





