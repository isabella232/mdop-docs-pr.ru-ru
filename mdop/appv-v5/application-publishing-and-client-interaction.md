---
title: Публикация приложений и взаимодействие с клиентом
description: Публикация приложений и взаимодействие с клиентом
author: dansimp
ms.assetid: c69a724a-85d1-4e2d-94a2-7ffe0b47d971
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b6080a501a8fdd2a39876ff979aa7a2982c76bbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814736"
---
# <span data-ttu-id="83c5c-103">Публикация приложений и взаимодействие с клиентом</span><span class="sxs-lookup"><span data-stu-id="83c5c-103">Application Publishing and Client Interaction</span></span>


<span data-ttu-id="83c5c-104">В этой статье приводятся технические сведения об общих операциях клиента App-V и их интеграции с локальной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="83c5c-104">This article provides technical information about common App-V client operations and their integration with the local operating system.</span></span>

-   [<span data-ttu-id="83c5c-105">Файлы пакета App-V, созданные секвенсором</span><span class="sxs-lookup"><span data-stu-id="83c5c-105">App-V package files created by the Sequencer</span></span>](#bkmk-appv-pkg-files-list)

-   [<span data-ttu-id="83c5c-106">Что находится в файле AppV?</span><span class="sxs-lookup"><span data-stu-id="83c5c-106">What’s in the appv file?</span></span>](#bkmk-appv-file-contents)

-   [<span data-ttu-id="83c5c-107">Места хранения данных клиента App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-107">App-V client data storage locations</span></span>](#bkmk-files-data-storage)

-   [<span data-ttu-id="83c5c-108">Реестр пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-108">Package registry</span></span>](#bkmk-pkg-registry)

-   [<span data-ttu-id="83c5c-109">Поведение хранилища пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-109">App-V package store behavior</span></span>](#bkmk-pkg-store-behavior)

-   [<span data-ttu-id="83c5c-110">Перемещаемый реестр и данные</span><span class="sxs-lookup"><span data-stu-id="83c5c-110">Roaming registry and data</span></span>](#bkmk-roaming-reg-data)

-   [<span data-ttu-id="83c5c-111">Управление жизненным циклом в клиентском приложении App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-111">App-V client application lifecycle management</span></span>](#bkmk-clt-app-lifecycle)

-   [<span data-ttu-id="83c5c-112">Интеграция пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-112">Integration of App-V packages</span></span>](#bkmk-integr-appv-pkgs)

-   [<span data-ttu-id="83c5c-113">Динамическая обработка конфигурации</span><span class="sxs-lookup"><span data-stu-id="83c5c-113">Dynamic configuration processing</span></span>](#bkmk-dynamic-config)

-   [<span data-ttu-id="83c5c-114">Параллельные сборки</span><span class="sxs-lookup"><span data-stu-id="83c5c-114">Side-by-side assemblies</span></span>](#bkmk-sidebyside-assemblies)

-   [<span data-ttu-id="83c5c-115">Ведение журнала на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="83c5c-115">Client logging</span></span>](#bkmk-client-logging)

<span data-ttu-id="83c5c-116">Дополнительные сведения можно найти в разделе [ресурсы документации Microsoft Application Virtualization (App-V) download page](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="83c5c-116">For additional reference information, see [Microsoft Application Virtualization (App-V) Documentation Resources Download Page](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-pkg-files-list"></a><span data-ttu-id="83c5c-117">Файлы пакета App-V, созданные секвенсором</span><span class="sxs-lookup"><span data-stu-id="83c5c-117">App-V package files created by the Sequencer</span></span>


<span data-ttu-id="83c5c-118">Секвенсор создает пакеты App-V и создает виртуализированное приложение.</span><span class="sxs-lookup"><span data-stu-id="83c5c-118">The Sequencer creates App-V packages and produces a virtualized application.</span></span> <span data-ttu-id="83c5c-119">В процессе упорядочивания создаются следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="83c5c-119">The sequencing process creates the following files:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-120">Файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-120">File</span></span></th>
<th align="left"><span data-ttu-id="83c5c-121">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-122">. AppV</span><span class="sxs-lookup"><span data-stu-id="83c5c-122">.appv</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-123">Основной файл пакета, который включает собранные ресурсы и сведения о состоянии из процесса упорядочения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-123">The primary package file, which contains the captured assets and state information from the sequencing process.</span></span></p></li>
<li><p><span data-ttu-id="83c5c-124">Архитектура файла пакета, сведения о публикации и реестр в маркерной форме, которая может быть повторно применена к компьютеру и определенному пользователю при доставке.</span><span class="sxs-lookup"><span data-stu-id="83c5c-124">Architecture of the package file, publishing information, and registry in a tokenized form that can be reapplied to a machine and to a specific user upon delivery.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-125">. УСТАНОВЩИКА</span><span class="sxs-lookup"><span data-stu-id="83c5c-125">.MSI</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-126">Исполняемая обертка развертывания, которую можно использовать для развертывания AppV-файлов вручную или с помощью сторонней платформы развертывания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-126">Executable deployment wrapper that you can use to deploy .appv files manually or by using a third-party deployment platform.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-127">_DeploymentConfig.XML</span><span class="sxs-lookup"><span data-stu-id="83c5c-127">_DeploymentConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-128">Файл, который используется для настройки параметров публикации по умолчанию для всех приложений в пакете, который развертывается глобально для всех пользователей на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-128">File used to customize the default publishing parameters for all applications in a package that is deployed globally to all users on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-129">_UserConfig.XML</span><span class="sxs-lookup"><span data-stu-id="83c5c-129">_UserConfig.XML</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-130">Файл, который используется для настройки параметров публикации для всех приложений в пакете, развернутого для определенного пользователя на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-130">File used to customize the publishing parameters for all applications in a package that is a deployed to a specific user on a computer that is running the App-V client.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-131">Report.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-131">Report.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-132">Сводка сообщений, которые приводили к процессу последовательности, включая пропущенные драйверы, файлы и расположения в реестре.</span><span class="sxs-lookup"><span data-stu-id="83c5c-132">Summary of messages resulting from the sequencing process, including omitted drivers, files, and registry locations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-133">. ФОРМАТЕ</span><span class="sxs-lookup"><span data-stu-id="83c5c-133">.CAB</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="83c5c-134">Необязательный: </em> файл ускорителя пакетов, используемый для автоматического перестроения ранее упорядоченного виртуального пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-134">Optional:</em> Package accelerator file used to automatically rebuild a previously sequenced virtual application package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-135">.appvt</span><span class="sxs-lookup"><span data-stu-id="83c5c-135">.appvt</span></span></p></td>
<td align="left"><p><em><span data-ttu-id="83c5c-136">Необязательный: </em> файл шаблона Sequencer, используемый для хранения часто используемых параметров секвенсора.</span><span class="sxs-lookup"><span data-stu-id="83c5c-136">Optional:</em> Sequencer template file used to retain commonly reused Sequencer settings.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83c5c-137">Сведения о последовательностях можно найти в [руководстве Виртуализация приложений 5,0](https://www.microsoft.com/download/details.aspx?id=27760).</span><span class="sxs-lookup"><span data-stu-id="83c5c-137">For information about sequencing, see [Application Virtualization 5.0 Sequencing Guide](https://www.microsoft.com/download/details.aspx?id=27760).</span></span>

## <a href="" id="bkmk-appv-file-contents"></a><span data-ttu-id="83c5c-138">Что находится в файле AppV?</span><span class="sxs-lookup"><span data-stu-id="83c5c-138">What’s in the appv file?</span></span>


<span data-ttu-id="83c5c-139">Файл AppV является контейнером, в котором хранятся XML-и неxml-файлы вместе в одной сущности.</span><span class="sxs-lookup"><span data-stu-id="83c5c-139">The appv file is a container that stores XML and non-XML files together in a single entity.</span></span> <span data-ttu-id="83c5c-140">Этот файл строится на основе формата AppX, который основан на стандартах Open Packaging Conventions (OPC).</span><span class="sxs-lookup"><span data-stu-id="83c5c-140">This file is built from the AppX format, which is based on the Open Packaging Conventions (OPC) standard.</span></span>

<span data-ttu-id="83c5c-141">Чтобы просмотреть содержимое файла AppV, сделайте копию пакета, а затем переименуйте копируемый файл на расширение ZIP.</span><span class="sxs-lookup"><span data-stu-id="83c5c-141">To view the appv file contents, make a copy of the package, and then rename the copied file to a ZIP extension.</span></span>

<span data-ttu-id="83c5c-142">В файле AppV находятся следующие папки и файлы, которые используются при создании и публикации виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-142">The appv file contains the following folder and files, which are used when creating and publishing a virtual application:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-143">Имя</span><span class="sxs-lookup"><span data-stu-id="83c5c-143">Name</span></span></th>
<th align="left"><span data-ttu-id="83c5c-144">Тип</span><span class="sxs-lookup"><span data-stu-id="83c5c-144">Type</span></span></th>
<th align="left"><span data-ttu-id="83c5c-145">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-145">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-146">Корень</span><span class="sxs-lookup"><span data-stu-id="83c5c-146">Root</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-147">Папка файла</span><span class="sxs-lookup"><span data-stu-id="83c5c-147">File folder</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-148">Каталог, содержащий файловую систему для виртуализированного приложения, которое захватывается во время упорядочения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-148">Directory that contains the file system for the virtualized application that is captured during sequencing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-149">[Content_Types]. XML</span><span class="sxs-lookup"><span data-stu-id="83c5c-149">[Content_Types].xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-150">XML-файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-150">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-151">Список основных типов контента в AppV-файле (например, DLL, EXE, BIN).</span><span class="sxs-lookup"><span data-stu-id="83c5c-151">List of the core content types in the appv file (e.g. DLL, EXE, BIN).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-152">AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-152">AppxBlockMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-153">XML-файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-153">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-154">Макет файла AppV, в котором используются элементы File, Block и BlockMap, которые обеспечивают расположение и проверку файлов в пакете App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-154">Layout of the appv file, which uses File, Block, and BlockMap elements that enable location and validation of files in the App-V package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-155">AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-155">AppxManifest.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-156">XML-файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-156">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-157">Метаданные для пакета, которые содержат необходимые сведения для добавления, публикации и запуска пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-157">Metadata for the package that contains the required information for adding, publishing, and launching the package.</span></span> <span data-ttu-id="83c5c-158">Включает точки расширения (сопоставления и сочетания для типов файлов), а также имена и GUID, связанные с пакетом.</span><span class="sxs-lookup"><span data-stu-id="83c5c-158">Includes extension points (file type associations and shortcuts) and the names and GUIDs associated with the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-159">FilesystemMetadata.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-159">FilesystemMetadata.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-160">XML-файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-160">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-161">Список файлов, собранных в ходе последовательности, включая атрибуты (например, каталоги, файлы, непрозрачные каталоги, пустые каталоги и длинные и короткие имена).</span><span class="sxs-lookup"><span data-stu-id="83c5c-161">List of the files captured during sequencing, including attributes (e.g., directories, files, opaque directories, empty directories,and long and short names).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-162">PackageHistory.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-162">PackageHistory.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-163">XML-файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-163">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-164">Сведения о компьютере виртуализации (версия операционной системы, версия Internet Explorer, версия .NET Framework) и процесс (обновление, версия пакета).</span><span class="sxs-lookup"><span data-stu-id="83c5c-164">Information about the sequencing computer (operating system version, Internet Explorer version, .Net Framework version) and process (upgrade, package version).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-165">Registry. dat</span><span class="sxs-lookup"><span data-stu-id="83c5c-165">Registry.dat</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-166">DAT файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-166">DAT File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-167">Разделы реестра и значения, захваченные во время процесса упорядочения для пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-167">Registry keys and values captured during the sequencing process for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-168">StreamMap.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-168">StreamMap.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-169">XML-файл</span><span class="sxs-lookup"><span data-stu-id="83c5c-169">XML File</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-170">Список файлов для основного и функционального блоков публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-170">List of files for the primary and publishing feature block.</span></span> <span data-ttu-id="83c5c-171">Функциональный блок публикации включает в себя ICO-файлы и необходимые части файлов (EXE и DLL) для публикации пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-171">The publishing feature block contains the ICO files and required portions of files (EXE and DLL) for publishing the package.</span></span> <span data-ttu-id="83c5c-172">При наличии основного блока функций включает файлы, которые были оптимизированы для потоковой передачи в процессе упорядочивания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-172">When present, the primary feature block includes files that have been optimized for streaming during the sequencing process.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-files-data-storage"></a><span data-ttu-id="83c5c-173">Места хранения данных клиента App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-173">App-V client data storage locations</span></span>


<span data-ttu-id="83c5c-174">Клиент App-V выполняет задачи, чтобы убедиться, что виртуальные приложения работают должным образом и работают как локально установленные приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-174">The App-V client performs tasks to ensure that virtual applications run properly and work like locally installed applications.</span></span> <span data-ttu-id="83c5c-175">Для открытия и запуска виртуальных приложений требуется сопоставление в виртуальной файловой системе и реестре, чтобы убедиться, что приложение содержит необходимые компоненты традиционного приложения, ожидаемые пользователями.</span><span class="sxs-lookup"><span data-stu-id="83c5c-175">The process of opening and running virtual applications requires mapping from the virtual file system and registry to ensure the application has the required components of a traditional application expected by users.</span></span> <span data-ttu-id="83c5c-176">В этом разделе описаны ресурсы, необходимые для запуска виртуальных приложений, и перечислены расположения, в которых App-V хранит ресурсы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-176">This section describes the assets that are required to run virtual applications and lists the location where App-V stores the assets.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-177">Имя</span><span class="sxs-lookup"><span data-stu-id="83c5c-177">Name</span></span></th>
<th align="left"><span data-ttu-id="83c5c-178">Расположение</span><span class="sxs-lookup"><span data-stu-id="83c5c-178">Location</span></span></th>
<th align="left"><span data-ttu-id="83c5c-179">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-179">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-180">Хранилище пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-180">Package Store</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-181">%ProgramData%\App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-181">%ProgramData%\App-V</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-182">Расположение по умолчанию для файлов пакетов только для чтения</span><span class="sxs-lookup"><span data-stu-id="83c5c-182">Default location for read only package files</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-183">Каталог компьютера</span><span class="sxs-lookup"><span data-stu-id="83c5c-183">Machine Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="83c5c-184">%ProgramData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-185">Содержимое документов конфигурации для компьютера</span><span class="sxs-lookup"><span data-stu-id="83c5c-185">Contains per-machine configuration documents</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-186">Каталог пользователей</span><span class="sxs-lookup"><span data-stu-id="83c5c-186">User Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-187">%AppData%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="83c5c-187">%AppData%\Microsoft\AppV\Client\Catalog</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-188">Содержат документы конфигурации для отдельных пользователей</span><span class="sxs-lookup"><span data-stu-id="83c5c-188">Contains per-user configuration documents</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-189">Резервные копии ярлыков</span><span class="sxs-lookup"><span data-stu-id="83c5c-189">Shortcut Backups</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span><span class="sxs-lookup"><span data-stu-id="83c5c-190">%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-191">Хранит предыдущие точки интеграции, которые обеспечивают восстановление пакета в процессе отмены публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-191">Stores previous integration points that enable restore on package unpublish</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-192">Копирование при записи в роуминге (COW)</span><span class="sxs-lookup"><span data-stu-id="83c5c-192">Copy on Write (COW) Roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-193">%AppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="83c5c-193">%AppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-194">Перемещаемое расположение для записи для изменения пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-194">Writeable roaming location for package modification</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-195">Локальное копирование на запись (COW)</span><span class="sxs-lookup"><span data-stu-id="83c5c-195">Copy on Write (COW) Local</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span><span class="sxs-lookup"><span data-stu-id="83c5c-196">%LocalAppData%\Microsoft\AppV\Client\VFS</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-197">Расположение для записи, которое не является перемещаемым, для изменения пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-197">Writeable non-roaming location for package modification</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-198">Реестр компьютера</span><span class="sxs-lookup"><span data-stu-id="83c5c-198">Machine Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-199">HKLM\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="83c5c-199">HKLM\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-200">Содержит сведения о состоянии пакета, включая VReg для компьютера или глобально опубликованных пакетов (куст машины).</span><span class="sxs-lookup"><span data-stu-id="83c5c-200">Contains package state information, including VReg for machine or globally published packages (Machine hive)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-201">Реестр пользователя</span><span class="sxs-lookup"><span data-stu-id="83c5c-201">User Registry</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-202">HKCU\Software\Microsoft\AppV</span><span class="sxs-lookup"><span data-stu-id="83c5c-202">HKCU\Software\Microsoft\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-203">Содержит сведения о состоянии пользовательского пакета, включая VReg</span><span class="sxs-lookup"><span data-stu-id="83c5c-203">Contains user package state information including VReg</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-204">Пользовательские классы реестра</span><span class="sxs-lookup"><span data-stu-id="83c5c-204">User Registry Classes</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-205">HKCU\Software\Classes\AppV</span><span class="sxs-lookup"><span data-stu-id="83c5c-205">HKCU\Software\Classes\AppV</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-206">Содержат дополнительные сведения о состоянии пользовательского пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-206">Contains additional user package state information</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83c5c-207">Дополнительные сведения о таблице приведены в разделе ниже и на протяжении всего документа.</span><span class="sxs-lookup"><span data-stu-id="83c5c-207">Additional details for the table are provided in the section below and throughout the document.</span></span>

### <span data-ttu-id="83c5c-208">Хранилище пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-208">Package store</span></span>

<span data-ttu-id="83c5c-209">Клиент App-V управляет активами приложений, смонтированными в магазине пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-209">The App-V Client manages the applications assets mounted in the package store.</span></span> <span data-ttu-id="83c5c-210">Это место хранения по умолчанию `%ProgramData%\App-V` , но вы можете настроить его во время или после установки с помощью `Set-AppVClientConfiguration` команды PowerShell, которая изменяет локальный реестр ( `PackageInstallationRoot` параметр под `HKLM\Software\Microsoft\AppV\Client\Streaming` ключом).</span><span class="sxs-lookup"><span data-stu-id="83c5c-210">This default storage location is `%ProgramData%\App-V`, but you can configure it during or after setup by using the `Set-AppVClientConfiguration` PowerShell command, which modifies the local registry (`PackageInstallationRoot` value under the `HKLM\Software\Microsoft\AppV\Client\Streaming` key).</span></span> <span data-ttu-id="83c5c-211">Хранилище пакетов должно находиться по локальному пути в клиентской операционной системе.</span><span class="sxs-lookup"><span data-stu-id="83c5c-211">The package store must be located at a local path on the client operating system.</span></span> <span data-ttu-id="83c5c-212">Отдельные пакеты хранятся в хранилище пакетов в подкаталогах, названных для GUID пакета и GUID версии.</span><span class="sxs-lookup"><span data-stu-id="83c5c-212">The individual packages are stored in the package store in subdirectories named for the Package GUID and Version GUID.</span></span>

<span data-ttu-id="83c5c-213">Пример пути к определенному приложению:</span><span class="sxs-lookup"><span data-stu-id="83c5c-213">Example of a path to a specific application:</span></span>

``` syntax
C:\ProgramData\App-V\PackGUID\VersionGUID
```

<span data-ttu-id="83c5c-214">Чтобы изменить расположение хранилища пакетов по умолчанию во время установки, ознакомьтесь со [сведениями о том, как развернуть клиент App-V](how-to-deploy-the-app-v-client-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="83c5c-214">To change the default location of the package store during setup, see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

### <span data-ttu-id="83c5c-215">Общее хранилище содержимого</span><span class="sxs-lookup"><span data-stu-id="83c5c-215">Shared Content Store</span></span>

<span data-ttu-id="83c5c-216">Если клиент App-V настроен в режиме хранения общего содержимого, при возникновении ошибки в потоке данные не записываются на диск, что означает, что для пакетов требуется минимальный объем локального диска (данные публикации).</span><span class="sxs-lookup"><span data-stu-id="83c5c-216">If the App-V Client is configured in Shared Content Store mode, no data is written to disk when a stream fault occurs, which means that the packages require minimal local disk space (publishing data).</span></span> <span data-ttu-id="83c5c-217">В средах VDI очень желательно использовать меньше дискового пространства, где локальное хранилище может быть ограничено, и потоковая передача приложений из высокопроизводительного сетевого расположения (например, SAN) предпочтительнее.</span><span class="sxs-lookup"><span data-stu-id="83c5c-217">The use of less disk space is highly desirable in VDI environments, where local storage can be limited, and streaming the applications from a high performance network location (such as a SAN) is preferable.</span></span> <span data-ttu-id="83c5c-218">Дополнительные сведения о режиме общего хранилища содержимого можно найти в разделе <https://go.microsoft.com/fwlink/p/?LinkId=392750> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-218">For more information on shared content store mode, see <https://go.microsoft.com/fwlink/p/?LinkId=392750>.</span></span>

<span data-ttu-id="83c5c-219">**Примечание**  Компьютер и хранилище пакетов должны располагаться на локальном диске, даже если вы используете конфигурации общего хранилища контента для клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-219">**Note** The machine and package store must be located on a local drive, even when you’re using Shared Content Store configurations for the App-V Client.</span></span>

 

### <span data-ttu-id="83c5c-220">Каталоги пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-220">Package catalogs</span></span>

<span data-ttu-id="83c5c-221">Клиент App-V управляет следующими двумя разположениями на основе файлов:</span><span class="sxs-lookup"><span data-stu-id="83c5c-221">The App-V Client manages the following two file-based locations:</span></span>

-   **<span data-ttu-id="83c5c-222">Каталоги (пользователи и компьютеры).</span><span class="sxs-lookup"><span data-stu-id="83c5c-222">Catalogs (user and machine).</span></span>**

-   <span data-ttu-id="83c5c-223">**Расположения в реестре** — зависят от того, как предназначен для публикации пакет.</span><span class="sxs-lookup"><span data-stu-id="83c5c-223">**Registry locations** - depends on how the package is targeted for publishing.</span></span> <span data-ttu-id="83c5c-224">Существует каталог (хранилище данных) для компьютера и каталог для каждого отдельного пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-224">There is a Catalog (data store) for the computer, and a catalog for each individual user.</span></span> <span data-ttu-id="83c5c-225">Каталог Machine хранит общие сведения, применимые для всех пользователей или пользователей, а каталог пользователей хранит сведения, применимые для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-225">The Machine Catalog stores global information applicable to all users or any user, and the User Catalog stores information applicable to a specific user.</span></span> <span data-ttu-id="83c5c-226">Каталог — это коллекция динамических конфигураций и файлов манифеста. для файлов и реестра в каждой версии пакета есть дискретные данные.</span><span class="sxs-lookup"><span data-stu-id="83c5c-226">The Catalog is a collection of Dynamic Configurations and manifest files; there is discrete data for both file and registry per package version.</span></span> 

### <span data-ttu-id="83c5c-227">Каталог компьютера</span><span class="sxs-lookup"><span data-stu-id="83c5c-227">Machine catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-228">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-228">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-229">Хранит документы пакета, доступные пользователям компьютера, при добавлении и публикации пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-229">Stores package documents that are available to users on the machine, when packages are added and published.</span></span> <span data-ttu-id="83c5c-230">Тем не менее, если во время публикации пакет является глобальным, интеграция будет доступна всем пользователям.</span><span class="sxs-lookup"><span data-stu-id="83c5c-230">However, if a package is “global” at publishing time, the integrations are available to all users.</span></span></p>
<p><span data-ttu-id="83c5c-231">Если пакет не является глобальным, они публикуются только для определенных пользователей, но глобальные ресурсы, которые были изменены и видны всем пользователям на клиентском компьютере (например, каталог пакета, находятся в общем расположении диска).</span><span class="sxs-lookup"><span data-stu-id="83c5c-231">If a package is non-global, the integrations are published only for specific users, but there are still global resources that are modified and visible to anyone on the client computer (e.g., the package directory is in a shared disk location).</span></span></p>
<p><span data-ttu-id="83c5c-232">Если пакет доступен для пользователя на компьютере (Global или non Global), манифест сохраняется в каталоге компьютера.</span><span class="sxs-lookup"><span data-stu-id="83c5c-232">If a package is available to a user on the computer (global or non-global), the manifest is stored in the Machine Catalog.</span></span> <span data-ttu-id="83c5c-233">Если пакет опубликован глобально, существует динамический файл конфигурации, хранящийся в каталоге компьютера; Таким образом, определение того, является ли пакет глобальным, зависит от того, есть ли в каталоге компьютера файл политики (файл UserDeploymentConfiguration).</span><span class="sxs-lookup"><span data-stu-id="83c5c-233">When a package is published globally, there is a Dynamic Configuration file, stored in the Machine Catalog; therefore, the determination of whether a package is global is defined according to whether there is a policy file (UserDeploymentConfiguration file) in the Machine Catalog.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-234">Место хранения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="83c5c-234">Default storage location</span></span></p></td>
<td align="left"><p><code>%programdata%\Microsoft\AppV\Client\Catalog&lt;/code&gt;</p>
<p><span data-ttu-id="83c5c-235">Это расположение не совпадает с расположением хранилища пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-235">This location is not the same as the Package Store location.</span></span> <span data-ttu-id="83c5c-236">Хранилище пакетов является золотым или pristine копией файлов пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-236">The Package Store is the golden or pristine copy of the package files.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-237">Файлы в каталоге компьютера</span><span class="sxs-lookup"><span data-stu-id="83c5c-237">Files in the machine catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-238">Manifest.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-238">Manifest.xml</span></span></p></li>
<li><p><span data-ttu-id="83c5c-239">DeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-239">DeploymentConfiguration.xml</span></span></p></li>
<li><p><span data-ttu-id="83c5c-240">UserManifest.xml (глобально опубликованный пакет)</span><span class="sxs-lookup"><span data-stu-id="83c5c-240">UserManifest.xml (Globally Published Package)</span></span></p></li>
<li><p><span data-ttu-id="83c5c-241">UserDeploymentConfiguration.xml (глобально опубликованный пакет)</span><span class="sxs-lookup"><span data-stu-id="83c5c-241">UserDeploymentConfiguration.xml (Globally Published Package)</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-242">Дополнительное расположение каталога компьютера, используемое, если пакет входит в группу подключения</span><span class="sxs-lookup"><span data-stu-id="83c5c-242">Additional machine catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-243">Следующее расположение находится в дополнение к определенному расположению пакета, упомянутому выше.</span><span class="sxs-lookup"><span data-stu-id="83c5c-243">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>%programdata%\Microsoft\AppV\Client\Catalog\PackageGroups\ConGroupGUID\ConGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-244">Дополнительные файлы в каталоге компьютера, если пакет входит в группу подключения</span><span class="sxs-lookup"><span data-stu-id="83c5c-244">Additional files in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-245">PackageGroupDescriptor.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-245">PackageGroupDescriptor.xml</span></span></p></li>
<li><p><span data-ttu-id="83c5c-246">UserPackageGroupDescriptor.xml (глобально опубликованная группа подключений)</span><span class="sxs-lookup"><span data-stu-id="83c5c-246">UserPackageGroupDescriptor.xml (globally published Connection Group)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83c5c-247">Каталог пользователей</span><span class="sxs-lookup"><span data-stu-id="83c5c-247">User catalog</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-248">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-248">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-249">Создан в процессе публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-249">Created during the publishing process.</span></span> <span data-ttu-id="83c5c-250">Содержит сведения, используемые для публикации пакета и используемые при запуске, чтобы убедиться, что пакет предоставлен определенному пользователю.</span><span class="sxs-lookup"><span data-stu-id="83c5c-250">Contains information used for publishing the package, and also used at launch to ensure that a package is provisioned to a specific user.</span></span> <span data-ttu-id="83c5c-251">Создан в перемещаемом расположении и включает сведения о публикации для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-251">Created in a roaming location and includes user-specific publishing information.</span></span></p>
<p><span data-ttu-id="83c5c-252">При публикации пакета для пользователя файл политики хранится в каталоге пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-252">When a package is published for a user, the policy file is stored in the User Catalog.</span></span> <span data-ttu-id="83c5c-253">В то же время копия манифеста также хранится в каталоге пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-253">At the same time, a copy of the manifest is also stored in the User Catalog.</span></span> <span data-ttu-id="83c5c-254">При удалении пакета обслуживания для пользователя связанные файлы пакета удаляются из каталога пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-254">When a package entitlement is removed for a user, the relevant package files are removed from the User Catalog.</span></span> <span data-ttu-id="83c5c-255">Просматривая каталог пользователей, администратор может просмотреть присутствие динамического файла конфигурации, указывающий на то, что пакет является уполномоченным для этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-255">Looking at the user catalog, an administrator can view the presence of a Dynamic Configuration file, which indicates that the package is entitled for that user.</span></span></p>
<p><span data-ttu-id="83c5c-256">Для перемещаемых пользователей каталог пользователей должен находиться в роуминге или в общем расположении, чтобы сохранить поведение устаревшего поведения App-V для пользователей по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83c5c-256">For roaming users, the User Catalog needs to be in a roaming or shared location to preserve the legacy App-V behavior of targeting users by default.</span></span> <span data-ttu-id="83c5c-257">Права на доступ к данным и политика связаны с пользователем, а не с компьютером, поэтому они должны перемещаться с пользователем после подготовки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-257">Entitlement and policy are tied to a user, not a computer, so they should roam with the user once they are provisioned.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-258">Место хранения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="83c5c-258">Default storage location</span></span></p></td>
<td align="left"><p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\Packages\PkgGUID\VerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-259">Файлы в каталоге пользователей</span><span class="sxs-lookup"><span data-stu-id="83c5c-259">Files in the user catalog</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-260">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-260">UserManifest.xml</span></span></p></li>
<li><p><span data-ttu-id="83c5c-261">DynamicConfiguration.xml или UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-261">DynamicConfiguration.xml or UserDeploymentConfiguration.xml</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-262">Дополнительное расположение пользовательского каталога, используемое, если пакет входит в группу подключения</span><span class="sxs-lookup"><span data-stu-id="83c5c-262">Additional user catalog location, used when the package is part of a connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-263">Следующее расположение находится в дополнение к определенному расположению пакета, упомянутому выше.</span><span class="sxs-lookup"><span data-stu-id="83c5c-263">The following location is in addition to the specific package location mentioned above:</span></span></p>
<p><code>appdata\roaming\Microsoft\AppV\Client\Catalog\PackageGroups\PkgGroupGUID\PkgGroupVerGUID</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-264">Дополнительный файл в каталоге компьютера, когда пакет входит в группу подключения</span><span class="sxs-lookup"><span data-stu-id="83c5c-264">Additional file in the machine catalog when the package is part of a connection group</span></span></p></td>
<td align="left"><p><code>UserPackageGroupDescriptor.xml</code></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83c5c-265">Резервные копии ярлыков</span><span class="sxs-lookup"><span data-stu-id="83c5c-265">Shortcut backups</span></span>

<span data-ttu-id="83c5c-266">В процессе публикации клиент App-V копирует все сочетания клавиш и точки интеграции в `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` эту резервную копию, что позволяет восстановить эти точки интеграции с более ранними версиями после отмены публикации пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-266">During the publishing process, the App-V Client backs up any shortcuts and integration points to `%AppData%\Microsoft\AppV\Client\Integration\ShortCutBackups.` This backup enables the restoration of these integration points to the previous versions when the package is unpublished.</span></span>

### <span data-ttu-id="83c5c-267">Копирование при записи файлов</span><span class="sxs-lookup"><span data-stu-id="83c5c-267">Copy on Write files</span></span>

<span data-ttu-id="83c5c-268">Хранилище пакетов содержит pristine копию файлов пакета, которые были упакованы на сервере публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-268">The Package Store contains a pristine copy of the package files that have been streamed from the publishing server.</span></span> <span data-ttu-id="83c5c-269">Во время нормальной работы приложения App-V пользователь или служба могут потребовать изменения файлов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-269">During normal operation of an App-V application, the user or service may require changes to the files.</span></span> <span data-ttu-id="83c5c-270">Эти изменения не вносятся в хранилище пакетов, чтобы сохранить возможность восстановления приложения, что приводит к удалению этих изменений.</span><span class="sxs-lookup"><span data-stu-id="83c5c-270">These changes are not made in the package store in order to preserve your ability to repair the application, which removes these changes.</span></span> <span data-ttu-id="83c5c-271">В этих расположениях, именуемом copy on write (COW), поддерживается как перемещаемые, так и неперемещаемые места.</span><span class="sxs-lookup"><span data-stu-id="83c5c-271">These locations, called Copy on Write (COW), support both roaming and non-roaming locations.</span></span> <span data-ttu-id="83c5c-272">Расположение, в котором хранятся изменения, зависит от того, где приложение запрограммировано для внесения изменений в собственный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="83c5c-272">The location where the modifications are stored depends where the application has been programmed to write changes to in a native experience.</span></span>

### <span data-ttu-id="83c5c-273">COW роуминг</span><span class="sxs-lookup"><span data-stu-id="83c5c-273">COW roaming</span></span>

<span data-ttu-id="83c5c-274">В указанном выше расположении для перемещения COW в файлах и каталогах, ориентированных на типичное расположение% AppData% или на \\Users\\{username}\\AppData\\Roaming, указаны изменения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-274">The COW Roaming location described above stores changes to files and directories that are targeted to the typical %AppData% location or \\Users\\{username}\\AppData\\Roaming location.</span></span> <span data-ttu-id="83c5c-275">Эти каталоги и файлы затем перемещаются в соответствии с параметрами операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-275">These directories and files are then roamed based on the operating system settings.</span></span>

### <span data-ttu-id="83c5c-276">Локальный COW</span><span class="sxs-lookup"><span data-stu-id="83c5c-276">COW local</span></span>

<span data-ttu-id="83c5c-277">Локальное расположение COW похоже на расположение для перемещения, но каталоги и файлы не перемещаются на другие компьютеры, даже если настроена поддержка роуминга.</span><span class="sxs-lookup"><span data-stu-id="83c5c-277">The COW Local location is similar to the roaming location, but the directories and files are not roamed to other computers, even if roaming support has been configured.</span></span> <span data-ttu-id="83c5c-278">Локальное расположение COW, описанное выше, сохраняет изменения, применимые к типичным окнам, а не к расположению% AppData%.</span><span class="sxs-lookup"><span data-stu-id="83c5c-278">The COW Local location described above stores changes applicable to typical windows and not the %AppData% location.</span></span> <span data-ttu-id="83c5c-279">Перечисленные каталоги будут различаться, но для некоторых типичных местоположений Windows (например, Общая папка AppData и распространенные папки AppData) будут отображаться два расположения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-279">The directories listed will vary but there will be two locations for any typical Windows locations (e.g. Common AppData and Common AppDataS).</span></span> <span data-ttu-id="83c5c-280">" **S** " указывает на расположение с ограничениями, когда виртуальная служба запрашивает изменение в качестве другого пользователя с повышенными правами от пользователей, которые вошли в систему.</span><span class="sxs-lookup"><span data-stu-id="83c5c-280">The **S** signifies the restricted location when the virtual service requests the change as a different elevated user from the logged on users.</span></span> <span data-ttu-id="83c5c-281">В расположении, отличном от**S** , сохраняются изменения, внесенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="83c5c-281">The non-**S** location stores user based changes.</span></span>

## <a href="" id="bkmk-pkg-registry"></a><span data-ttu-id="83c5c-282">Реестр пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-282">Package registry</span></span>


<span data-ttu-id="83c5c-283">Перед тем как приложение сможет получить доступ к данным реестра пакета, клиент App-V должен сделать данные реестра пакета доступными для приложений.</span><span class="sxs-lookup"><span data-stu-id="83c5c-283">Before an application can access the package registry data, the App-V Client must make the package registry data available to the applications.</span></span> <span data-ttu-id="83c5c-284">Клиент App-V использует реальный реестр в качестве резервного хранилища для всех данных реестра.</span><span class="sxs-lookup"><span data-stu-id="83c5c-284">The App-V Client uses the real registry as a backing store for all registry data.</span></span>

<span data-ttu-id="83c5c-285">При добавлении нового пакета в клиент App-V копия реестра. DAT — файл, на который вы создали пакет `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-285">When a new package is added to the App-V Client, a copy of the REGISTRY.DAT file from the package is created at `%ProgramData%\Microsoft\AppV\Client\VREG\{Version GUID}.dat`.</span></span> <span data-ttu-id="83c5c-286">Именем файла является GUID версии с помощью. Расширение DAT.</span><span class="sxs-lookup"><span data-stu-id="83c5c-286">The name of the file is the version GUID with the .DAT extension.</span></span> <span data-ttu-id="83c5c-287">Причина, по которой вы сделали это, заключается в том, чтобы убедиться в том, что фактический файл куста в пакете не используется, что может привести к невозможности удаления пакета позже.</span><span class="sxs-lookup"><span data-stu-id="83c5c-287">The reason this copy is made is to ensure that the actual hive file in the package is never in use, which would prevent the removal of the package at a later time.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83c5c-288">Registry. dat из хранилища пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-288">Registry.dat from Package Store</span></span></strong></p></td>
<td align="left"><p><strong> &gt; </strong></p></td>
<td align="left"><p><strong><span data-ttu-id="83c5c-289">%ProgramData%\Microsoft\AppV\Client\Vreg {VersionGuid}. dat</span><span class="sxs-lookup"><span data-stu-id="83c5c-289">%ProgramData%\Microsoft\AppV\Client\Vreg{VersionGuid}.dat</span></span></strong></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83c5c-290">Когда первое приложение из пакета запускается на клиентском компьютере, клиент помещает или копирует содержимое из файла куста, повторно создавая данные реестра пакета в другом расположении `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-290">When the first application from the package is launched on the client, the client stages or copies the contents out of the hive file, re-creating the package registry data in an alternate location `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\Packages\PackageGuid\Versions\VersionGuid\REGISTRY`.</span></span> <span data-ttu-id="83c5c-291">У поэтапных данных в реестре есть два различных типа данных компьютера и данные пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-291">The staged registry data has two distinct types of machine data and user data.</span></span> <span data-ttu-id="83c5c-292">Данные компьютера будут общими для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="83c5c-292">Machine data is shared across all users on the machine.</span></span> <span data-ttu-id="83c5c-293">Пользовательские данные помещаются для каждого пользователя в userspecific расположение `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-293">User data is staged for each user to a userspecific location `HKCU\Software\Microsoft\AppV\Client\Packages\PackageGuid\Registry\User`.</span></span> <span data-ttu-id="83c5c-294">Данные компьютера в конечном итоге удаляются во время удаления пакета, и данные пользователя удаляются при отмене публикации пользователем.</span><span class="sxs-lookup"><span data-stu-id="83c5c-294">The machine data is ultimately removed at package removal time, and the user data is removed on a user unpublish operation.</span></span>

### <span data-ttu-id="83c5c-295">Настройка промежуточного хранения и реестра для групп подключений</span><span class="sxs-lookup"><span data-stu-id="83c5c-295">Package registry staging vs. connection group registry staging</span></span>

<span data-ttu-id="83c5c-296">При наличии групп соединений предыдущий процесс размещения реестра имеет значение истина, но вместо одного файла куста для обработки существует больше одного.</span><span class="sxs-lookup"><span data-stu-id="83c5c-296">When connection groups are present, the previous process of staging the registry holds true, but instead of having one hive file to process, there are more than one.</span></span> <span data-ttu-id="83c5c-297">Файлы обрабатываются в том порядке, в котором они отображаются в XML-файле группы соединения, при этом первый модуль записи выигрывает любые конфликты.</span><span class="sxs-lookup"><span data-stu-id="83c5c-297">The files are processed in the order in which they appear in the connection group XML, with the first writer winning any conflicts.</span></span>

<span data-ttu-id="83c5c-298">Поэтапный реестр сохраняется так же, как и в одном корпусе пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-298">The staged registry persists the same way as in the single package case.</span></span> <span data-ttu-id="83c5c-299">Промежуточные данные пользовательского реестра остаются для группы подключения до тех пор, пока они не будут отключены; данные реестра для промежуточного компьютера удаляются при удалении группы подключения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-299">Staged user registry data remains for the connection group until it is disabled; staged machine registry data is removed on connection group removal.</span></span>

### <span data-ttu-id="83c5c-300">Виртуальный реестр</span><span class="sxs-lookup"><span data-stu-id="83c5c-300">Virtual registry</span></span>

<span data-ttu-id="83c5c-301">Цель виртуального реестра (VREG) — предоставить единое объединенное представление реестра пакета и собственного реестра для приложений.</span><span class="sxs-lookup"><span data-stu-id="83c5c-301">The purpose of the virtual registry (VREG) is to provide a single merged view of the package registry and the native registry to applications.</span></span> <span data-ttu-id="83c5c-302">Она также предоставляет функциональность копирования при записи (COW), что позволяет вносить любые изменения, внесенные в реестр из контекста виртуального процесса, в отдельном расположении COW.</span><span class="sxs-lookup"><span data-stu-id="83c5c-302">It also provides copy-on-write (COW) functionality – that is any changes made to the registry from the context of a virtual process are made to a separate COW location.</span></span> <span data-ttu-id="83c5c-303">Это означает, что VREG должен объединять до трех отдельных расположений в одном представлении, основываясь на заполненных расположениях в реестре COW — &gt; &gt; native Package.</span><span class="sxs-lookup"><span data-stu-id="83c5c-303">This means that the VREG must combine up to three separate registry locations into a single view based on the populated locations in the registry COW -&gt; package -&gt; native.</span></span> <span data-ttu-id="83c5c-304">При выполнении запроса для данных в реестре он будет расположен в нужном порядке, пока не обнаружит данные, которые они запросили.</span><span class="sxs-lookup"><span data-stu-id="83c5c-304">When a request is made for a registry data it will locate in order until it finds the data it was requesting.</span></span> <span data-ttu-id="83c5c-305">Это означает, что при наличии значения, хранящегося в COW расположении, оно не будет переходить к другим расположениям, но если в COW расположении отсутствуют данные, они будут переходить к пакету, а затем найдет собственное расположение, пока не обнаружит соответствующие данные.</span><span class="sxs-lookup"><span data-stu-id="83c5c-305">Meaning if there is a value stored in a COW location it will not proceed to other locations, however, if there is no data in the COW location it will proceed to the Package and then Native location until it finds the appropriate data.</span></span>

### <span data-ttu-id="83c5c-306">Расположения в реестре</span><span class="sxs-lookup"><span data-stu-id="83c5c-306">Registry locations</span></span>

<span data-ttu-id="83c5c-307">Существует два расположения реестра Package и два расположения групп подключений, в которых клиент App-V хранит данные реестра в зависимости от того, публикуется ли пакет по отдельности или как часть группы подключения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-307">There are two package registry locations and two connection group locations where the App-V Client stores registry information, depending on whether the Package is published individually or as part of a connection group.</span></span> <span data-ttu-id="83c5c-308">Существуют три места COW для пакетов и 3 для групп подключения, которые создаются и управляются VREG.</span><span class="sxs-lookup"><span data-stu-id="83c5c-308">There are three COW locations for packages and three for connection groups, which are created and managed by the VREG.</span></span> <span data-ttu-id="83c5c-309">Параметры пакетов и групп подключений не являются общими.</span><span class="sxs-lookup"><span data-stu-id="83c5c-309">Settings for packages and connection groups are not shared:</span></span>

**<span data-ttu-id="83c5c-310">VReg одного пакета:</span><span class="sxs-lookup"><span data-stu-id="83c5c-310">Single Package VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83c5c-311">Расположение</span><span class="sxs-lookup"><span data-stu-id="83c5c-311">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="83c5c-312">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-312">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83c5c-313">COW</span><span class="sxs-lookup"><span data-stu-id="83c5c-313">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-314">Компьютер Registry\Client\Packages\PkgGUID\REGISTRY (только процесс с повышенными привилегиями может написать)</span><span class="sxs-lookup"><span data-stu-id="83c5c-314">Machine Registry\Client\Packages\PkgGUID\REGISTRY (Only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="83c5c-315">User Registry\Client\Packages\PkgGUID\REGISTRY (пользователь, который в HKCU и на нем написаны все, кроме Software\Classes</span><span class="sxs-lookup"><span data-stu-id="83c5c-315">User Registry\Client\Packages\PkgGUID\REGISTRY (User Roaming anything written under HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="83c5c-316">Classes\Client\Packages\PkgGUID\REGISTRY реестра пользователя (HKCU\Software\Classes записи и HKLM для процесса без повышенных привилегий)</span><span class="sxs-lookup"><span data-stu-id="83c5c-316">User Registry Classes\Client\Packages\PkgGUID\REGISTRY (HKCU\Software\Classes writes and HKLM for non elevated process)</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83c5c-317">Пакет</span><span class="sxs-lookup"><span data-stu-id="83c5c-317">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span><span class="sxs-lookup"><span data-stu-id="83c5c-318">Machine Registry\Client\Packages\PkgGUID\Versions\VerGuid\Registry\Machine</span></span></p></li>
<li><p><span data-ttu-id="83c5c-319">Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry реестра пользователя</span><span class="sxs-lookup"><span data-stu-id="83c5c-319">User Registry Classes\Client\Packages\PkgGUID\Versions\VerGUID\Registry</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83c5c-320">Разряд</span><span class="sxs-lookup"><span data-stu-id="83c5c-320">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-321">Расположение реестра собственного приложения</span><span class="sxs-lookup"><span data-stu-id="83c5c-321">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

**<span data-ttu-id="83c5c-322">VReg группы подключения:</span><span class="sxs-lookup"><span data-stu-id="83c5c-322">Connection Group VReg:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83c5c-323">Расположение</span><span class="sxs-lookup"><span data-stu-id="83c5c-323">Location</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="83c5c-324">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-324">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83c5c-325">COW</span><span class="sxs-lookup"><span data-stu-id="83c5c-325">COW</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-326">Компьютер Registry\Client\PackageGroups\GrpGUID\REGISTRY (только процесс с повышенными привилегиями может написать)</span><span class="sxs-lookup"><span data-stu-id="83c5c-326">Machine Registry\Client\PackageGroups\GrpGUID\REGISTRY (only elevate process can write)</span></span></p></li>
<li><p><span data-ttu-id="83c5c-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (все, что написано в HKCU, за исключением Software\Classes</span><span class="sxs-lookup"><span data-stu-id="83c5c-327">User Registry\Client\PackageGroups\GrpGUID\REGISTRY (Anything written to HKCU except Software\Classes</span></span></p></li>
<li><p><span data-ttu-id="83c5c-328">Classes\Client\PackageGroups\GrpGUID\REGISTRY реестра пользователя</span><span class="sxs-lookup"><span data-stu-id="83c5c-328">User Registry Classes\Client\PackageGroups\GrpGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="83c5c-329">Пакет</span><span class="sxs-lookup"><span data-stu-id="83c5c-329">Package</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span><span class="sxs-lookup"><span data-stu-id="83c5c-330">Machine Registry\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
<li><p><span data-ttu-id="83c5c-331">Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY реестра пользователя</span><span class="sxs-lookup"><span data-stu-id="83c5c-331">User Registry Classes\Client\PackageGroups\GrpGUID\Versions\VerGUID\REGISTRY</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="83c5c-332">Разряд</span><span class="sxs-lookup"><span data-stu-id="83c5c-332">Native</span></span></strong></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="83c5c-333">Расположение реестра собственного приложения</span><span class="sxs-lookup"><span data-stu-id="83c5c-333">Native application registry location</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="83c5c-334">Для HKLM существует два места COW; процессы с повышенными привилегиями и без повышенных привилегий.</span><span class="sxs-lookup"><span data-stu-id="83c5c-334">There are two COW locations for HKLM; elevated and non-elevated processes.</span></span> <span data-ttu-id="83c5c-335">Процессы с повышенными правами всегда записывают изменения в HKLM в безопасном COW в разделе HKLM.</span><span class="sxs-lookup"><span data-stu-id="83c5c-335">Elevated processes always write HKLM changes to the secure COW under HKLM.</span></span> <span data-ttu-id="83c5c-336">Процессы без повышенных привилегий всегда записывают изменения в HKLM в незащищенный COW в разделе HKCU\\Software\\Classes.</span><span class="sxs-lookup"><span data-stu-id="83c5c-336">Non-elevated processes always write HKLM changes to the non-secure COW under HKCU\\Software\\Classes.</span></span> <span data-ttu-id="83c5c-337">Когда приложение считывает изменения из раздела реестра HKLM, в процессах с повышенными привилегиями будут прочитаны изменения из безопасного COW в разделе HKLM.</span><span class="sxs-lookup"><span data-stu-id="83c5c-337">When an application reads changes from HKLM, elevated processes will read changes from the secure COW under HKLM.</span></span> <span data-ttu-id="83c5c-338">Непривилегированные операции чтения из обоих двух и повышают вероятность изменений, внесенных в небезопасных COW.</span><span class="sxs-lookup"><span data-stu-id="83c5c-338">Non-elevated reads from both, favoring the changes made in the unsecure COW first.</span></span>

### <span data-ttu-id="83c5c-339">Сквозные ключи</span><span class="sxs-lookup"><span data-stu-id="83c5c-339">Pass-through keys</span></span>

<span data-ttu-id="83c5c-340">С помощью сквозных ключей администратор может настроить определенные ключи таким образом, чтобы они могли быть прочитаны только из собственного реестра, минуя пакеты и расположения COW.</span><span class="sxs-lookup"><span data-stu-id="83c5c-340">Pass-through keys enable an administrator to configure certain keys so they can only be read from the native registry, bypassing the Package and COW locations.</span></span> <span data-ttu-id="83c5c-341">Транзитные расположения являются глобальными для компьютера (но не для определенного пакета), и его можно настроить, добавив путь к разделу, который должен обрабатываться как проход к параметру **reg \ _MULTI \ _SZ** , именуемому **PassThroughPaths** для ключа `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-341">Pass-through locations are global to the machine (not package specific) and can be configured by adding the path to the key, which should be treated as pass-through to the **REG\_MULTI\_SZ** value called **PassThroughPaths** of the key `HKLM\Software\Microsoft\AppV\Subsystem\VirtualRegistry`.</span></span> <span data-ttu-id="83c5c-342">Любые клавиши, которые отображаются в этом многострочном значении (и их дочерних элементах), обрабатываются как сквозные.</span><span class="sxs-lookup"><span data-stu-id="83c5c-342">Any key that appears under this multi-string value (and their children) will be treated as pass-through.</span></span>

<span data-ttu-id="83c5c-343">Следующие расположения по умолчанию настроены как транзитные.</span><span class="sxs-lookup"><span data-stu-id="83c5c-343">The following locations are configured as pass-through locations by default:</span></span>

-   <span data-ttu-id="83c5c-344">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="83c5c-344">HKEY\_CURRENT\_USER\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="83c5c-345">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span><span class="sxs-lookup"><span data-stu-id="83c5c-345">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\Local Settings\\Software\\Microsoft\\Windows\\CurrentVersion\\AppModel</span></span>

-   <span data-ttu-id="83c5c-346">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span><span class="sxs-lookup"><span data-stu-id="83c5c-346">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\WINEVT</span></span>

-   <span data-ttu-id="83c5c-347">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span><span class="sxs-lookup"><span data-stu-id="83c5c-347">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\services\\eventlog\\Application</span></span>

-   <span data-ttu-id="83c5c-348">HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span><span class="sxs-lookup"><span data-stu-id="83c5c-348">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\WMI\\Autologger</span></span>

-   <span data-ttu-id="83c5c-349">HKEY \ _CURRENT \ _USER параметров \\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet</span><span class="sxs-lookup"><span data-stu-id="83c5c-349">HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Internet Settings</span></span>

-   <span data-ttu-id="83c5c-350">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span><span class="sxs-lookup"><span data-stu-id="83c5c-350">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Perflib</span></span>

-   <span data-ttu-id="83c5c-351">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="83c5c-351">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Policies</span></span>

-   <span data-ttu-id="83c5c-352">HKEY \ _CURRENT \ _USER \\SOFTWARE\\Policies</span><span class="sxs-lookup"><span data-stu-id="83c5c-352">HKEY\_CURRENT\_USER\\SOFTWARE\\Policies</span></span>

<span data-ttu-id="83c5c-353">Цель сквозных ключей заключается в том, чтобы виртуальное приложение не записывало данные реестра в VReg, которое требуется для невиртуальных приложений для успешной работы или интеграции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-353">The purpose of Pass-through keys is to ensure that a virtual application does not write registry data in the VReg that is required for non-virtual applications for successful operation or integration.</span></span> <span data-ttu-id="83c5c-354">Ключ "политики" гарантирует, что параметры групповой политики, заданные администратором, используются и не предназначены для настройки пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-354">The Policies key ensures that Group Policy based settings set by the administrator are utilized and not per package settings.</span></span> <span data-ttu-id="83c5c-355">Для интеграции с приложениями Windows на базе пользовательского интерфейса требуется ключ AppModel.</span><span class="sxs-lookup"><span data-stu-id="83c5c-355">The AppModel key is required for integration with Windows Modern UI based applications.</span></span> <span data-ttu-id="83c5c-356">Рекомендуется, чтобы администрирование не изменялись по умолчанию ни один из входных ключей, но в некоторых случаях в зависимости от поведения приложения может потребоваться добавить дополнительные сквозные ключи.</span><span class="sxs-lookup"><span data-stu-id="83c5c-356">It is recommend that administers do not modify any of the default pass-through keys, but in some instances, based on application behavior may require adding additional pass-through keys.</span></span>

## <a href="" id="bkmk-pkg-store-behavior"></a><span data-ttu-id="83c5c-357">Поведение хранилища пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-357">App-V package store behavior</span></span>


<span data-ttu-id="83c5c-358">Приложение App-V 5 управляет хранилищем пакетов, то есть расположением, в котором хранятся развернутые файлы ресурсов из AppV-файла.</span><span class="sxs-lookup"><span data-stu-id="83c5c-358">App-V 5 manages the Package Store, which is the location where the expanded asset files from the appv file are stored.</span></span> <span data-ttu-id="83c5c-359">По умолчанию это расположение хранится на%ProgramData%\\App-V и ограничено возможностями хранения только за счет свободного места на диске.</span><span class="sxs-lookup"><span data-stu-id="83c5c-359">By default, this location is stored at %ProgramData%\\App-V, and is limited in terms of storage capabilities only by free disk space.</span></span> <span data-ttu-id="83c5c-360">Хранилище пакетов упорядочивается по идентификаторам GUID для пакета и версии, как упоминалось в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="83c5c-360">The package store is organized by the GUIDs for the package and version as mentioned in the previous section.</span></span>

### <span data-ttu-id="83c5c-361">Добавление пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-361">Add packages</span></span>

<span data-ttu-id="83c5c-362">Пакеты App-V помещаются на этапе добавления к компьютеру с помощью клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-362">App-V Packages are staged upon addition to the computer with the App-V Client.</span></span> <span data-ttu-id="83c5c-363">Клиент App-V обеспечивает промежуточное хранение по запросу.</span><span class="sxs-lookup"><span data-stu-id="83c5c-363">The App-V Client provides on-demand staging.</span></span> <span data-ttu-id="83c5c-364">При публикации или добавлении вручную в AppVClientPackage структура данных строится в магазине пакетов (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span><span class="sxs-lookup"><span data-stu-id="83c5c-364">During publishing or a manual Add-AppVClientPackage, the data structure is built in the package store (c:\\programdata\\App-V\\{PkgGUID}\\{VerGUID}).</span></span> <span data-ttu-id="83c5c-365">Файлы пакетов, определенные в блоке публикации, определенном в StreamMap.xml, добавляются в систему и папки верхнего уровня и дочерние файлы для обеспечения существования соответствующих ресурсов приложения при запуске.</span><span class="sxs-lookup"><span data-stu-id="83c5c-365">The package files identified in the publishing block defined in the StreamMap.xml are added to the system and the top level folders and child files staged to ensure proper application assets exist at launch.</span></span>

### <span data-ttu-id="83c5c-366">Монтирование пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-366">Mounting packages</span></span>

<span data-ttu-id="83c5c-367">Пакеты можно загрузить явным образом с помощью PowerShell `Mount-AppVClientPackage` или с помощью **клиентского интерфейса App-V** для загрузки пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-367">Packages can be explicitly loaded using the PowerShell `Mount-AppVClientPackage` or by using the **App-V Client UI** to download a package.</span></span> <span data-ttu-id="83c5c-368">Эта операция полностью загружает весь пакет в хранилище пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-368">This operation completely loads the entire package into the package store.</span></span>

### <span data-ttu-id="83c5c-369">Потоковые пакеты</span><span class="sxs-lookup"><span data-stu-id="83c5c-369">Streaming packages</span></span>

<span data-ttu-id="83c5c-370">Клиент App-V может быть настроен для изменения поведения потоковой передачи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83c5c-370">The App-V Client can be configured to change the default behavior of streaming.</span></span> <span data-ttu-id="83c5c-371">Все политики потоковой передачи хранятся в следующем разделе реестра: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-371">All streaming policies are stored under the following registry key: `HKEY_LOCAL_MAcHINE\Software\Microsoft\AppV\Client\Streaming`.</span></span> <span data-ttu-id="83c5c-372">Политики задаются с помощью командлета PowerShell `Set-AppvClientConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-372">Policies are set using the PowerShell cmdlet `Set-AppvClientConfiguration`.</span></span> <span data-ttu-id="83c5c-373">Для потоковой передачи данных применяются следующие политики:</span><span class="sxs-lookup"><span data-stu-id="83c5c-373">The following policies apply to Streaming:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-374">Политика</span><span class="sxs-lookup"><span data-stu-id="83c5c-374">Policy</span></span></th>
<th align="left"><span data-ttu-id="83c5c-375">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-375">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-376">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="83c5c-376">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-377">В Windows 8 это позволяет выполнять потоковую передачу в сетях 3G и сотовой сети</span><span class="sxs-lookup"><span data-stu-id="83c5c-377">On Windows 8 it allows streaming over 3G and cellular networks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-378">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="83c5c-378">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-379">Задает параметр загрузки в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="83c5c-379">Specifies the Background Load setting:</span></span></p>
<p><strong><span data-ttu-id="83c5c-380">0 </strong> - отключено</span><span class="sxs-lookup"><span data-stu-id="83c5c-380">0</strong> - Disabled</span></span></p>
<p><strong><span data-ttu-id="83c5c-381">1 </strong> — только ранее использованные пакеты</span><span class="sxs-lookup"><span data-stu-id="83c5c-381">1</strong> – Previously Used Packages only</span></span></p>
<p><strong><span data-ttu-id="83c5c-382">2 </strong> — все пакеты</span><span class="sxs-lookup"><span data-stu-id="83c5c-382">2</strong> – All Packages</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-383">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="83c5c-383">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-384">Корневая папка для хранилища пакетов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="83c5c-384">The root folder for the package store in the local machine</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-385">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="83c5c-385">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-386">Переопределение корневого элемента, из которого должны передаваться пакеты.</span><span class="sxs-lookup"><span data-stu-id="83c5c-386">The root override where packages should be streamed from</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-387">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="83c5c-387">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-388">Включает использование общего хранилища содержимого для сценариев VDI.</span><span class="sxs-lookup"><span data-stu-id="83c5c-388">Enables the use of Shared Content Store for VDI scenarios</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="83c5c-389">Эти параметры влияют на поведение потоковых ресурсов пакета App-V в клиенте.</span><span class="sxs-lookup"><span data-stu-id="83c5c-389">These settings affect the behavior of streaming App-V package assets to the client.</span></span> <span data-ttu-id="83c5c-390">По умолчанию для App-V загружаются только ресурсы, необходимые после загрузки первоначальных функциональных блоков публикации и основного.</span><span class="sxs-lookup"><span data-stu-id="83c5c-390">By default, App-V only downloads the assets required after downloading the initial publishing and primary feature blocks.</span></span> <span data-ttu-id="83c5c-391">Потоковые пакеты, которые необходимо объяснить, имеют три конкретных поведения:</span><span class="sxs-lookup"><span data-stu-id="83c5c-391">There are three specific behaviors around streaming packages that must be explained:</span></span>

-   <span data-ttu-id="83c5c-392">Фоновая потоковая передача</span><span class="sxs-lookup"><span data-stu-id="83c5c-392">Background Streaming</span></span>

-   <span data-ttu-id="83c5c-393">Оптимизированная потоковая передача</span><span class="sxs-lookup"><span data-stu-id="83c5c-393">Optimized Streaming</span></span>

-   <span data-ttu-id="83c5c-394">Ошибки потока</span><span class="sxs-lookup"><span data-stu-id="83c5c-394">Stream Faults</span></span>

### <span data-ttu-id="83c5c-395">Фоновая потоковая передача</span><span class="sxs-lookup"><span data-stu-id="83c5c-395">Background streaming</span></span>

<span data-ttu-id="83c5c-396">Командлет PowerShell `Get-AppvClientConfiguration` можно использовать для определения текущего режима фоновой передачи данных с помощью параметра AutoLoad и его изменения с помощью командлета Set-AppvClientConfiguration или в реестре (ключ HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming).</span><span class="sxs-lookup"><span data-stu-id="83c5c-396">The PowerShell cmdlet `Get-AppvClientConfiguration` can be used to determine the current mode for background streaming with the AutoLoad setting and modified with the cmdlet Set-AppvClientConfiguration or from the registry (HKLM\\SOFTWARE\\Microsoft\\AppV\\ClientStreaming key).</span></span> <span data-ttu-id="83c5c-397">Фоновая потоковая передача — это параметр по умолчанию, в котором для параметра autoload задано значение Загрузка ранее использованных пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-397">Background streaming is a default setting where the Autoload setting is set to download previously used packages.</span></span> <span data-ttu-id="83c5c-398">Поведение, основанное на параметре по умолчанию (Value = 1), загружает блоки данных App-V в фоновом режиме после запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-398">The behavior based on default setting (value=1) downloads App-V data blocks in the background after the application has been launched.</span></span> <span data-ttu-id="83c5c-399">Этот параметр может быть отключен вместе (value = 0) или включен для всех пакетов (Value = 2), независимо от того, были ли они запущены.</span><span class="sxs-lookup"><span data-stu-id="83c5c-399">This setting can be disabled all together (value=0) or enabled for all packages (value=2), whether they have been launched.</span></span>

### <span data-ttu-id="83c5c-400">Оптимизированная потоковая передача</span><span class="sxs-lookup"><span data-stu-id="83c5c-400">Optimized streaming</span></span>

<span data-ttu-id="83c5c-401">Пакеты App-V можно настроить с помощью основного блока функций во время последовательности.</span><span class="sxs-lookup"><span data-stu-id="83c5c-401">App-V packages can be configured with a primary feature block during sequencing.</span></span> <span data-ttu-id="83c5c-402">Этот параметр позволяет инженеру по виртуализации отслеживать файлы запуска для определенного приложения или приложения, а также помечать блоки данных в пакете App-V для потоковой передачи при первом запуске любого приложения в пакете.</span><span class="sxs-lookup"><span data-stu-id="83c5c-402">This setting allows the sequencing engineer to monitor launch files for a specific application, or applications, and mark the blocks of data in the App-V package for streaming at first launch of any application in the package.</span></span>

### <span data-ttu-id="83c5c-403">Ошибки потока</span><span class="sxs-lookup"><span data-stu-id="83c5c-403">Stream faults</span></span>

<span data-ttu-id="83c5c-404">После первоначального потока любых публикуемых данных и основного блока функций запросы на дополнительные файлы выполняют ошибки потока.</span><span class="sxs-lookup"><span data-stu-id="83c5c-404">After the initial stream of any publishing data and the primary feature block, requests for additional files perform stream faults.</span></span> <span data-ttu-id="83c5c-405">Эти блоки данных загружаются в хранилище пакетов по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="83c5c-405">These blocks of data are downloaded to the package store on an as-needed basis.</span></span> <span data-ttu-id="83c5c-406">Это позволяет пользователю загружать только небольшие части пакета, как правило, для запуска пакета и выполнения обычных задач.</span><span class="sxs-lookup"><span data-stu-id="83c5c-406">This allows a user to download only a small part of the package, typically enough to launch the package and run normal tasks.</span></span> <span data-ttu-id="83c5c-407">Все остальные блоки загружаются, когда пользователь инициирует операцию, для которой требуются данные, не находящиеся в хранилище пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-407">All other blocks are downloaded when a user initiates an operation that requires data not currently in the package store.</span></span>

<span data-ttu-id="83c5c-408">Дополнительные сведения о потоковой передаче пакетов App-V: <https://go.microsoft.com/fwlink/?LinkId=392770> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-408">For more information on App-V Package streaming visit: <https://go.microsoft.com/fwlink/?LinkId=392770>.</span></span>

<span data-ttu-id="83c5c-409">Последовательность оптимизации потоков можно найти по адресу: <https://go.microsoft.com/fwlink/?LinkId=392771> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-409">Sequencing for streaming optimization is available at: <https://go.microsoft.com/fwlink/?LinkId=392771>.</span></span>

### <span data-ttu-id="83c5c-410">Обновления пакетов</span><span class="sxs-lookup"><span data-stu-id="83c5c-410">Package upgrades</span></span>

<span data-ttu-id="83c5c-411">Пакеты App-V требуют обновления в течение всего жизненного цикла приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-411">App-V Packages require updating throughout the lifecycle of the application.</span></span> <span data-ttu-id="83c5c-412">Обновления пакетов App-V похожи на операцию публикации пакета, так как каждая версия будет создана в отдельном расположении PackageRoot: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}` .</span><span class="sxs-lookup"><span data-stu-id="83c5c-412">App-V Package upgrades are similar to the package publish operation, as each version will be created in its own PackageRoot location: `%ProgramData%\App-V\{PkgGUID}\{newVerGUID}`.</span></span> <span data-ttu-id="83c5c-413">Действие по обновлению оптимизируется путем создания жесткой ссылки на идентичные и потоковые файлы из других версий одного и того же пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-413">The upgrade operation is optimized by creating hard links to identical- and streamed-files from other versions of the same package.</span></span>

### <span data-ttu-id="83c5c-414">Удаление пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-414">Package removal</span></span>

<span data-ttu-id="83c5c-415">Поведение клиента App-V при удалении пакетов зависит от метода, используемого для удаления.</span><span class="sxs-lookup"><span data-stu-id="83c5c-415">The behavior of the App-V Client when packages are removed depends on the method used for removal.</span></span> <span data-ttu-id="83c5c-416">С помощью полной инфраструктуры App-V для отмены публикации приложения удаляются файлы каталога пользователей (каталог компьютера для глобальных опубликованных приложений), но сохраняются расположение хранилища пакетов и COWые места.</span><span class="sxs-lookup"><span data-stu-id="83c5c-416">Using an App-V full infrastructure to unpublish the application, the user catalog files (machine catalog for globally published applications) are removed, but retains the package store location and COW locations.</span></span> <span data-ttu-id="83c5c-417">При использовании командлета PowerShell `Remove-AppVClientPackge` для удаления пакета App-V место в хранилище пакетов очищается.</span><span class="sxs-lookup"><span data-stu-id="83c5c-417">When the PowerShell cmdlet `Remove-AppVClientPackge` is used to remove an App-V Package, the package store location is cleaned.</span></span> <span data-ttu-id="83c5c-418">Следует помнить, что отмена публикации пакета App-V с сервера управления не приводит к выполнению операции удаления.</span><span class="sxs-lookup"><span data-stu-id="83c5c-418">Remember that unpublishing an App-V Package from the Management Server does not perform a Remove operation.</span></span> <span data-ttu-id="83c5c-419">Ни одна из операций не приведет к удалению файлов пакета магазина пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-419">Neither operation will remove the Package Store package files.</span></span>

## <a href="" id="bkmk-roaming-reg-data"></a><span data-ttu-id="83c5c-420">Перемещаемый реестр и данные</span><span class="sxs-lookup"><span data-stu-id="83c5c-420">Roaming registry and data</span></span>


<span data-ttu-id="83c5c-421">Приложение App-V 5 может обеспечивать практически собственный интерфейс при роуминге, в зависимости от того, как написано приложение.</span><span class="sxs-lookup"><span data-stu-id="83c5c-421">App-V 5 is able to provide a near-native experience when roaming, depending on how the application being used is written.</span></span> <span data-ttu-id="83c5c-422">По умолчанию App-V перемещает AppData, хранящийся в перемещаемом расположении, в зависимости от конфигурации роуминга операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-422">By default, App-V roams AppData that is stored in the roaming location, based on the roaming configuration of the operating system.</span></span> <span data-ttu-id="83c5c-423">Другие расположения для хранения данных на основе файлов не перемещаются с компьютера на компьютер, так как они находятся в неперемещаемых местах.</span><span class="sxs-lookup"><span data-stu-id="83c5c-423">Other locations for storage of file-based data do not roam from computer to computer, since they are in locations that are not roamed.</span></span>

### <a href="" id="bkmk-clt-inter-roam-reqs"></a><span data-ttu-id="83c5c-424">Требования к роумингу и хранилище данных в каталоге пользователей</span><span class="sxs-lookup"><span data-stu-id="83c5c-424">Roaming requirements and user catalog data storage</span></span>

<span data-ttu-id="83c5c-425">App-V хранит данные, которые представляют состояние каталога пользователя, в форме:</span><span class="sxs-lookup"><span data-stu-id="83c5c-425">App-V stores data, which represents the state of the user’s catalog, in the form of:</span></span>

-   <span data-ttu-id="83c5c-426">Файлы в разделе%appdata%\\Microsoft\\AppV\\Client\\Catalog</span><span class="sxs-lookup"><span data-stu-id="83c5c-426">Files under %appdata%\\Microsoft\\AppV\\Client\\Catalog</span></span>

-   <span data-ttu-id="83c5c-427">Параметры реестра в разделе</span><span class="sxs-lookup"><span data-stu-id="83c5c-427">Registry settings under</span></span> `HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages`

<span data-ttu-id="83c5c-428">Вместе эти файлы и параметры реестра представляют каталог пользователя, поэтому оба должны быть перемещены либо ни один из них не должен перемещаться для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-428">Together, these files and registry settings represent the user’s catalog, so either both must be roamed, or neither must be roamed for a given user.</span></span> <span data-ttu-id="83c5c-429">Приложение App-V не поддерживает перемещаемые% AppData%, но не перенаносит в себя пользовательский профиль (реестр) или наоборот.</span><span class="sxs-lookup"><span data-stu-id="83c5c-429">App-V does not support roaming %AppData%, but not roaming the user’s profile (registry), or vice versa.</span></span>

<span data-ttu-id="83c5c-430">**Примечание**  Командлет **Repair-AppvClientPackage** не восстанавливает состояние публикации пакетов, где состояние App-V `HKEY_CURRENT_USER` отсутствует или не совпадает с данными в% AppData%.</span><span class="sxs-lookup"><span data-stu-id="83c5c-430">**Note** The **Repair-AppvClientPackage** cmdlet does not repair the publishing state of packages, where the user’s App-V state under `HKEY_CURRENT_USER` is missing or mismatched with the data in %appdata%.</span></span>

 

### <span data-ttu-id="83c5c-431">Данные на основе реестра</span><span class="sxs-lookup"><span data-stu-id="83c5c-431">Registry-based data</span></span>

<span data-ttu-id="83c5c-432">Роуминг в реестре App-V состоит из двух сценариев, как показано в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="83c5c-432">App-V registry roaming falls into two scenarios, as shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-433">Сценарий</span><span class="sxs-lookup"><span data-stu-id="83c5c-433">Scenario</span></span></th>
<th align="left"><span data-ttu-id="83c5c-434">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-434">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-435">Приложения, которые выполняются как обычные пользователи</span><span class="sxs-lookup"><span data-stu-id="83c5c-435">Applications that are run as standard users</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-436">Когда стандартный пользователь запускает приложение App-V, в кусте HKCU на компьютере сохраняются как HKLM, так и HKCU для приложений App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-436">When a standard user launches an App-V application, both HKLM and HKCU for App-V applications are stored in the HKCU hive on the machine.</span></span> <span data-ttu-id="83c5c-437">Это два отдельных пути.</span><span class="sxs-lookup"><span data-stu-id="83c5c-437">This presents as two distinct paths:</span></span></p>
<ul>
<li><p><span data-ttu-id="83c5c-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages {PkgGUID} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="83c5c-438">HKLM: HKCU\SOFTWARE\Classes\AppV\Client\Packages{PkgGUID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="83c5c-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ REGISTRY\USER {о} \ программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="83c5c-439">HKCU: HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\REGISTRY\USER{UserSID}\SOFTWARE</span></span></p></li>
</ul>
<p><span data-ttu-id="83c5c-440">Для расположения разрешено перемещение на основе параметров операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-440">The locations are enabled for roaming based on the operating system settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-441">Приложения, запускаемые с повышением прав</span><span class="sxs-lookup"><span data-stu-id="83c5c-441">Applications that are run with elevation</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-442">При запуске приложения с повышением прав:</span><span class="sxs-lookup"><span data-stu-id="83c5c-442">When an application is launched with elevation:</span></span></p>
<ul>
<li><p><span data-ttu-id="83c5c-443">Данные HKLM хранятся в кусте HKLM на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="83c5c-443">HKLM data is stored in the HKLM hive on the local computer</span></span></p></li>
<li><p><span data-ttu-id="83c5c-444">Данные HKCU хранятся в пользовательском расположении реестра.</span><span class="sxs-lookup"><span data-stu-id="83c5c-444">HKCU data is stored in the User Registry location</span></span></p></li>
</ul>
<p><span data-ttu-id="83c5c-445">В этом случае эти параметры не будут перемещаться с помощью обычных перемещаемых конфигураций операционной системы, а полученные разделы и значения реестра будут храниться в следующем расположении:</span><span class="sxs-lookup"><span data-stu-id="83c5c-445">In this scenario, these settings are not roamed with normal operating system roaming configurations, and the resulting registry keys and values are stored in the following location:</span></span></p>
<ul>
<li><p><span data-ttu-id="83c5c-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} {.\n\n-} \ REGISTRY\MACHINE\SOFTWARE</span><span class="sxs-lookup"><span data-stu-id="83c5c-446">HKLM\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}{UserSID}\REGISTRY\MACHINE\SOFTWARE</span></span></p></li>
<li><p><span data-ttu-id="83c5c-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages {PkgGUID} \ Registry\User {.\n\n-} \ программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="83c5c-447">HKCU\SOFTWARE\Microsoft\AppV\Client\Packages{PkgGUID}\Registry\User{UserSID}\SOFTWARE</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83c5c-448">Перенаправление для App-V и папок</span><span class="sxs-lookup"><span data-stu-id="83c5c-448">App-V and folder redirection</span></span>

<span data-ttu-id="83c5c-449">Приложение App-V 5.0 SP2 поддерживает перенаправление папок перемещаемой папки AppData (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="83c5c-449">App-V 5.0SP2 supports folder redirection of the roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="83c5c-450">При запуске виртуальной среды состояние роуминга AppData из папки перемещаемой AppData копируется в локальный кэш.</span><span class="sxs-lookup"><span data-stu-id="83c5c-450">When the virtual environment is started, the roaming AppData state from the user’s roaming AppData directory is copied to the local cache.</span></span> <span data-ttu-id="83c5c-451">И наоборот, при завершении работы виртуальной среды локальный кэш, связанный с перемещаемой AppData, будет передаваться в фактическое расположение папки с перемещаемой AppData пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-451">Conversely, when the virtual environment is shut down, the local cache that is associated with a specific user’s roaming AppData is transferred to the actual location of that user’s roaming AppData directory.</span></span>

<span data-ttu-id="83c5c-452">У типичного пакета есть несколько местоположений, сопоставленных в резервном хранилище пользователя для параметров в AppData\\Local и AppData\\Roaming.</span><span class="sxs-lookup"><span data-stu-id="83c5c-452">A typical package has several locations mapped in the user’s backing store for settings in both AppData\\Local and AppData\\Roaming.</span></span> <span data-ttu-id="83c5c-453">Эти расположения предназначены для копирования на место, которое хранится на каждом пользователе в профиле пользователя и используются для хранения изменений, внесенных в каталоги VFS и для защиты пакета по умолчанию VFS.</span><span class="sxs-lookup"><span data-stu-id="83c5c-453">These locations are the Copy on Write locations that are stored per user in the user’s profile, and that are used to store changes made to the package VFS directories and to protect the default package VFS.</span></span>

<span data-ttu-id="83c5c-454">В следующей таблице показаны локальные и перемещаемые расположения, если перенаправление папок не реализовано.</span><span class="sxs-lookup"><span data-stu-id="83c5c-454">The following table shows local and roaming locations, when folder redirection has not been implemented.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-455">VFS Directory в пакете</span><span class="sxs-lookup"><span data-stu-id="83c5c-455">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="83c5c-456">Сопоставленное расположение резервного хранилища</span><span class="sxs-lookup"><span data-stu-id="83c5c-456">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-457">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-457">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-458">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-458">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-459">SystemX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-459">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-460">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-460">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-461">Windows</span><span class="sxs-lookup"><span data-stu-id="83c5c-461">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-462">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="83c5c-462">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-463">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="83c5c-463">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-464">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="83c5c-464">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-465">AppData</span><span class="sxs-lookup"><span data-stu-id="83c5c-465">AppData</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-466">C:\users\jsmith\AppData &lt; сильное &gt; роуминг </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="83c5c-466">C:\users\jsmith\AppData&lt;strong&gt;Roaming</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="83c5c-467">В следующей таблице показаны локальные и перемещаемые расположения, если перенаправление папки реализовано для% AppData%, а расположение было перенаправлено (обычно — в сетевое расположение).</span><span class="sxs-lookup"><span data-stu-id="83c5c-467">The following table shows local and roaming locations, when folder redirection has been implemented for %AppData%, and the location has been redirected (typically to a network location).</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-468">VFS Directory в пакете</span><span class="sxs-lookup"><span data-stu-id="83c5c-468">VFS directory in package</span></span></th>
<th align="left"><span data-ttu-id="83c5c-469">Сопоставленное расположение резервного хранилища</span><span class="sxs-lookup"><span data-stu-id="83c5c-469">Mapped location of backing store</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-470">ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-470">ProgramFilesX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-471">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-471">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\ProgramFilesX86</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-472">SystemX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-472">SystemX86</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-473">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \SystemX86</span><span class="sxs-lookup"><span data-stu-id="83c5c-473">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\SystemX86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-474">Windows</span><span class="sxs-lookup"><span data-stu-id="83c5c-474">Windows</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-475">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \Windows</span><span class="sxs-lookup"><span data-stu-id="83c5c-475">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\Windows</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-476">appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="83c5c-476">appv_ROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-477">C:\users\jsmith\AppData &lt; strong &gt; Местная </strong> \Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \ appv_ROOT</span><span class="sxs-lookup"><span data-stu-id="83c5c-477">C:\users\jsmith\AppData&lt;strong&gt;Local</strong>\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\appv_ROOT</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-478">AppData</span><span class="sxs-lookup"><span data-stu-id="83c5c-478">AppData</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="83c5c-479">\Fileserver </strong> \users\jsmith\roaming\Microsoft\AppV\Client\VFS &amp; lt; GUID &gt; \AppData</span><span class="sxs-lookup"><span data-stu-id="83c5c-479">\Fileserver</strong>\users\jsmith\roaming\Microsoft\AppV\Client\VFS&amp;lt;GUID&gt;\AppData</span></span></p></td>
</tr>
</tbody>
</table>

 

 

<span data-ttu-id="83c5c-480">Текущий драйвер VFS клиента App-V не может записать в сеть, поэтому клиент App-V обнаруживает наличие перенаправления папок и копирует данные на локальном диске во время публикации и при запуске виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="83c5c-480">The current App-V Client VFS driver cannot write to network locations, so the App-V Client detects the presence of folder redirection and copies the data on the local drive during publishing and when the virtual environment starts.</span></span> <span data-ttu-id="83c5c-481">После того как пользователь закроет приложение App-V, а клиент App-V закроет виртуальную среду, локальное хранилище VFS AppData копируется в сеть, позволяя перемещаться на дополнительные компьютеры, где процесс будет повторен.</span><span class="sxs-lookup"><span data-stu-id="83c5c-481">After the user closes the App-V application and the App-V Client closes the virtual environment, the local storage of the VFS AppData is copied back to the network, enabling roaming to additional machines, where the process will be repeated.</span></span> <span data-ttu-id="83c5c-482">Ниже приведены подробные инструкции по выполнению процессов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-482">The detailed steps of the processes are:</span></span>

1.  <span data-ttu-id="83c5c-483">При запуске публикации или виртуальной среды клиент App-V обнаруживает расположение каталога AppData.</span><span class="sxs-lookup"><span data-stu-id="83c5c-483">During publishing or virtual environment startup, the App-V Client detects the location of the AppData directory.</span></span>

2.  <span data-ttu-id="83c5c-484">Если путь для перемещаемой AppData является локальным или INO AppData\\Roaming расположением, ничего не происходит.</span><span class="sxs-lookup"><span data-stu-id="83c5c-484">If the roaming AppData path is local or ino AppData\\Roaming location is mapped, nothing happens.</span></span>

3.  <span data-ttu-id="83c5c-485">Если путь к перемещаемой папке AppData не является локальным, каталог AppData VFS будет сопоставлен с каталогом локальных AppData.</span><span class="sxs-lookup"><span data-stu-id="83c5c-485">If the roaming AppData path is not local, the VFS AppData directory is mapped to the local AppData directory.</span></span>

<span data-ttu-id="83c5c-486">Этот процесс решает проблему, связанную с нелокальной% AppData%, которая не поддерживается драйвером клиента App-V VFS.</span><span class="sxs-lookup"><span data-stu-id="83c5c-486">This process solves the problem of a non-local %AppData% that is not supported by the App-V Client VFS driver.</span></span> <span data-ttu-id="83c5c-487">Однако данные, хранящиеся в этом новом расположении, не перемещаются с помощью перенаправления папок.</span><span class="sxs-lookup"><span data-stu-id="83c5c-487">However, the data stored in this new location is not roamed with folder redirection.</span></span> <span data-ttu-id="83c5c-488">Все изменения, внесенные во время выполнения приложения, происходят в локальной папке AppData и должны быть скопированы в перенаправленное расположение.</span><span class="sxs-lookup"><span data-stu-id="83c5c-488">All changes during the running of the application happen to the local AppData location and must be copied to the redirected location.</span></span> <span data-ttu-id="83c5c-489">Ниже приведено подробное описание этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="83c5c-489">The detailed steps of this process are:</span></span>

1.  <span data-ttu-id="83c5c-490">Приложение App-V завершает работу, что закрывает виртуальную среду.</span><span class="sxs-lookup"><span data-stu-id="83c5c-490">App-V application is shut down, which shuts down the virtual environment.</span></span>

2.  <span data-ttu-id="83c5c-491">Локальный кэш перемещаемой папки AppData сжимается и сохраняется в ZIP-файле.</span><span class="sxs-lookup"><span data-stu-id="83c5c-491">The local cache of the roaming AppData location is compressed and stored in a ZIP file.</span></span>

3.  <span data-ttu-id="83c5c-492">Для присвоения имени файлу используется метка времени в конце процесса упаковки ZIP.</span><span class="sxs-lookup"><span data-stu-id="83c5c-492">A timestamp at the end of the ZIP packaging process is used to name the file.</span></span>

4.  <span data-ttu-id="83c5c-493">Метка времени записывается в реестр: HKEY \ _CURRENT \ _USER \\Software\\Microsoft\\AppV\\Client\\Packages\\ &lt; GUID &gt; \\AppDataTime как последнюю известную временную метку APPDATA.</span><span class="sxs-lookup"><span data-stu-id="83c5c-493">The timestamp is recorded in the registry: HKEY\_CURRENT\_USER\\Software\\Microsoft\\AppV\\Client\\Packages\\&lt;GUID&gt;\\AppDataTime as the last known AppData timestamp.</span></span>

5.  <span data-ttu-id="83c5c-494">Процесс перенаправления папок вызывается для оценки и инициализации ZIP-файла, отправленного в каталог роуминга AppData.</span><span class="sxs-lookup"><span data-stu-id="83c5c-494">The folder redirection process is called to evaluate and initiate the ZIP file uploaded to the roaming AppData directory.</span></span>

<span data-ttu-id="83c5c-495">Метка времени используется для определения сценария последнего составителя, если возник конфликт и используется для оптимизации загрузки данных при публикации приложения App-V или при запуске виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="83c5c-495">The timestamp is used to determine a “last writer wins” scenario if there is a conflict and is used to optimize the download of the data when the App-V application is published or the virtual environment is started.</span></span> <span data-ttu-id="83c5c-496">Перенаправление папок обеспечивает доступ к данным на всех клиентах, охваченных поддержкой политики поддержки, и инициирует процесс сохранения данных AppData\\Roaming в локальной папке AppData на клиенте.</span><span class="sxs-lookup"><span data-stu-id="83c5c-496">Folder redirection will make the data available from any other clients covered by the supporting policy and will initiate the process of storing the AppData\\Roaming data to the local AppData location on the client.</span></span> <span data-ttu-id="83c5c-497">Ниже описаны подробные процессы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-497">The detailed processes are:</span></span>

1.  <span data-ttu-id="83c5c-498">Пользователь запускает виртуальную среду, запустив приложение.</span><span class="sxs-lookup"><span data-stu-id="83c5c-498">The user starts the virtual environment by starting an application.</span></span>

2.  <span data-ttu-id="83c5c-499">Виртуальная среда приложения проверяет, не был ли последний сжатый ZIP-файл, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="83c5c-499">The application’s virtual environment checks for the most recent time stamped ZIP file, if present.</span></span>

3.  <span data-ttu-id="83c5c-500">Реестр проверяются на наличие последней известной отметкой времени (если она есть).</span><span class="sxs-lookup"><span data-stu-id="83c5c-500">The registry is checked for the last known uploaded timestamp, if present.</span></span>

4.  <span data-ttu-id="83c5c-501">Последний ZIP-файл загружается за исключением тех случаев, когда локальная последняя известная отметка времени отправки больше или равна отметке времени из ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="83c5c-501">The most recent ZIP file is downloaded unless the local last known upload timestamp is greater than or equal to the timestamp from the ZIP file.</span></span>

5.  <span data-ttu-id="83c5c-502">Если локальная последняя известная отметка времени отправки более ранняя, чем последняя ZIP-файл в расположении для перемещаемой оснастки, ZIP-файл извлекается в локальный временный каталог в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-502">If the local last known upload timestamp is earlier than that of the most recent ZIP file in the roaming AppData location, the ZIP file is extracted to the local temp directory in the user’s profile.</span></span>

6.  <span data-ttu-id="83c5c-503">После успешного извлечения ZIP-файла локальный кэш перемещаемой папки AppData переименовывается, и новые данные перемещаются на место.</span><span class="sxs-lookup"><span data-stu-id="83c5c-503">After the ZIP file is successfully extracted, the local cache of the roaming AppData directory is renamed and the new data is moved into place.</span></span>

7.  <span data-ttu-id="83c5c-504">Переименованный каталог удаляется, а приложение открывается с использованием последнего сохраненного данных роуминга AppData.</span><span class="sxs-lookup"><span data-stu-id="83c5c-504">The renamed directory is deleted and the application opens with the most recently saved roaming AppData data.</span></span>

<span data-ttu-id="83c5c-505">Это завершит успешное перемещение параметров приложения, которые присутствуют в AppData\\Roaming местоположений.</span><span class="sxs-lookup"><span data-stu-id="83c5c-505">This completes the successful roaming of application settings that are present in AppData\\Roaming locations.</span></span> <span data-ttu-id="83c5c-506">Единственным другим условием, которое необходимо устранить, является операция восстановления пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-506">The only other condition that must be addressed is a package repair operation.</span></span> <span data-ttu-id="83c5c-507">Сведения о процессе:</span><span class="sxs-lookup"><span data-stu-id="83c5c-507">The details of the process are:</span></span>

1.  <span data-ttu-id="83c5c-508">Во время восстановления определите, не является ли путь к каталогу перемещаемой AppData пользователя локальным.</span><span class="sxs-lookup"><span data-stu-id="83c5c-508">During repair, detect if the path to the user’s roaming AppData directory is not local.</span></span>

2.  <span data-ttu-id="83c5c-509">Сопоставьте нелокальные целевые объекты пути AppData с роумингом повторно.</span><span class="sxs-lookup"><span data-stu-id="83c5c-509">Map the non-local roaming AppData path targets are recreated the expected roaming and local AppData locations.</span></span>

3.  <span data-ttu-id="83c5c-510">Удаление метки времени, хранящейся в реестре, если она есть.</span><span class="sxs-lookup"><span data-stu-id="83c5c-510">Delete the timestamp stored in the registry, if present.</span></span>

<span data-ttu-id="83c5c-511">Этот процесс заново создаст локальные и сетевые расположения для AppData и удалит запись реестра для временной метки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-511">This process will re-create both the local and network locations for AppData and remove the registry record of the timestamp.</span></span>

## <a href="" id="bkmk-clt-app-lifecycle"></a><span data-ttu-id="83c5c-512">Управление жизненным циклом в клиентском приложении App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-512">App-V client application lifecycle management</span></span>


<span data-ttu-id="83c5c-513">В полной инфраструктуре App-V после упорядочения приложений они управляются и публикуются для пользователей и компьютеров с помощью управления App-V и сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="83c5c-513">In an App-V Full Infrastructure, after applications are sequenced they are managed and published to users or computers via the App-V Management and Publishing servers.</span></span> <span data-ttu-id="83c5c-514">В этом разделе описаны операции, возникающие при выполнении общих операций жизненного цикла приложения App-V (Добавление, публикация, запуск, обновление и удаление), а также файлов и расположений реестра, измененных и измененных с точки зрения клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-514">This section details the operations that occur during the common App-V application lifecycle operations (Add, publishing, launch, upgrade, and removal) and the file and registry locations that are changed and modified from the App-V Client perspective.</span></span> <span data-ttu-id="83c5c-515">Клиентские операции App-V выполняются как серии команд PowerShell, инициированных на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-515">The App-V Client operations are performed as a series of PowerShell commands initiated on the computer running the App-V Client.</span></span>

<span data-ttu-id="83c5c-516">В этом документе основное внимание уделяется решениям для всех инфраструктур App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-516">This document focuses on App-V Full Infrastructure solutions.</span></span> <span data-ttu-id="83c5c-517">Подробные сведения о интеграции App-V и Configuration Manager 2012: <https://go.microsoft.com/fwlink/?LinkId=392773> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-517">For specific information on App-V Integration with Configuration Manager 2012 visit: <https://go.microsoft.com/fwlink/?LinkId=392773>.</span></span>

<span data-ttu-id="83c5c-518">Задачи жизненного цикла приложения App-V запускаются при входе пользователя (по умолчанию), запуске компьютера или в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="83c5c-518">The App-V application lifecycle tasks are triggered at user login (default), machine startup, or as background timed operations.</span></span> <span data-ttu-id="83c5c-519">Параметры клиентских операций App-V, в том числе серверы публикации, интервалы обновления, включение и использование сценария пакета, задаются во время настройки клиента или после установки с помощью команд PowerShell.</span><span class="sxs-lookup"><span data-stu-id="83c5c-519">The settings for the App-V Client operations, including Publishing Servers, refresh intervals, package script enablement, and others, are configured during setup of the client or post-setup with PowerShell commands.</span></span> <span data-ttu-id="83c5c-520">Сведения о том, как [развернуть клиент App-V](how-to-deploy-the-app-v-client-gb18030.md) или использовать PowerShell, можно найти в разделе Развертывание клиента в TechNet.</span><span class="sxs-lookup"><span data-stu-id="83c5c-520">See the How to Deploy the Client section on TechNet at: [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md) or utilize the PowerShell:</span></span>

```powershell
get-command *appv*
```

### <span data-ttu-id="83c5c-521">Обновление публикации</span><span class="sxs-lookup"><span data-stu-id="83c5c-521">Publishing refresh</span></span>

<span data-ttu-id="83c5c-522">Процесс обновления публикации состоит из нескольких операций с небольшим объемом, которые выполняются в клиенте App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-522">The publishing refresh process is comprised of several smaller operations that are performed on the App-V Client.</span></span> <span data-ttu-id="83c5c-523">Поскольку App-V — это технология виртуализации приложений, а не технология планирования задач, планировщик заданий Windows используется для включения процесса при входе пользователя в систему, запуске компьютера и в запланированные интервалы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-523">Since App-V is an application virtualization technology and not a task scheduling technology, the Windows Task Scheduler is utilized to enable the process at user logon, machine startup, and at scheduled intervals.</span></span> <span data-ttu-id="83c5c-524">Настройка клиента в указанных выше случаях является предпочтительным способом при распространении клиента на большую группу компьютеров с правильными параметрами.</span><span class="sxs-lookup"><span data-stu-id="83c5c-524">The configuration of the client during setup listed above is the preferred method when distributing the client to a large group of computers with the correct settings.</span></span> <span data-ttu-id="83c5c-525">Эти параметры клиента можно настроить с помощью следующих командлетов PowerShell:</span><span class="sxs-lookup"><span data-stu-id="83c5c-525">These client settings can be configured with the following PowerShell cmdlets:</span></span>

-   <span data-ttu-id="83c5c-526">**Add-AppVPublishingServer:** Настраивает Клиент с помощью сервера публикаций App-V, предоставляющего пакеты App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-526">**Add-AppVPublishingServer:** Configures the client with an App-V Publishing Server that provides App-V packages.</span></span>

-   <span data-ttu-id="83c5c-527">**Set-AppVPublishingServer:** Изменение текущих параметров для сервера публикаций App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-527">**Set-AppVPublishingServer:** Modifies the current settings for the App-V Publishing Server.</span></span>

-   <span data-ttu-id="83c5c-528">**Set-AppVClientConfiguration:** Изменяет параметры текущих параметров для клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-528">**Set-AppVClientConfiguration:** Modifies the currents settings for the App-V Client.</span></span>

-   <span data-ttu-id="83c5c-529">**Sync (синхронизация) — AppVPublishingServer:** Инициирует процесс обновления публикации App-V вручную.</span><span class="sxs-lookup"><span data-stu-id="83c5c-529">**Sync-AppVPublishingServer:** Initiates an App-V Publishing Refresh process manually.</span></span> <span data-ttu-id="83c5c-530">Это также используется в запланированных задачах, созданных при настройке сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="83c5c-530">This is also utilized in the scheduled tasks created during configuration of the publishing server.</span></span>

<span data-ttu-id="83c5c-531">В следующих разделах описаны действия, которые выполняются на разных этапах обновления публикации для App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-531">The focus of the following sections is to detail the operations that occur during different phases of an App-V Publishing Refresh.</span></span> <span data-ttu-id="83c5c-532">В этой статье рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="83c5c-532">The topics include:</span></span>

-   <span data-ttu-id="83c5c-533">Добавление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-533">Adding an App-V Package</span></span>

-   <span data-ttu-id="83c5c-534">Публикация пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-534">Publishing an App-V Package</span></span>

### <span data-ttu-id="83c5c-535">Добавление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-535">Adding an App-V package</span></span>

<span data-ttu-id="83c5c-536">Добавление пакета App-V на клиент — это первый этап процесса обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-536">Adding an App-V package to the client is the first step of the publishing refresh process.</span></span> <span data-ttu-id="83c5c-537">Конечный результат совпадает с `Add-AppVClientPackage` командлетом в PowerShell (за исключением случаев, когда процесс добавления обновления публикации) отвечает на настроенный сервер публикации и передает ему высокоуровневый список приложений обратно клиенту для получения более подробных сведений, а не одной операции добавления пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-537">The end result is the same as the `Add-AppVClientPackage` cmdlet in PowerShell, except during the publishing refresh add process, the configured publishing server is contacted and passes a high-level list of applications back to the client to pull more detailed information and not a single package add operation.</span></span> <span data-ttu-id="83c5c-538">Процесс продолжается путем настройки клиента для добавления или обновления группы или подключения, а затем для доступа к файлу AppV.</span><span class="sxs-lookup"><span data-stu-id="83c5c-538">The process continues by configuring the client for package or connection group additions or updates, then accesses the appv file.</span></span> <span data-ttu-id="83c5c-539">Затем содержимое AppV файла разворачивается и размещается в локальной операционной системе в соответствующих расположениях.</span><span class="sxs-lookup"><span data-stu-id="83c5c-539">Next, the contents of the appv file are expanded and placed on the local operating system in the appropriate locations.</span></span> <span data-ttu-id="83c5c-540">Ниже приведен подробный рабочий процесс процесса, предполагая, что пакет настроен для потоковой передачи ошибок.</span><span class="sxs-lookup"><span data-stu-id="83c5c-540">The following is a detailed workflow of the process, assuming the package is configured for Fault Streaming.</span></span>

**<span data-ttu-id="83c5c-541">Добавление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-541">How to add an App-V package</span></span>**

1.  <span data-ttu-id="83c5c-542">Ручная Инициация с помощью PowerShell или инициации последовательности задач процесса обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-542">Manual initiation via PowerShell or Task Sequence initiation of the Publishing Refresh process.</span></span>

    1.  <span data-ttu-id="83c5c-543">Клиент App-V делает соединение HTTP и запрашивает список приложений на основе целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="83c5c-543">The App-V Client makes an HTTP connection and requests a list of applications based on the target.</span></span> <span data-ttu-id="83c5c-544">Процесс обновления публикации поддерживает целевые компьютеры или пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-544">The Publishing refresh process supports targeting machines or users.</span></span>

    2.  <span data-ttu-id="83c5c-545">Сервер публикации App-V использует идентификацию целевого объекта, пользователя или компьютера, а также запрос к базе данных для списка приложений, имеющих право.</span><span class="sxs-lookup"><span data-stu-id="83c5c-545">The App-V Publishing Server uses the identity of the initiating target, user or machine, and queries the database for a list of entitled applications.</span></span> <span data-ttu-id="83c5c-546">Список приложений предоставляется в виде ответа XML, который используется клиентом для отправки дополнительных запросов на сервер для получения дополнительных сведений о каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="83c5c-546">The list of applications is provided as an XML response, which the client uses to send additional requests to the server for more information on a per package basis.</span></span>

2.  <span data-ttu-id="83c5c-547">Агент публикаций в клиенте App-V выполняет все действия, приведенные ниже.</span><span class="sxs-lookup"><span data-stu-id="83c5c-547">The Publishing Agent on the App-V Client performs all actions below serialized.</span></span>

    <span data-ttu-id="83c5c-548">Оценка всех групп подключений, которые не опубликованы или отключены, так как обновления версии пакетов, которые являются частью группы подключения, не могут быть обработаны.</span><span class="sxs-lookup"><span data-stu-id="83c5c-548">Evaluate any connection groups that are unpublished or disabled, since package version updates that are part of the connection group cannot be processed.</span></span>

3.  <span data-ttu-id="83c5c-549">Настройте пакеты, определив операции добавления или обновления.</span><span class="sxs-lookup"><span data-stu-id="83c5c-549">Configure the packages by identifying an Add or Update operations.</span></span>

    1.  <span data-ttu-id="83c5c-550">Клиент App-V использует API AppX из Windows и обращается к файлу AppV с сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="83c5c-550">The App-V Client utilizes the AppX API from Windows and accesses the appv file from the publishing server.</span></span>

    2.  <span data-ttu-id="83c5c-551">Файл пакета открывается, а AppXManifest.xml и StreamMap.xml загружаются в хранилище пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-551">The package file is opened and the AppXManifest.xml and StreamMap.xml are downloaded to the Package Store.</span></span>

    3.  <span data-ttu-id="83c5c-552">Полностью потоковые данные блока публикации, определенные в StreamMap.xml.</span><span class="sxs-lookup"><span data-stu-id="83c5c-552">Completely stream publishing block data defined in the StreamMap.xml.</span></span> <span data-ttu-id="83c5c-553">Хранит данные блока публикации в пакете Store\\PkgGUID\\VerGUID\\Root.</span><span class="sxs-lookup"><span data-stu-id="83c5c-553">Stores the publishing block data in the Package Store\\PkgGUID\\VerGUID\\Root.</span></span>

        -   <span data-ttu-id="83c5c-554">Значки: целевые точки расширения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-554">Icons: Targets of extension points.</span></span>

        -   <span data-ttu-id="83c5c-555">Переносимые заголовки (заголовков PE): целевые точки расширения, которые содержат базовые сведения о том, что изображение должно быть доступно на диске, непосредственно из него или с помощью типов файлов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-555">Portable Executable Headers (PE Headers): Targets of extension points that contain the base information about the image need on disk, directly accessed or via file types.</span></span>

        -   <span data-ttu-id="83c5c-556">Сценарии: скачивание каталога сценариев для использования во время публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-556">Scripts: Download scripts directory for use throughout the publishing process.</span></span>

    4.  <span data-ttu-id="83c5c-557">Заполните хранилище пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-557">Populate the Package store:</span></span>

        1.  <span data-ttu-id="83c5c-558">Создавайте разреженные файлы на диске, представляющие извлеченный пакет для всех указанных каталогов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-558">Create sparse files on disk that represent the extracted package for any directories listed.</span></span>

        2.  <span data-ttu-id="83c5c-559">Файлы и каталоги верхнего уровня в корневом каталоге рабочей области.</span><span class="sxs-lookup"><span data-stu-id="83c5c-559">Stage top level files and directories under root.</span></span>

        3.  <span data-ttu-id="83c5c-560">Все остальные файлы создаются в том случае, если папка указана как разреженные на диске и потоковая передача по запросу.</span><span class="sxs-lookup"><span data-stu-id="83c5c-560">All other files are created when the directory is listed as sparse on disk and streamed on demand.</span></span>

    5.  <span data-ttu-id="83c5c-561">Создайте записи каталога компьютеров.</span><span class="sxs-lookup"><span data-stu-id="83c5c-561">Create the machine catalog entries.</span></span> <span data-ttu-id="83c5c-562">Создавайте Manifest.xml и DeploymentConfiguration.xml из файлов пакета (если в пакете не создан файл DeploymentConfiguration.xml).</span><span class="sxs-lookup"><span data-stu-id="83c5c-562">Create the Manifest.xml and DeploymentConfiguration.xml from the package files (if no DeploymentConfiguration.xml file in the package a placeholder is created).</span></span>

    6.  <span data-ttu-id="83c5c-563">Создание места хранения пакетов в реестре HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span><span class="sxs-lookup"><span data-stu-id="83c5c-563">Create location of the package store in the registry HKLM\\Software\\Microsoft\\AppV\\Client\\Packages\\PkgGUID\\Versions\\VerGUID\\Catalog</span></span>

    7.  <span data-ttu-id="83c5c-564">Создайте файл Registry. dat из хранилища пакетов в%ProgramData%\\Microsoft\\AppV\\Client\\VReg\\ {VersionGUID}. dat</span><span class="sxs-lookup"><span data-stu-id="83c5c-564">Create the Registry.dat file from the package store to %ProgramData%\\Microsoft\\AppV\\Client\\VReg\\{VersionGUID}.dat</span></span>

    8.  <span data-ttu-id="83c5c-565">Регистрация пакета с помощью драйвера режима ядра App-V HKLM\\Microsoft\\Software\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="83c5c-565">Register the package with the App-V Kernel Mode Driver HKLM\\Microsoft\\Software\\AppV\\MAV</span></span>

    9.  <span data-ttu-id="83c5c-566">Вызовите сценарии из файла AppxManifest.xml или DeploymentConfig.xml, чтобы добавить время добавления пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-566">Invoke scripting from the AppxManifest.xml or DeploymentConfig.xml file for Package Add timing.</span></span>

4.  <span data-ttu-id="83c5c-567">Настройка групп подключений путем добавления и включения и отключения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-567">Configure Connection Groups by adding and enabling or disabling.</span></span>

5.  <span data-ttu-id="83c5c-568">Удаляйте объекты, которые не опубликованы в целевом объекте (пользователь или компьютер).</span><span class="sxs-lookup"><span data-stu-id="83c5c-568">Remove objects that are not published to the target (user or machine).</span></span>

    <span data-ttu-id="83c5c-569">**Примечание**  Это не приведет к удалению пакета и удалению точек интеграции для определенного целевого объекта (пользователя или компьютера) и удаления файлов каталога пользователей (файлы каталога компьютера для публикации в глобальном каталоге).</span><span class="sxs-lookup"><span data-stu-id="83c5c-569">**Note** This will not perform a package deletion but rather remove integration points for the specific target (user or machine) and remove user catalog files (machine catalog files for globally published).</span></span>

     

6.  <span data-ttu-id="83c5c-570">Вызвать монтирование фоновой нагрузки на основе конфигурации клиента;</span><span class="sxs-lookup"><span data-stu-id="83c5c-570">Invoke background load mounting based on client configuration.</span></span>

7.  <span data-ttu-id="83c5c-571">Пакеты, у которых уже есть сведения о публикации для компьютера или пользователя, немедленно восстанавливаются.</span><span class="sxs-lookup"><span data-stu-id="83c5c-571">Packages that already have publishing information for the machine or user are immediately restored.</span></span>

    <span data-ttu-id="83c5c-572">**Примечание**  Это условие выполняется как произведение удаления без отмены публикации в фоновом добавлении пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-572">**Note** This condition occurs as a product of removal without unpublishing with background addition of the package.</span></span>

     

<span data-ttu-id="83c5c-573">После этого пакет App-V добавляет процесс обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-573">This completes an App-V package add of the publishing refresh process.</span></span> <span data-ttu-id="83c5c-574">Следующий шаг — Публикация пакета для определенного целевого объекта (компьютера или пользователя).</span><span class="sxs-lookup"><span data-stu-id="83c5c-574">The next step is publishing the package to the specific target (machine or user).</span></span>

![Упаковка добавления файлов и данных реестра](images/packageaddfileandregistrydata.png)

### <span data-ttu-id="83c5c-576">Публикация пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-576">Publishing an App-V package</span></span>

<span data-ttu-id="83c5c-577">В ходе операции обновления публикации определенная операция публикации (Publish-AppVClientPackage) добавляет записи в пользовательский каталог, сопоставляет данные с пользователем, определяет локальное хранилище и завершает работу, выполняя все этапы интеграции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-577">During the Publishing Refresh operation, the specific publishing operation (Publish-AppVClientPackage) adds entries to the user catalog, maps entitlement to the user, identifies the local store, and finishes by completing any integration steps.</span></span> <span data-ttu-id="83c5c-578">Ниже приведены подробные инструкции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-578">The following are the detailed steps.</span></span>

**<span data-ttu-id="83c5c-579">Публикация пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-579">How to publish and App-V package</span></span>**

1.  <span data-ttu-id="83c5c-580">Записи пакетов добавляются в каталог пользователей</span><span class="sxs-lookup"><span data-stu-id="83c5c-580">Package entries are added to the user catalog</span></span>

    1.  <span data-ttu-id="83c5c-581">Пакеты, предназначенные для пользователей: UserDeploymentConfiguration.xml и UserManifest.xml размещаются на компьютере в каталоге пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-581">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the User Catalog</span></span>

    2.  <span data-ttu-id="83c5c-582">Целевые (глобальные) пакеты для компьютера: UserDeploymentConfiguration.xml помещено в каталог компьютера;</span><span class="sxs-lookup"><span data-stu-id="83c5c-582">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the Machine Catalog</span></span>

2.  <span data-ttu-id="83c5c-583">Регистрация пакета с помощью драйвера режима ядра для пользователя на HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="83c5c-583">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

3.  <span data-ttu-id="83c5c-584">Выполнение задач интеграции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-584">Perform integration tasks.</span></span>

    1.  <span data-ttu-id="83c5c-585">Создание точек расширения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-585">Create extension points.</span></span>

    2.  <span data-ttu-id="83c5c-586">Храните резервные копии в реестре пользователя и перемещаемом профиле (Архивация ярлыков).</span><span class="sxs-lookup"><span data-stu-id="83c5c-586">Store backup information in the user’s registry and roaming profile (Shortcut Backups).</span></span>

        <span data-ttu-id="83c5c-587">**Примечание**  Это позволяет восстановить точки расширения, если пакет не опубликован.</span><span class="sxs-lookup"><span data-stu-id="83c5c-587">**Note** This enables restore extension points if the package is unpublished.</span></span>

         

    3.  <span data-ttu-id="83c5c-588">Выполнение сценариев, предназначенных для синхронизации публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-588">Run scripts targeted for publishing timing.</span></span>

<span data-ttu-id="83c5c-589">Публикация пакета App-V, который входит в группу соединения, очень похожа на описанный выше процесс.</span><span class="sxs-lookup"><span data-stu-id="83c5c-589">Publishing an App-V Package that is part of a Connection Group is very similar to the above process.</span></span> <span data-ttu-id="83c5c-590">Для групп подключений путь, хранящий определенную информацию о каталоге, включает PackageGroups в качестве дочернего элемента каталога каталога.</span><span class="sxs-lookup"><span data-stu-id="83c5c-590">For connection groups, the path that stores the specific catalog information includes PackageGroups as a child of the Catalog Directory.</span></span> <span data-ttu-id="83c5c-591">Ознакомьтесь со сведениями о каталоге компьютеров и пользователей выше, чтобы получить подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-591">Review the machine and users catalog information above for details.</span></span>

![пакет добавляет данные файлов и реестра — Global](images/packageaddfileandregistrydata-global.png)

### <span data-ttu-id="83c5c-593">Запуск приложения</span><span class="sxs-lookup"><span data-stu-id="83c5c-593">Application launch</span></span>

<span data-ttu-id="83c5c-594">После обновления публикации пользователь запускается и затем повторно запускает приложение App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-594">After the Publishing Refresh process, the user launches and subsequently re-launches an App-V application.</span></span> <span data-ttu-id="83c5c-595">Процесс очень прост и оптимизирован для быстрого запуска с минимальным объемом сетевого трафика.</span><span class="sxs-lookup"><span data-stu-id="83c5c-595">The process is very simple and optimized to launch quickly with a minimum of network traffic.</span></span> <span data-ttu-id="83c5c-596">Клиент App-V проверяет путь к каталогу пользователей для файлов, создаваемых во время публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-596">The App-V Client checks the path to the user catalog for files created during publishing.</span></span> <span data-ttu-id="83c5c-597">После установления прав на запуск пакета клиент App-V создает виртуальную среду, начинает потоковую передачу необходимых данных и применяет соответствующие файлы конфигурации манифеста и развертывания во время создания виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="83c5c-597">After rights to launch the package are established, the App-V Client creates a virtual environment, begins streaming any necessary data, and applies the appropriate manifest and deployment configuration files during virtual environment creation.</span></span> <span data-ttu-id="83c5c-598">С помощью виртуальной среды, созданной и настроенной для определенного пакета и приложения, запускается приложение.</span><span class="sxs-lookup"><span data-stu-id="83c5c-598">With the virtual environment created and configured for the specific package and application, the application starts.</span></span>

**<span data-ttu-id="83c5c-599">Запуск приложений App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-599">How to launch App-V applications</span></span>**

1.  <span data-ttu-id="83c5c-600">Пользователь запускает приложение, щелкая ярлык или тип файла.</span><span class="sxs-lookup"><span data-stu-id="83c5c-600">User launches the application by clicking on a shortcut or file type invocation.</span></span>

2.  <span data-ttu-id="83c5c-601">Клиент App-V проверяет наличие указанных ниже файлов в каталоге пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-601">The App-V Client verifies existence in the User Catalog for the following files</span></span>

    -   <span data-ttu-id="83c5c-602">UserDeploymentConfiguration.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-602">UserDeploymentConfiguration.xml</span></span>

    -   <span data-ttu-id="83c5c-603">UserManifest.xml</span><span class="sxs-lookup"><span data-stu-id="83c5c-603">UserManifest.xml</span></span>

3.  <span data-ttu-id="83c5c-604">Если файлы находятся в списке, это значит, что приложение предназначено для определенного пользователя, и приложение запустит процесс для запуска.</span><span class="sxs-lookup"><span data-stu-id="83c5c-604">If the files are present, the application is entitled for that specific user and the application will start the process for launch.</span></span> <span data-ttu-id="83c5c-605">На этом этапе отсутствует сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="83c5c-605">There is no network traffic at this point.</span></span>

4.  <span data-ttu-id="83c5c-606">Затем клиент App-V проверяет, является ли путь к пакету, зарегистрированному для службы клиента App-V, найденным в реестре.</span><span class="sxs-lookup"><span data-stu-id="83c5c-606">Next, the App-V Client checks that the path for the package registered for the App-V Client service is found in the registry.</span></span>

5.  <span data-ttu-id="83c5c-607">После того как вы нашли путь к хранилищу пакетов, создается виртуальная среда.</span><span class="sxs-lookup"><span data-stu-id="83c5c-607">Upon finding the path to the package store, the virtual environment is created.</span></span> <span data-ttu-id="83c5c-608">Если это первый запуск, основной блок функций загружается, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="83c5c-608">If this is the first launch, the Primary Feature Block downloads if present.</span></span>

6.  <span data-ttu-id="83c5c-609">После загрузки служба клиента App-V использует файлы конфигурации манифеста и развертывания для настройки виртуальной среды и загрузки всех подсистем App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-609">After downloading, the App-V Client service consumes the manifest and deployment configuration files to configure the virtual environment and all App-V subsystems are loaded.</span></span>

7.  <span data-ttu-id="83c5c-610">Запускается приложение.</span><span class="sxs-lookup"><span data-stu-id="83c5c-610">The Application launches.</span></span> <span data-ttu-id="83c5c-611">Для любых отсутствующих файлов в хранилище пакетов (разреженные файлы) приложение App-V будет перезаписывать ошибки файлов по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="83c5c-611">For any missing files in the package store (sparse files), App-V will stream fault the files on an as needed basis.</span></span>

    ![пакет добавить данные файла и реестра — Stream](images/packageaddfileandregistrydata-stream.png)

### <span data-ttu-id="83c5c-613">Обновление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-613">Upgrading an App-V package</span></span>

<span data-ttu-id="83c5c-614">Процесс обновления пакета App-V 5 отличается от предыдущих версий App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-614">The App-V 5 package upgrade process differs from the older versions of App-V.</span></span> <span data-ttu-id="83c5c-615">Приложение App-V поддерживает несколько версий одного пакета на компьютере, предназначенном для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-615">App-V supports multiple versions of the same package on a machine entitled to different users.</span></span> <span data-ttu-id="83c5c-616">Версии пакетов можно добавлять в любое время, так как в магазине и каталоги пакетов будут обновляться с учетом новых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-616">Package versions can be added at any time as the package store and catalogs are updated with the new resources.</span></span> <span data-ttu-id="83c5c-617">Единственный процесс, относящийся к добавлению новых ресурсов версий, — это Оптимизация хранилища.</span><span class="sxs-lookup"><span data-stu-id="83c5c-617">The only process specific to the addition of new version resources is storage optimization.</span></span> <span data-ttu-id="83c5c-618">Во время обновления в новом расположении в хранилище версий добавляются только новые файлы, а для файлов с неизмененными изменениями создаются жесткие ссылки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-618">During an upgrade, only the new files are added to the new version store location and hard links are created for unchanged files.</span></span> <span data-ttu-id="83c5c-619">Это уменьшает общее хранилище, выводит файл только на одном диске, а затем проецирование во все папки с помощью записи расположения файла на диске.</span><span class="sxs-lookup"><span data-stu-id="83c5c-619">This reduces the overall storage by only presenting the file on one disk location and then projecting it into all folders with a file location entry on the disk.</span></span> <span data-ttu-id="83c5c-620">Ниже указаны некоторые сведения об обновлении пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-620">The specific details of upgrading an App-V Package are as follows:</span></span>

**<span data-ttu-id="83c5c-621">Обновление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-621">How to upgrade an App-V package</span></span>**

1.  <span data-ttu-id="83c5c-622">Клиент App-V выполняет обновление публикации и открывают более новую версию пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-622">The App-V Client performs a Publishing Refresh and discovers a newer version of an App-V Package.</span></span>

2.  <span data-ttu-id="83c5c-623">Записи пакета добавляются в соответствующий каталог для новой версии</span><span class="sxs-lookup"><span data-stu-id="83c5c-623">Package entries are added to the appropriate catalog for the new version</span></span>

    1.  <span data-ttu-id="83c5c-624">Пакеты, предназначенные для пользователей: UserDeploymentConfiguration.xml и UserManifest.xml размещаются на компьютере в каталоге пользователей по адресу appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="83c5c-624">User targeted packages: the UserDeploymentConfiguration.xml and UserManifest.xml are placed on the machine in the user catalog at appdata\\roaming\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

    2.  <span data-ttu-id="83c5c-625">Целевые (глобальные) пакеты для компьютера: UserDeploymentConfiguration.xml помещены в каталог Machine по адресу%programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span><span class="sxs-lookup"><span data-stu-id="83c5c-625">Machine targeted (global) packages: the UserDeploymentConfiguration.xml is placed in the machine catalog at %programdata%\\Microsoft\\AppV\\Client\\Catalog\\Packages\\PkgGUID\\VerGUID</span></span>

3.  <span data-ttu-id="83c5c-626">Регистрация пакета с помощью драйвера режима ядра для пользователя на HKLM\\Software\\Microsoft\\AppV\\MAV</span><span class="sxs-lookup"><span data-stu-id="83c5c-626">Register the package with the kernel mode driver for the user at HKLM\\Software\\Microsoft\\AppV\\MAV</span></span>

4.  <span data-ttu-id="83c5c-627">Выполнение задач интеграции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-627">Perform integration tasks.</span></span>

    -   <span data-ttu-id="83c5c-628">Интегрируйте точки расширения (EP) из файлов манифеста и динамической конфигурации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-628">Integrate extensions points (EP) from the Manifest and Dynamic Configuration files.</span></span>

    1.  <span data-ttu-id="83c5c-629">Данные EP на основе файлов хранятся в папке AppData с использованием точек соединения из хранилища пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-629">File based EP data is stored in the AppData folder utilizing Junction Points from the package store.</span></span>

    2.  <span data-ttu-id="83c5c-630">Если новая версия станет доступна, Внешняя спецификация версии 1 уже существует.</span><span class="sxs-lookup"><span data-stu-id="83c5c-630">Version 1 EPs already exist when a new version becomes available.</span></span>

    3.  <span data-ttu-id="83c5c-631">Точки расширения переключаются на расположение версии 2 в каталогах компьютеров или пользователей для новых или обновленных точек расширения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-631">The extension points are switched to the Version 2 location in machine or user catalogs for any newer or updated extension points.</span></span>

5.  <span data-ttu-id="83c5c-632">Выполнение сценариев, предназначенных для синхронизации публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-632">Run scripts targeted for publishing timing.</span></span>

6.  <span data-ttu-id="83c5c-633">Устанавливайте параллельные сборки по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="83c5c-633">Install Side by Side assemblies as required.</span></span>

### <span data-ttu-id="83c5c-634">Обновление используемого пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-634">Upgrading an in-use App-V package</span></span>

<span data-ttu-id="83c5c-635">**Начиная с версии App-V 5 SP2**: при попытке обновить пакет, который используется конечным пользователем, задача обновления будет находиться в состоянии ожидания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-635">**Starting in App-V 5 SP2**: If you try to upgrade a package that is in use by an end user, the upgrade task is placed in a pending state.</span></span> <span data-ttu-id="83c5c-636">Обновление будет запущено позже в соответствии с приведенными ниже правилами.</span><span class="sxs-lookup"><span data-stu-id="83c5c-636">The upgrade will run later, according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-637">Тип задачи</span><span class="sxs-lookup"><span data-stu-id="83c5c-637">Task type</span></span></th>
<th align="left"><span data-ttu-id="83c5c-638">Применимое правило</span><span class="sxs-lookup"><span data-stu-id="83c5c-638">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-639">Пользовательская задача, например Публикация пакета для пользователя</span><span class="sxs-lookup"><span data-stu-id="83c5c-639">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-640">Задача будет выполнена после того, как пользователь войдет в систему, а затем снова войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="83c5c-640">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-641">Глобально на основе задач, например включение глобальной группы подключения</span><span class="sxs-lookup"><span data-stu-id="83c5c-641">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-642">Задача, ожидающая выполнения, будет выполнена после отключения компьютера и повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="83c5c-642">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83c5c-643">Когда задача размещается в состоянии ожидания, клиент App-V также создает раздел реестра для задачи с отложенным вводом, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="83c5c-643">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-644">Задача на основе пользователей или глобально</span><span class="sxs-lookup"><span data-stu-id="83c5c-644">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="83c5c-645">Где создается раздел реестра</span><span class="sxs-lookup"><span data-stu-id="83c5c-645">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-646">Пользовательские задачи</span><span class="sxs-lookup"><span data-stu-id="83c5c-646">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-647">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="83c5c-647">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-648">Глобально на основе задач</span><span class="sxs-lookup"><span data-stu-id="83c5c-648">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-649">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="83c5c-649">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83c5c-650">Прежде чем пользователи смогут использовать новую версию пакета, необходимо выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="83c5c-650">The following operations must be completed before users can use the newer version of the package:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-651">Задача</span><span class="sxs-lookup"><span data-stu-id="83c5c-651">Task</span></span></th>
<th align="left"><span data-ttu-id="83c5c-652">Сведения</span><span class="sxs-lookup"><span data-stu-id="83c5c-652">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-653">Добавление пакета на компьютер</span><span class="sxs-lookup"><span data-stu-id="83c5c-653">Add the package to the computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-654">Эта задача предназначена для определенного компьютера, и вы можете сделать это в любое время, выполнив действия, описанные в разделе Добавление пакета выше.</span><span class="sxs-lookup"><span data-stu-id="83c5c-654">This task is computer specific and you can perform it at any time by completing the steps in the Package Add section above.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-655">Публикация пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-655">Publish the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-656">Инструкции приведены в разделе Публикация пакетов выше.</span><span class="sxs-lookup"><span data-stu-id="83c5c-656">See the Package Publishing section above for steps.</span></span> <span data-ttu-id="83c5c-657">Для этого процесса требуется обновить точки расширения в системе.</span><span class="sxs-lookup"><span data-stu-id="83c5c-657">This process requires that you update extension points on the system.</span></span> <span data-ttu-id="83c5c-658">Конечные пользователи не могут использовать приложение, когда вы закончите эту задачу.</span><span class="sxs-lookup"><span data-stu-id="83c5c-658">End users cannot be using the application when you complete this task.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="83c5c-659">Воспользуйтесь приведенными ниже примерами сценариев в качестве руководства по обновлению пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-659">Use the following example scenarios as a guide for updating packages.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-660">Сценарий</span><span class="sxs-lookup"><span data-stu-id="83c5c-660">Scenario</span></span></th>
<th align="left"><span data-ttu-id="83c5c-661">Требования</span><span class="sxs-lookup"><span data-stu-id="83c5c-661">Requirements</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-662">Пакет App-V не используется при попытке обновления</span><span class="sxs-lookup"><span data-stu-id="83c5c-662">App-V package is not in use when you try to upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-663">Ни один из следующих компонентов пакета не может быть использован: виртуальное приложение, COM-сервер или расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-663">None of the following components of the package can be in use: virtual application, COM server, or shell extensions.</span></span></p>
<p><span data-ttu-id="83c5c-664">Администратор публикует более новую версию пакета, и обновление работает при следующем запуске компонента или приложения в пакете.</span><span class="sxs-lookup"><span data-stu-id="83c5c-664">The administrator publishes a newer version of the package and the upgrade works the next time a component or application inside the package is launched.</span></span> <span data-ttu-id="83c5c-665">Новая версия пакета помещается в поток и выполняется.</span><span class="sxs-lookup"><span data-stu-id="83c5c-665">The new version of the package is streamed and run.</span></span> <span data-ttu-id="83c5c-666">В этом сценарии ничего не изменилось в App-V 5 SP2 из предыдущих выпусков App-V 5.</span><span class="sxs-lookup"><span data-stu-id="83c5c-666">Nothing has changed in this scenario in App-V 5 SP2 from previous releases of App-V 5.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-667">Пакет App-V используется, когда администратор публикует более новую версию пакета</span><span class="sxs-lookup"><span data-stu-id="83c5c-667">App-V package is in use when the administrator publishes a newer version of the package</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-668">Для операции обновления установлен режим ожидания клиента App-V, что означает, что он находится в очереди и выполняется позже, когда пакет не используется.</span><span class="sxs-lookup"><span data-stu-id="83c5c-668">The upgrade operation is set to pending by the App-V Client, which means that it is queued and carried out later when the package is not in use.</span></span></p>
<p><span data-ttu-id="83c5c-669">Если приложение пакета используется, пользователь закрывает виртуальное приложение, после чего может происходить обновление.</span><span class="sxs-lookup"><span data-stu-id="83c5c-669">If the package application is in use, the user shuts down the virtual application, after which the upgrade can occur.</span></span></p>
<p><span data-ttu-id="83c5c-670">Если в пакете есть расширения оболочки (Office 2013), которые окончательно загружаются проводником Windows, пользователь не может войти в систему.</span><span class="sxs-lookup"><span data-stu-id="83c5c-670">If the package has shell extensions (Office 2013), which are permanently loaded by Windows Explorer, the user cannot be logged in.</span></span> <span data-ttu-id="83c5c-671">Пользователи должны выйти из системы и снова войти в систему, чтобы начать обновление пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-671">Users must log off and the log back in to initiate the App-V package upgrade.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83c5c-672">Глобальная публикация пользователей и групп</span><span class="sxs-lookup"><span data-stu-id="83c5c-672">Global vs user publishing</span></span>

<span data-ttu-id="83c5c-673">Пакеты App-V можно публиковать одним из двух способов: Пользователь, который имеет право на доступ пакета App-V к определенному пользователю или группе пользователей и глобальным пользователям, которые имеют доступ к пакету App-V для всего компьютера для всех пользователей компьютера.</span><span class="sxs-lookup"><span data-stu-id="83c5c-673">App-V Packages can be published in one of two ways; User which entitles an App-V package to a specific user or group of users and Global which entitles the App-V package to the entire machine for all users of the machine.</span></span> <span data-ttu-id="83c5c-674">После завершения обновления пакета, если пакет App-V не используется, рассматривайте два типа публикации:</span><span class="sxs-lookup"><span data-stu-id="83c5c-674">Once a package upgrade has been pended and the App-V package is not in use, consider the two types of publishing:</span></span>

-   <span data-ttu-id="83c5c-675">**Опубликовано глобально**: приложение опубликовано на компьютере; все пользователи на этом компьютере могут использовать его.</span><span class="sxs-lookup"><span data-stu-id="83c5c-675">**Globally published**: the application is published to a machine; all users on that machine can use it.</span></span> <span data-ttu-id="83c5c-676">Обновление происходит при запуске клиентской службы App-V, что фактически означает перезагрузку компьютера.</span><span class="sxs-lookup"><span data-stu-id="83c5c-676">The upgrade will happen when the App-V Client Service starts, which effectively means a machine restart.</span></span>

-   <span data-ttu-id="83c5c-677">**Опубликованные пользователи**: приложение опубликовано для пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-677">**User published**: the application is published to a user.</span></span> <span data-ttu-id="83c5c-678">Если на компьютере несколько пользователей, приложение можно опубликовать в подмножестве пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-678">If there are multiple users on the machine, the application can be published to a subset of the users.</span></span> <span data-ttu-id="83c5c-679">Обновление происходит при входе пользователя в систему или при повторной его публикации (периодическое обновление политики ConfigMgr, его оценка или периодическая публикация и обновление приложения-V или явное применение команд PowerShell).</span><span class="sxs-lookup"><span data-stu-id="83c5c-679">The upgrade will happen when the user logs in or when it is published again (periodically, ConfigMgr Policy refresh and evaluation, or an App-V periodic publishing/refresh, or explicitly via PowerShell commands).</span></span>

### <span data-ttu-id="83c5c-680">Удаление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-680">Removing an App-V package</span></span>

<span data-ttu-id="83c5c-681">Удаление приложений App-V в полной инфраструктуре является операцией отмены публикации и не выполняет удаление пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-681">Removing App-V applications in a Full Infrastructure is an unpublish operation, and does not perform a package removal.</span></span> <span data-ttu-id="83c5c-682">Процесс аналогичен процессу публикации, но вместо добавления процесса удаления изменяет изменения, внесенные в пакеты App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-682">The process is the same as the publish process above, but instead of adding the removal process reverses the changes that have been made for App-V Packages.</span></span>

### <span data-ttu-id="83c5c-683">Восстановление пакета App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-683">Repairing an App-V package</span></span>

<span data-ttu-id="83c5c-684">Операция восстановления очень проста, но может повлиять на многие места на компьютере.</span><span class="sxs-lookup"><span data-stu-id="83c5c-684">The repair operation is very simple but may affect many locations on the machine.</span></span> <span data-ttu-id="83c5c-685">Ранее указанные места в разделе "запись (COW)" удаляются, а точки расширения становятся неинтегрированными, а затем снова интегрируются.</span><span class="sxs-lookup"><span data-stu-id="83c5c-685">The previously mentioned Copy on Write (COW) locations are removed, and extension points are de-integrated and then re-integrated.</span></span> <span data-ttu-id="83c5c-686">Просмотрите места расположения данных COW, просмотрев, где они зарегистрированы в реестре.</span><span class="sxs-lookup"><span data-stu-id="83c5c-686">Please review the COW data placement locations by reviewing where they are registered in the registry.</span></span> <span data-ttu-id="83c5c-687">Эта операция выполняется автоматически, но отсутствует административный элемент управления, не управляющий операцией восстановления на клиентской консоли App-V или через PowerShell (Repair-AppVClientPackage).</span><span class="sxs-lookup"><span data-stu-id="83c5c-687">This operation is done automatically and there is no administrative control other than initiating a Repair operation from the App-V Client Console or via PowerShell (Repair-AppVClientPackage).</span></span>

## <a href="" id="bkmk-integr-appv-pkgs"></a><span data-ttu-id="83c5c-688">Интеграция пакетов App-V</span><span class="sxs-lookup"><span data-stu-id="83c5c-688">Integration of App-V packages</span></span>


<span data-ttu-id="83c5c-689">Архитектура клиента и пакета App-V обеспечивает определенную интеграцию с локальной операционной системой во время добавления и публикации пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-689">The App-V Client and package architecture provides specific integration with the local operating system during the addition and publishing of packages.</span></span> <span data-ttu-id="83c5c-690">Три файла определяют точки интеграции или расширения для пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-690">Three files define the integration or extension points for an App-V Package:</span></span>

-   <span data-ttu-id="83c5c-691">AppXManifest.xml: хранимые в пакете резервные копии, хранящиеся в хранилище пакетов и в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-691">AppXManifest.xml: Stored inside of the package with fallback copies stored in the package store and the user profile.</span></span> <span data-ttu-id="83c5c-692">Содержат параметры, созданные в процессе упорядочивания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-692">Contains the options created during the sequencing process.</span></span>

-   <span data-ttu-id="83c5c-693">DeploymentConfig.xml: предоставляет сведения о конфигурации точек расширения интеграции на компьютере и на основе пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-693">DeploymentConfig.xml: Provides configuration information of computer and user based integration extension points.</span></span>

-   <span data-ttu-id="83c5c-694">UserConfig.xml: подмножество Deploymentconfig.xml, предоставляющее только пользовательские конфигурации и предназначенные только целевые точки расширения на основе пользователей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-694">UserConfig.xml: A subset of the Deploymentconfig.xml that only provides user- based configurations and only targets user-based extension points.</span></span>

### <span data-ttu-id="83c5c-695">Правила интеграции</span><span class="sxs-lookup"><span data-stu-id="83c5c-695">Rules of integration</span></span>

<span data-ttu-id="83c5c-696">Когда приложения App-V публикуются на компьютере с клиентом App-V, выполняются некоторые действия, описанные в приведенном ниже списке.</span><span class="sxs-lookup"><span data-stu-id="83c5c-696">When App-V applications are published to a computer with the App-V Client, some specific actions take place as described in the list below:</span></span>

-   <span data-ttu-id="83c5c-697">Глобальная публикация: сочетания клавиш хранятся в расположении профиля "все пользователи", а другие точки расширения хранятся в реестре куста HKLM.</span><span class="sxs-lookup"><span data-stu-id="83c5c-697">Global Publishing: Shortcuts are stored in the All Users profile location and other extension points are stored in the registry in the HKLM hive.</span></span>

-   <span data-ttu-id="83c5c-698">Публикация пользователей: сочетания клавиш хранятся в текущем профиле учетной записи пользователя, а другие точки расширения хранятся в реестре в кусте HKCU.</span><span class="sxs-lookup"><span data-stu-id="83c5c-698">User Publishing: Shortcuts are stored in the current user account profile and other extension points are stored in the registry in the HKCU hive.</span></span>

-   <span data-ttu-id="83c5c-699">Резервное копирование и восстановление: существующие данные собственного приложения и реестр (например, регистрация FTA) записываются в резервную копию во время публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-699">Backup and Restore: Existing native application data and registry (such as FTA registrations) are backed up during publishing.</span></span>

    1.  <span data-ttu-id="83c5c-700">Пакеты App-V получают владение на основе последнего интегрированного пакета, в котором владение передается в последнее опубликованное приложение App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-700">App-V packages are given ownership based on the last integrated package where the ownership is passed to the newest published App-V application.</span></span>

    2.  <span data-ttu-id="83c5c-701">Передача владения из одного пакета App-V в другой при публикации пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-701">Ownership transfers from one App-V package to another when the owning App-V package is unpublished.</span></span> <span data-ttu-id="83c5c-702">Это не приведет к восстановлению данных или реестра.</span><span class="sxs-lookup"><span data-stu-id="83c5c-702">This will not initiate a restore of the data or registry.</span></span>

    3.  <span data-ttu-id="83c5c-703">Восстановление заархивированных данных при разпубликации и удалении последнего пакета для каждой точки расширения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-703">Restore the backed up data when the last package is unpublished or removed on a per extension point basis.</span></span>

### <span data-ttu-id="83c5c-704">Точки расширения</span><span class="sxs-lookup"><span data-stu-id="83c5c-704">Extension points</span></span>

<span data-ttu-id="83c5c-705">Файлы публикации App-V (манифест и динамическая конфигурация) предоставляют несколько точек расширения, которые позволяют приложению интегрироваться с локальной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="83c5c-705">The App-V publishing files (manifest and dynamic configuration) provide several extension points that enable the application to integrate with the local operating system.</span></span> <span data-ttu-id="83c5c-706">Эти точки расширения выполняют типичные задачи по установке приложений, такие как размещение сочетаний клавиш, создание сопоставлений типов файлов и регистрация компонентов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-706">These extension points perform typical application installation tasks, such as placing shortcuts, creating file type associations, and registering components.</span></span> <span data-ttu-id="83c5c-707">Так как это виртуализированные приложения, которые не установлены так же, как традиционное приложение, существует ряд отличий.</span><span class="sxs-lookup"><span data-stu-id="83c5c-707">As these are virtualized applications that are not installed in the same manner a traditional application, there are some differences.</span></span> <span data-ttu-id="83c5c-708">Ниже приведен список точек расширения, описанных в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="83c5c-708">The following is a list of extension points covered in this section:</span></span>

-   <span data-ttu-id="83c5c-709">Горячие</span><span class="sxs-lookup"><span data-stu-id="83c5c-709">Shortcuts</span></span>

-   <span data-ttu-id="83c5c-710">Сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="83c5c-710">File Type Associations</span></span>

-   <span data-ttu-id="83c5c-711">Расширения оболочки</span><span class="sxs-lookup"><span data-stu-id="83c5c-711">Shell Extensions</span></span>

-   <span data-ttu-id="83c5c-712">НАДСТРОЙК</span><span class="sxs-lookup"><span data-stu-id="83c5c-712">COM</span></span>

-   <span data-ttu-id="83c5c-713">Клиенты программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="83c5c-713">Software Clients</span></span>

-   <span data-ttu-id="83c5c-714">Возможности приложения</span><span class="sxs-lookup"><span data-stu-id="83c5c-714">Application capabilities</span></span>

-   <span data-ttu-id="83c5c-715">Обработчик протокола URL-адреса</span><span class="sxs-lookup"><span data-stu-id="83c5c-715">URL Protocol Handler</span></span>

-   <span data-ttu-id="83c5c-716">AppPath</span><span class="sxs-lookup"><span data-stu-id="83c5c-716">AppPath</span></span>

-   <span data-ttu-id="83c5c-717">Виртуальное приложение</span><span class="sxs-lookup"><span data-stu-id="83c5c-717">Virtual Application</span></span>

### <span data-ttu-id="83c5c-718">Горячие</span><span class="sxs-lookup"><span data-stu-id="83c5c-718">Shortcuts</span></span>

<span data-ttu-id="83c5c-719">Краткое вырезание — это один из основных элементов интеграции с ОС и является интерфейсом для непосредственного запуска приложения App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-719">The short cut is one of the basic elements of integration with the OS and is the interface for direct user launch of an App-V application.</span></span> <span data-ttu-id="83c5c-720">Во время публикации и отмены публикации приложений App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-720">During the publishing and unpublishing of App-V applications.</span></span>

<span data-ttu-id="83c5c-721">Из манифеста пакета и XML-файлов динамической конфигурации путь к определенному исполняемому файлу приложения можно найти в разделе, аналогичном следующему:</span><span class="sxs-lookup"><span data-stu-id="83c5c-721">From the package manifest and dynamic configuration XML files, the path to a specific application executable can be found in a section similar to the following:</span></span>

```xml
<Extension Category="AppV.Shortcut">
          <Shortcut>
            <File>[{Common Desktop}]\Adobe Reader 9.lnk</File>
            <Target>[{AppVPackageRoot}]\Reader\AcroRd32.exe</Target>
            <Icon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\SC_Reader.ico</Icon>
            <Arguments />
            <WorkingDirectory />
            <ShowCommand>1</ShowCommand>
            <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
          </Shortcut>
        </Extension>
```

<span data-ttu-id="83c5c-722">Как упоминалось ранее, сочетания клавиш App-V помещаются по умолчанию в пользовательском профиле в соответствии с операцией обновления.</span><span class="sxs-lookup"><span data-stu-id="83c5c-722">As mentioned previously, the App-V shortcuts are placed by default in the user’s profile based on the refresh operation.</span></span> <span data-ttu-id="83c5c-723">Общие сочетания клавиш в профиле All Users и User Refresh хранят их в определенном пользователем профиле.</span><span class="sxs-lookup"><span data-stu-id="83c5c-723">Global refresh places shortcuts in the All Users profile and user refresh stores them in the specific user’s profile.</span></span> <span data-ttu-id="83c5c-724">Фактический исполняемый файл хранится в хранилище пакетов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-724">The actual executable is stored in the Package Store.</span></span> <span data-ttu-id="83c5c-725">Расположение ICO-файла — это расположение, в котором размещается лексема в пакете App + V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-725">The location of the ICO file is a tokenized location in the App-V package.</span></span>

### <span data-ttu-id="83c5c-726">Сопоставления типов файлов</span><span class="sxs-lookup"><span data-stu-id="83c5c-726">File type associations</span></span>

<span data-ttu-id="83c5c-727">Клиент App-V управляет связями типов файлов локальной операционной системы во время публикации, что позволяет пользователям использовать вызовы типов файлов или открывать файлы с особым зарегистрированным расширением (DOCX) для запуска приложения App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-727">The App-V Client manages the local operating system File Type Associations during publishing, which enables users to use file type invocations or to open a file with a specifically registered extension (.docx) to start an App-V application.</span></span> <span data-ttu-id="83c5c-728">Сопоставления типов файлов представлены в файлах манифеста и динамической конфигурации, как показано в примере ниже.</span><span class="sxs-lookup"><span data-stu-id="83c5c-728">File type associations are present in the manifest and dynamic configuration files as represented in the example below:</span></span>

```xml
<Extension Category="AppV.FileTypeAssociation">
          <FileTypeAssociation>
            <FileExtension MimeAssociation="true">
              <Name>.xdp</Name>
              <ProgId>AcroExch.XDPDoc</ProgId>
              <ContentType>application/vnd.adobe.xdp+xml</ContentType>
            </FileExtension>
            <ProgId>
              <Name>AcroExch.XDPDoc</Name>
              <Description>Adobe Acrobat XML Data Package File</Description>
              <EditFlags>65536</EditFlags>
              <DefaultIcon>[{Windows}]\Installer\{AC76BA86-7AD7-1033-7B44-A94000000001}\XDPFile_8.ico</DefaultIcon>
              <ShellCommands>
                <DefaultCommand>Read</DefaultCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Open</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Printto</Name>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe"  /t "%1" "%2" "%3" "%4"</CommandLine>
                </ShellCommand>
                <ShellCommand>
                  <ApplicationId>[{AppVPackageRoot}]\Reader\AcroRd32.exe</ApplicationId>
                  <Name>Read</Name>
                  <FriendlyName>Open with Adobe Reader 9</FriendlyName>
                  <CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>
                </ShellCommand>
              </ShellCommands>
            </ProgId>
          </FileTypeAssociation>
        </Extension>
```

<span data-ttu-id="83c5c-729">**Примечание**  В этом примере:</span><span class="sxs-lookup"><span data-stu-id="83c5c-729">**Note** In this example:</span></span>

-   `<Name>.xdp</Name>` <span data-ttu-id="83c5c-730">является расширением</span><span class="sxs-lookup"><span data-stu-id="83c5c-730">is the extension</span></span>

-   `<Name>AcroExch.XDPDoc</Name>` <span data-ttu-id="83c5c-731">значение ProgId (которое указывает на смежный ProgId)</span><span class="sxs-lookup"><span data-stu-id="83c5c-731">is the ProgId value (which points to the adjoining ProgId)</span></span>

-   `<CommandLine>"[{AppVPackageRoot}]\Reader\AcroRd32.exe" "%1"</CommandLine>` <span data-ttu-id="83c5c-732">— Это Командная строка, указывающая на исполняемый файл приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-732">is the command line, which points to the application executable</span></span>

 

### <span data-ttu-id="83c5c-733">Расширения оболочки</span><span class="sxs-lookup"><span data-stu-id="83c5c-733">Shell extensions</span></span>

<span data-ttu-id="83c5c-734">Расширения оболочки встраиваются в пакет автоматически в процессе упорядочивания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-734">Shell extensions are embedded in the package automatically during the sequencing process.</span></span> <span data-ttu-id="83c5c-735">Если пакет опубликован глобально, расширение оболочки предоставляет пользователям те же функциональные возможности, что и при локальном установлении приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-735">When the package is published globally, the shell extension gives users the same functionality as if the application were locally installed.</span></span> <span data-ttu-id="83c5c-736">Для включения функций расширения оболочки приложению не требуется дополнительная настройка или Настройка клиента.</span><span class="sxs-lookup"><span data-stu-id="83c5c-736">The application requires no additional setup or configuration on the client to enable the shell extension functionality.</span></span>

**<span data-ttu-id="83c5c-737">Требования для использования расширений оболочки:</span><span class="sxs-lookup"><span data-stu-id="83c5c-737">Requirements for using shell extensions:</span></span>**

-   <span data-ttu-id="83c5c-738">Пакеты, содержащие внедренные расширения оболочки, должны быть опубликованы глобально.</span><span class="sxs-lookup"><span data-stu-id="83c5c-738">Packages that contain embedded shell extensions must be published globally.</span></span>

-   <span data-ttu-id="83c5c-739">"Разрядность" приложения, секвенсора и клиента App-V должны совпадать, или расширения оболочки не работают.</span><span class="sxs-lookup"><span data-stu-id="83c5c-739">The “bitness” of the application, Sequencer, and App-V client must match, or the shell extensions won’t work.</span></span> <span data-ttu-id="83c5c-740">Пример</span><span class="sxs-lookup"><span data-stu-id="83c5c-740">For example:</span></span>

    -   <span data-ttu-id="83c5c-741">Версия приложения — 64-разр.</span><span class="sxs-lookup"><span data-stu-id="83c5c-741">The version of the application is 64-bit.</span></span>

    -   <span data-ttu-id="83c5c-742">Секвенсор выполняется на 64-разрядном компьютере.</span><span class="sxs-lookup"><span data-stu-id="83c5c-742">The Sequencer is running on a 64-bit computer.</span></span>

    -   <span data-ttu-id="83c5c-743">Пакет доставляется на клиентский компьютер App-V 64-bit.</span><span class="sxs-lookup"><span data-stu-id="83c5c-743">The package is being delivered to a 64-bit App-V client computer.</span></span>

<span data-ttu-id="83c5c-744">В следующей таблице показаны поддерживаемые расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-744">The following table displays the supported shell extensions.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-745">Обработчик</span><span class="sxs-lookup"><span data-stu-id="83c5c-745">Handler</span></span></th>
<th align="left"><span data-ttu-id="83c5c-746">Описание</span><span class="sxs-lookup"><span data-stu-id="83c5c-746">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-747">Обработчик контекстного меню</span><span class="sxs-lookup"><span data-stu-id="83c5c-747">Context menu handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-748">Добавляет элементы меню в контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="83c5c-748">Adds menu items to the context menu.</span></span> <span data-ttu-id="83c5c-749">Вызывается перед отображением контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="83c5c-749">It is called before the context menu is displayed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-750">Обработчик перетаскивания</span><span class="sxs-lookup"><span data-stu-id="83c5c-750">Drag-and-drop handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-751">Управление действием при щелчке правой кнопкой мыши и изменением появившегося контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="83c5c-751">Controls the action upon right-click drag-and-drop and modifies the context menu that appears.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-752">Целевой обработчик перетаскивания</span><span class="sxs-lookup"><span data-stu-id="83c5c-752">Drop target handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-753">Управляет действием после перетаскивания объекта данных и отбрасываниям по направлению, например к файлу.</span><span class="sxs-lookup"><span data-stu-id="83c5c-753">Controls the action after a data object is dragged-and-dropped over a drop target such as a file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-754">Обработчик объектов данных</span><span class="sxs-lookup"><span data-stu-id="83c5c-754">Data object handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-755">Управляет действием после того, как файл копируется в буфер обмена или перетаскивается и отбрасывается по направлению перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-755">Controls the action after a file is copied to the clipboard or dragged-and-dropped over a drop target.</span></span> <span data-ttu-id="83c5c-756">Он может предоставлять дополнительные форматы буфера обмена для целевого объекта перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="83c5c-756">It can provide additional clipboard formats to the drop target.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-757">Обработчик страницы свойств</span><span class="sxs-lookup"><span data-stu-id="83c5c-757">Property sheet handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-758">Заменяет или добавляет страницы в диалоговое окно "страница свойств" объекта.</span><span class="sxs-lookup"><span data-stu-id="83c5c-758">Replaces or adds pages to the property sheet dialog box of an object.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-759">Обработчик всплывающих подсказк</span><span class="sxs-lookup"><span data-stu-id="83c5c-759">Infotip handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-760">Позволяет получить сведения о флагах и всплывающих подсказках для элемента и отобразить его в всплывающей подсказке при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="83c5c-760">Allows retrieving flags and infotip information for an item and displaying it inside a popup tooltip upon mouse- hover.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-761">Обработчик столбцов</span><span class="sxs-lookup"><span data-stu-id="83c5c-761">Column handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-762">Позволяет создавать и отображать пользовательские столбцы в представлении "сведения" в проводнике Windows <em> </em> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-762">Allows creating and displaying custom columns in Windows Explorer <em>Details view</em>.</span></span> <span data-ttu-id="83c5c-763">Его можно использовать для расширенной сортировки и группировки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-763">It can be used to extend sorting and grouping.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-764">Обработчик просмотра</span><span class="sxs-lookup"><span data-stu-id="83c5c-764">Preview handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-765">Обеспечивает предварительный просмотр файла, который будет отображаться в области предварительного просмотра в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="83c5c-765">Enables a preview of a file to be displayed in the Windows Explorer Preview Pane.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="83c5c-766">НАДСТРОЙК</span><span class="sxs-lookup"><span data-stu-id="83c5c-766">COM</span></span>

<span data-ttu-id="83c5c-767">Клиент App-V поддерживает публикацию приложений с поддержкой интеграции и виртуализации COM.</span><span class="sxs-lookup"><span data-stu-id="83c5c-767">The App-V Client supports publishing applications with support for COM integration and virtualization.</span></span> <span data-ttu-id="83c5c-768">Интеграция COM позволяет клиенту App-V регистрировать COM-объекты в локальной операционной системе и виртуализации объектов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-768">COM integration allows the App-V Client to register COM objects on the local operating system and virtualization of the objects.</span></span> <span data-ttu-id="83c5c-769">Для целей этого документа интеграция COM-объектов требует дополнительных подробностей.</span><span class="sxs-lookup"><span data-stu-id="83c5c-769">For the purposes of this document, the integration of COM objects requires additional detail.</span></span>

<span data-ttu-id="83c5c-770">Приложение App-V поддерживает регистрацию COM-объектов из пакета в локальную операционную систему с двумя типами процессов: вне процесса и внутри процесса.</span><span class="sxs-lookup"><span data-stu-id="83c5c-770">App-V supports registering COM objects from the package to the local operating system with two process types: Out-of-process and in-process.</span></span> <span data-ttu-id="83c5c-771">Регистрация COM-объектов выполняется в одном или нескольких режимах работы для определенного пакета App-V, который включает в себя автономный, изолированный и интегрированный.</span><span class="sxs-lookup"><span data-stu-id="83c5c-771">Registering COM objects is accomplished with one or a combination of multiple modes of operation for a specific App-V package that includes off, Isolated, and Integrated.</span></span> <span data-ttu-id="83c5c-772">Интегрированный режим настраивается как для, так и для типа внутрипроцессного или внутрипроцессного.</span><span class="sxs-lookup"><span data-stu-id="83c5c-772">The integrated mode is configured for either the out-of-process or in-process type.</span></span> <span data-ttu-id="83c5c-773">Настройка режимов и типов COM осуществляется с помощью динамических файлов конфигурации (deploymentconfig.xml или userconfig.xml).</span><span class="sxs-lookup"><span data-stu-id="83c5c-773">Configuration of COM modes and types is accomplished with dynamic configuration files (deploymentconfig.xml or userconfig.xml).</span></span>

<span data-ttu-id="83c5c-774">Подробные сведения о интеграции App-V можно найти по адресу: <https://go.microsoft.com/fwlink/?LinkId=392834> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-774">Details on App-V integration are available at: <https://go.microsoft.com/fwlink/?LinkId=392834>.</span></span>

### <span data-ttu-id="83c5c-775">Клиенты программного обеспечения и возможности приложений</span><span class="sxs-lookup"><span data-stu-id="83c5c-775">Software clients and application capabilities</span></span>

<span data-ttu-id="83c5c-776">Приложение App-V поддерживает конкретные клиенты и точки расширения возможностей приложения, которые позволяют регистрировать виртуализированные приложения с помощью программного клиента операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-776">App-V supports specific software clients and application capabilities extension points that enable virtualized applications to be registered with the software client of the operating system.</span></span> <span data-ttu-id="83c5c-777">Это позволяет пользователям выбирать программы по умолчанию для таких операций, как электронная почта, Обмен мгновенными сообщениями и проигрыватель мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="83c5c-777">This enables users to select default programs for operations like email, instant messaging, and media player.</span></span> <span data-ttu-id="83c5c-778">Эта операция выполняется на панели управления с помощью настройки доступа к программам и параметров по умолчанию, а также при настройке последовательности в файлах манифеста или динамической конфигурации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-778">This operation is performed in the control panel with the Set Program Access and Computer Defaults, and configured during sequencing in the manifest or dynamic configuration files.</span></span> <span data-ttu-id="83c5c-779">Возможности приложения поддерживаются только в том случае, если приложения App-V публикуются глобально.</span><span class="sxs-lookup"><span data-stu-id="83c5c-779">Application capabilities are only supported when the App-V applications are published globally.</span></span>

<span data-ttu-id="83c5c-780">Пример регистрации клиента программного обеспечения для почтового клиента на базе App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-780">Example of software client registration of an App-V based mail client.</span></span>

```xml
    <SoftwareClients Enabled="true">
      <ClientConfiguration EmailEnabled="true" />
      <Extensions>
        <Extension Category="AppV.SoftwareClient">
          <SoftwareClients>
            <EMail MakeDefault="true">
              <Name>Mozilla Thunderbird</Name>
              <Description>Mozilla Thunderbird</Description>
              <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
              <InstallationInformation>
                <RegistrationCommands>
                  <Reinstall>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /SetAsDefaultAppGlobal</Reinstall>
                  <HideIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /HideShortcuts</HideIcons>
                  <ShowIcons>"[{ProgramFilesX86}]\Mozilla Thunderbird\uninstall\helper.exe" /ShowShortcuts</ShowIcons>
                </RegistrationCommands>
                <IconsVisible>1</IconsVisible>
                <OEMSettings />
              </InstallationInformation>
              <ShellCommands>
                <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -mail</Open>
              </ShellCommands>
              <MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>
              <MailToProtocol>
                <Description>Thunderbird URL</Description>
                <EditFlags>2</EditFlags>
                <DefaultIcon>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe,0</DefaultIcon>
                <ShellCommands>
                  <ApplicationId>[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe</ApplicationId>
                  <Open>"[{ProgramFilesX86}]\Mozilla Thunderbird\thunderbird.exe" -osint -compose "%1"</Open>
                </ShellCommands>
              </MailToProtocol>
            </EMail>
          </SoftwareClients>
        </Extension>
      </Extensions>
    </SoftwareClients>
```

<span data-ttu-id="83c5c-781">**Примечание**  В этом примере:</span><span class="sxs-lookup"><span data-stu-id="83c5c-781">**Note** In this example:</span></span>

-   `<ClientConfiguration EmailEnabled="true" />` <span data-ttu-id="83c5c-782">— Это общая настройка клиентов по электронной почте для интеграции с клиентами.</span><span class="sxs-lookup"><span data-stu-id="83c5c-782">is the overall Software Clients setting to integrate Email clients</span></span>

-   `<EMail MakeDefault="true">` <span data-ttu-id="83c5c-783">флаг для настройки определенного почтового клиента в качестве почтового клиента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="83c5c-783">is the flag to set a particular Email client as the default Email client</span></span>

-   `<MAPILibrary>[{ProgramFilesX86}]\Mozilla Thunderbird\mozMapi32_InUse.dll</MAPILibrary>` <span data-ttu-id="83c5c-784">— это регистрация библиотеки MAPI</span><span class="sxs-lookup"><span data-stu-id="83c5c-784">is the MAPI dll registration</span></span>

 

### <span data-ttu-id="83c5c-785">Обработчик протокола URL-адреса</span><span class="sxs-lookup"><span data-stu-id="83c5c-785">URL Protocol handler</span></span>

<span data-ttu-id="83c5c-786">Приложения не всегда называются виртуализированными приложениями, использующих вызов типов файлов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-786">Applications do not always specifically called virtualized applications utilizing file type invocation.</span></span> <span data-ttu-id="83c5c-787">Например, в приложении, которое поддерживает внедрение ссылки mailto: в документ или веб-страницу, пользователь щелкает ссылку mailto:, и ожидается получение зарегистрированного почтового клиента.</span><span class="sxs-lookup"><span data-stu-id="83c5c-787">For, example, in an application that supports embedding a mailto: link inside a document or web page, the user clicks on a mailto: link and expects to get their registered mail client.</span></span> <span data-ttu-id="83c5c-788">App-V поддерживает обработчики протоколов URL-адресов, которые могут быть зарегистрированы для каждого пакета с помощью локальной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-788">App-V supports URL Protocol handlers that can be registered on a per-package basis with the local operating system.</span></span> <span data-ttu-id="83c5c-789">Во время последовательности обработчики протокола URL-адреса автоматически добавляются в пакет.</span><span class="sxs-lookup"><span data-stu-id="83c5c-789">During sequencing, the URL protocol handlers are automatically added to the package.</span></span>

<span data-ttu-id="83c5c-790">В ситуациях, когда имеется более одного приложения, которое может зарегистрировать конкретный обработчик протокола URL-адреса, можно использовать динамические файлы конфигурации для изменения поведения и подавления или отключения этой функции для приложения, которое не должно быть запущено основным приложением.</span><span class="sxs-lookup"><span data-stu-id="83c5c-790">For situations where there is more than one application that could register the specific URL Protocol handler, the dynamic configuration files can be utilized to modify the behavior and suppress or disable this feature for an application that should not be the primary application launched.</span></span>

### <span data-ttu-id="83c5c-791">AppPath</span><span class="sxs-lookup"><span data-stu-id="83c5c-791">AppPath</span></span>

<span data-ttu-id="83c5c-792">Точка расширения AppPath поддерживает вызов приложений App-V непосредственно из операционной системы.</span><span class="sxs-lookup"><span data-stu-id="83c5c-792">The AppPath extension point supports calling App-V applications directly from the operating system.</span></span> <span data-ttu-id="83c5c-793">Обычно это выполняется с экрана запуска или запуска, в зависимости от операционной системы, которая позволяет администраторам предоставлять доступ к приложениям App-V из команд или сценариев операционной системы, не вызывая определенный путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="83c5c-793">This is typically accomplished from the Run or Start Screen, depending on the operating system, which enables administrators to provide access to App-V applications from operating system commands or scripts without calling the specific path to the executable.</span></span> <span data-ttu-id="83c5c-794">Таким образом, вы не изменяете переменную среды системного пути во всех системах, так как она выполняется во время публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-794">It therefore avoids modifying the system path environment variable on all systems, as it is accomplished during publishing.</span></span>

<span data-ttu-id="83c5c-795">Точка расширения AppPath настраивается либо в манифесте, либо в файлах динамической конфигурации и хранится в реестре на локальном компьютере во время публикации для пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-795">The AppPath extension point is configured either in the manifest or in the dynamic configuration files and is stored in the registry on the local machine during publishing for the user.</span></span> <span data-ttu-id="83c5c-796">Дополнительные сведения о AppPath рецензировании: <https://go.microsoft.com/fwlink/?LinkId=392835> .</span><span class="sxs-lookup"><span data-stu-id="83c5c-796">For additional information on AppPath review: <https://go.microsoft.com/fwlink/?LinkId=392835>.</span></span>

### <span data-ttu-id="83c5c-797">Виртуальное приложение</span><span class="sxs-lookup"><span data-stu-id="83c5c-797">Virtual application</span></span>

<span data-ttu-id="83c5c-798">Эта подсистема предоставляет список приложений, собранных в процессе упорядочивания, который обычно используется другими компонентами App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-798">This subsystem provides a list of applications captured during sequencing which is usually consumed by other App-V components.</span></span> <span data-ttu-id="83c5c-799">Интеграция точек расширения, принадлежащих определенному приложению, может быть отключена с помощью динамических файлов конфигурации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-799">Integration of extension points belonging to a particular application can be disabled using dynamic configuration files.</span></span> <span data-ttu-id="83c5c-800">Например, если пакет содержит два приложения, можно отключить все точки расширения, принадлежащие одному приложению, чтобы разрешить только интеграцию точек расширения другого приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-800">For example, if a package contains two applications, it is possible to disable all extension points belonging to one application, in order to allow only integration of extension points of other application.</span></span>

### <span data-ttu-id="83c5c-801">Правила точки расширения</span><span class="sxs-lookup"><span data-stu-id="83c5c-801">Extension point rules</span></span>

<span data-ttu-id="83c5c-802">Описанные выше точки расширения интегрированы в операционную систему в зависимости от того, как были опубликованы пакеты.</span><span class="sxs-lookup"><span data-stu-id="83c5c-802">The extension points described above are integrated into the operating system based on how the packages has been published.</span></span> <span data-ttu-id="83c5c-803">В общедоступных местах публикации, где пользователи публикуют точки расширения в расположениях пользователей, размести расширения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-803">Global publishing places extension points in public machine locations, where user publishing places extension points in user locations.</span></span> <span data-ttu-id="83c5c-804">Например, ярлык, созданный на рабочем столе и опубликованный глобально, приведет к созданию данных файла для ярлыка (%Public%\\Desktop) и данных реестра (HKLM\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="83c5c-804">For example a shortcut that is created on the desktop and published globally will result in the file data for the shortcut (%Public%\\Desktop) and the registry data (HKLM\\Software\\Classes).</span></span> <span data-ttu-id="83c5c-805">Один и тот же ярлык может иметь данные файла (%UserProfile%\\Desktop) и данные реестра (HKCU\\Software\\Classes).</span><span class="sxs-lookup"><span data-stu-id="83c5c-805">The same shortcut would have file data (%UserProfile%\\Desktop) and registry data (HKCU\\Software\\Classes).</span></span>

<span data-ttu-id="83c5c-806">Точки расширения не публикуются так же, как и для некоторых точек расширения требуется глобальная публикация, а для некоторых из них требуется последовательность для конкретной операционной системы и архитектуры, где они были доставлены.</span><span class="sxs-lookup"><span data-stu-id="83c5c-806">Extension points are not all published the same way, where some extension points will require global publishing and others require sequencing on the specific operating system and architecture where they are delivered.</span></span> <span data-ttu-id="83c5c-807">Ниже приведена таблица, в которой описаны эти два ключевых правила.</span><span class="sxs-lookup"><span data-stu-id="83c5c-807">Below is a table that describes these two key rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="83c5c-808">Виртуальное расширение</span><span class="sxs-lookup"><span data-stu-id="83c5c-808">Virtual Extension</span></span></th>
<th align="left"><span data-ttu-id="83c5c-809">Требуется упорядочение целевой операционной системы</span><span class="sxs-lookup"><span data-stu-id="83c5c-809">Requires target OS Sequencing</span></span></th>
<th align="left"><span data-ttu-id="83c5c-810">Требуется глобальная публикация</span><span class="sxs-lookup"><span data-stu-id="83c5c-810">Requires Global Publishing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-811">Появивше</span><span class="sxs-lookup"><span data-stu-id="83c5c-811">Shortcut</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-812">Сопоставление типов файлов</span><span class="sxs-lookup"><span data-stu-id="83c5c-812">File Type Association</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-813">Протоколы URL-адресов</span><span class="sxs-lookup"><span data-stu-id="83c5c-813">URL Protocols</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-814">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-814">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-815">AppPaths</span><span class="sxs-lookup"><span data-stu-id="83c5c-815">AppPaths</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-816">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-816">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-817">Режим COM</span><span class="sxs-lookup"><span data-stu-id="83c5c-817">COM Mode</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-818">Клиент программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="83c5c-818">Software Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-819">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-819">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-820">Возможности приложения</span><span class="sxs-lookup"><span data-stu-id="83c5c-820">Application Capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-821">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-821">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-822">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-822">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-823">Обработчик контекстного меню</span><span class="sxs-lookup"><span data-stu-id="83c5c-823">Context Menu Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-824">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-824">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-825">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-825">X</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-826">Обработчик перетаскивания</span><span class="sxs-lookup"><span data-stu-id="83c5c-826">Drag-and-drop Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-827">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-827">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-828">Обработчик объектов данных</span><span class="sxs-lookup"><span data-stu-id="83c5c-828">Data Object Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-829">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-829">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-830">Обработчик страницы свойств</span><span class="sxs-lookup"><span data-stu-id="83c5c-830">Property Sheet Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-831">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-831">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-832">Обработчик всплывающих подсказк</span><span class="sxs-lookup"><span data-stu-id="83c5c-832">Infotip Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-833">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-833">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-834">Обработчик столбцов</span><span class="sxs-lookup"><span data-stu-id="83c5c-834">Column Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-835">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-835">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-836">Расширения оболочки</span><span class="sxs-lookup"><span data-stu-id="83c5c-836">Shell Extensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-837">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-837">X</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="83c5c-838">Вспомогательный объект браузера</span><span class="sxs-lookup"><span data-stu-id="83c5c-838">Browser Helper Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-839">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-839">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-840">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-840">X</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="83c5c-841">Объект Active X</span><span class="sxs-lookup"><span data-stu-id="83c5c-841">Active X Object</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-842">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-842">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="83c5c-843">X</span><span class="sxs-lookup"><span data-stu-id="83c5c-843">X</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-dynamic-config"></a><span data-ttu-id="83c5c-844">Динамическая обработка конфигурации</span><span class="sxs-lookup"><span data-stu-id="83c5c-844">Dynamic configuration processing</span></span>


<span data-ttu-id="83c5c-845">Развертывание пакетов App-V на одном компьютере или в пользовательском интерфейсе очень просто.</span><span class="sxs-lookup"><span data-stu-id="83c5c-845">Deploying App-V packages to one machine or user is very simple.</span></span> <span data-ttu-id="83c5c-846">Тем не менее, поскольку организации развертывают приложения AppV для бизнес-строк и географических и геограниц, возможность одновременных последовательностей приложения с одним набором параметров становится невозможной.</span><span class="sxs-lookup"><span data-stu-id="83c5c-846">However, as organizations deploy AppV applications across business lines and geographic and political boundaries, the ability to sequence an application one time with one set of settings becomes impossible.</span></span> <span data-ttu-id="83c5c-847">Приложение App-V было спроектировано для этого сценария, так как оно собирает определенные параметры и конфигурации во время последовательности в файле манифеста, но также поддерживает изменение с динамическими файлами конфигурации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-847">App-V was designed for this scenario, as it captures specific settings and configurations during sequencing in the Manifest file, but also supports modification with Dynamic Configuration files.</span></span>

<span data-ttu-id="83c5c-848">Динамическая настройка App-V позволяет указать политику для пакета либо на уровне компьютера, либо на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="83c5c-848">App-V dynamic configuration allows for specifying a policy for a package either at the machine level or at the user level.</span></span> <span data-ttu-id="83c5c-849">Динамические файлы конфигурации позволяют инженерам-последовательностью изменить конфигурацию пакета, после последовательной последовательности, чтобы удовлетворить потребности отдельных групп пользователей или компьютеров.</span><span class="sxs-lookup"><span data-stu-id="83c5c-849">The Dynamic Configuration files enable sequencing engineers to modify the configuration of a package, post-sequencing, to address the needs of individual groups of users or machines.</span></span> <span data-ttu-id="83c5c-850">В некоторых случаях может потребоваться внесение изменений в приложение для обеспечения надлежащей работы в среде App-V.</span><span class="sxs-lookup"><span data-stu-id="83c5c-850">In some instances it may be necessary to make modifications to the application to provide proper functionality within the App-V environment.</span></span> <span data-ttu-id="83c5c-851">Например, может потребоваться внесение изменений в файлы \ _ \ \* config.xml, чтобы выполнить определенные действия в определенный момент во время выполнения приложения, например отключение расширения mailto, чтобы предотвратить перезапись расширения приложением из другого приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-851">For example, it may be necessary to make modifications to the \_\*config.xml files to allow certain actions to be performed at a specified time during the execution of the application, like disabling a mailto extension to prevent a virtualized application from overwriting that extension from another application.</span></span>

<span data-ttu-id="83c5c-852">Пакеты App-V содержат файл манифеста в файле пакета AppV, который является представителем последовательностей операций и является политикой выбора, если не назначены динамические файлы конфигурации определенному пакету.</span><span class="sxs-lookup"><span data-stu-id="83c5c-852">App-V Packages contain the Manifest file inside of the appv package file, which is representative of sequencing operations and is the policy of choice unless Dynamic Configuration files are assigned to a specific package.</span></span> <span data-ttu-id="83c5c-853">После последовательной последовательности файлов динамические файлы конфигурации можно изменить, чтобы разрешить публикацию приложения на разных компьютерах или пользователей с разными точками расширения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-853">Post-sequencing, the Dynamic Configuration files can be modified to allow the publishing of an application to different desktops or users with different extension points.</span></span> <span data-ttu-id="83c5c-854">Два динамических файла конфигурации — это динамические конфигурации развертывания (DDC) и динамические файлы конфигурации (DUC).</span><span class="sxs-lookup"><span data-stu-id="83c5c-854">The two Dynamic Configuration Files are the Dynamic Deployment Configuration (DDC) and Dynamic User Configuration (DUC) files.</span></span> <span data-ttu-id="83c5c-855">В этом разделе рассказывается о сочетаниях файлов манифеста и динамической конфигурации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-855">This section focuses on the combination of the manifest and dynamic configuration files.</span></span>

### <span data-ttu-id="83c5c-856">Пример для динамических файлов конфигурации</span><span class="sxs-lookup"><span data-stu-id="83c5c-856">Example for dynamic configuration files</span></span>

<span data-ttu-id="83c5c-857">В примере ниже показано сочетание манифеста, конфигурации развертывания и файлов конфигурации пользователя после публикации и выполнения обычной операции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-857">The example below shows the combination of the Manifest, Deployment Configuration and User Configuration files after publishing and during normal operation.</span></span> <span data-ttu-id="83c5c-858">Эти примеры являются сокращенными примерами каждого из файлов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-858">These examples are abbreviated examples of each of the files.</span></span> <span data-ttu-id="83c5c-859">Цель — это отображение только сочетаний файлов, а не полного описания конкретных категорий, доступных в каждом из файлов.</span><span class="sxs-lookup"><span data-stu-id="83c5c-859">The purpose is show the combination of the files only and not to be a complete description of the specific categories available in each of the files.</span></span> <span data-ttu-id="83c5c-860">Для получения дополнительной информации ознакомьтесь с руководством по виртуализации App-V 5 по адресу:</span><span class="sxs-lookup"><span data-stu-id="83c5c-860">For more information review the App-V 5 Sequencing Guide at:</span></span> <https://go.microsoft.com/fwlink/?LinkID=269810>

**<span data-ttu-id="83c5c-861">Является</span><span class="sxs-lookup"><span data-stu-id="83c5c-861">Manifest</span></span>**

```xml
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
```

**<span data-ttu-id="83c5c-862">Конфигурация развертывания</span><span class="sxs-lookup"><span data-stu-id="83c5c-862">Deployment Configuration</span></span>**

```xml
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path= "\REGISTRY\Machine\Software\7zip">
                    <Value Type="REG_SZ" Name="Config" Data="1234"/>
                    </Key>
               </Include>
          </Registry>
     </Subsystems>
```

**<span data-ttu-id="83c5c-863">Конфигурация пользователя</span><span class="sxs-lookup"><span data-stu-id="83c5c-863">User Configuration</span></span>**

```xml
<UserConfiguration>
     <Subsystems>
<appv:ExtensionCategory="AppV.Shortcut">
     <appv:Shortcut>
          <appv:File>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM exe.O.ico</appv:Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<UserConfiguration>
     <Subsystems>
<appv:Extension Category="AppV.Shortcut">
     <appv:Shortcut>
          <appv:Fìle>[{Desktop}]\7-Zip\7-Zip File Manager.lnk</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot}]\7zFM.exe.O.ico</appv:Icon>
     </appv:Shortcut>
     <appv:Shortcut>
          <appv:File>[{Common Programs}]\7-Zip\7-Zip File Manager.Ink</appv:File>
          <appv:Target>[{AppVPackageRoot}]\7zFM.exe</appv:Target>
          <appv:Icon>[{AppVPackageRoot)]\7zFM.exe.O.ico</appv: Icon>
     </appv:Shortcut>
</appv:Extension>
     </Subsystems>
<MachineConfiguration>
     <Subsystems>
          <Registry>
               <Include>
                    <Key Path="\REGISTRY\Machine\Software\7zip">
                    <Value Type=”REG_SZ" Name="Config" Data="1234"/>
               </Include>
          </Registry>
     </Subsystems>
```

## <a href="" id="bkmk-sidebyside-assemblies"></a><span data-ttu-id="83c5c-864">Параллельные сборки</span><span class="sxs-lookup"><span data-stu-id="83c5c-864">Side-by-side assemblies</span></span>


<span data-ttu-id="83c5c-865">Приложение App-V поддерживает автоматическую упаковку параллельных сборок (SxS) во время виртуализации и развертывания на клиенте во время публикации виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="83c5c-865">App-V supports the automatic packaging of side-by-side (SxS) assemblies during sequencing and deployment on the client during virtual application publishing.</span></span> <span data-ttu-id="83c5c-866">App-V 5 SP2 поддерживает сбор сборок SxS во время виртуализации для сборок, отсутствующих на компьютере, на котором установлена последовательность.</span><span class="sxs-lookup"><span data-stu-id="83c5c-866">App-V 5 SP2 supports capturing SxS assemblies during sequencing for assemblies not present on the sequencing machine.</span></span> <span data-ttu-id="83c5c-867">И для сборок, состоящих из Visual C++ (версии 8 и более поздней) и во время выполнения MSXML, программа Sequencer автоматически обнаружит и захватит эти зависимости, даже если они не были установлены во время наблюдения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-867">And for assemblies consisting of Visual C++ (Version 8 and newer) and/or MSXML run-time, the Sequencer will automatically detect and capture these dependencies even if they were not installed during monitoring.</span></span> <span data-ttu-id="83c5c-868">Функция "параллельные сборки" удаляет ограничения для предыдущих версий App-V, где приложение App-V Sequencer не захватывает сборки, уже присутствующие на рабочей станции, и privatizing сборки, для каждой из которых установлен ограниченный одноразрядный номер версии.</span><span class="sxs-lookup"><span data-stu-id="83c5c-868">The Side by Side assemblies feature removes the limitations of previous versions of App-V, where the App-V Sequencer did not capture assemblies already present on the sequencing workstation, and privatizing the assemblies which limited to one bit version per package.</span></span> <span data-ttu-id="83c5c-869">Это поведение привело к развернутым приложениям App-V для клиентов, у которых нет требуемых сборок SxS, что приводит к сбою при запуске приложения.</span><span class="sxs-lookup"><span data-stu-id="83c5c-869">This behavior resulted in deployed App-V applications to clients missing the required SxS assemblies, causing application launch failures.</span></span> <span data-ttu-id="83c5c-870">Таким образом, процесс упаковки будет применен к документу, а затем убедиться, что все сборки, необходимые для пакетов, были локально установлены в клиентской операционной системе пользователя, чтобы обеспечить поддержку виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="83c5c-870">This forced the packaging process to document and then ensure that all assemblies required for packages were locally installed on the user’s client operating system to ensure support for the virtual applications.</span></span> <span data-ttu-id="83c5c-871">На основе числа сборок и нехватки документации приложения для необходимых зависимостей эта задача была как задачей для управления, так и ее реализации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-871">Based on the number of assemblies and the lack of application documentation for the required dependencies, this task was both a management and implementation challenge.</span></span>

<span data-ttu-id="83c5c-872">Поддержка параллельных сборок в App-V имеет перечисленные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="83c5c-872">Side by Side Assembly support in App-V has the following features.</span></span>

-   <span data-ttu-id="83c5c-873">Автоматическое создание сборок SxS во время последовательности, независимо от того, была ли сборка уже установлена на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="83c5c-873">Automatic captures of SxS assembly during Sequencing, regardless of whether the assembly was already installed on the sequencing workstation.</span></span>

-   <span data-ttu-id="83c5c-874">Клиент App-V автоматически устанавливает на клиентский компьютер необходимые сборки SxS на момент публикации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-874">The App-V Client automatically installs required SxS assemblies to the client computer at publishing time when they are not present.</span></span>

-   <span data-ttu-id="83c5c-875">Секвенсор возвращает зависимость VC-времени выполнения в механизме составления отчетов секвенсора.</span><span class="sxs-lookup"><span data-stu-id="83c5c-875">The Sequencer reports the VC run-time dependency in Sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="83c5c-876">Секвенсор позволяет не упаковывать сборки, которые уже установлены в секвенсор, и поддерживать сценарии, в которых сборки ранее были установлены на целевые компьютеры.</span><span class="sxs-lookup"><span data-stu-id="83c5c-876">The Sequencer allows opting to not package the assemblies that are already installed on the Sequencer, supporting scenarios where the assemblies have previously been installed on the target computers.</span></span>

### <span data-ttu-id="83c5c-877">Автоматическая публикация сборок SxS</span><span class="sxs-lookup"><span data-stu-id="83c5c-877">Automatic publishing of SxS assemblies</span></span>

<span data-ttu-id="83c5c-878">При публикации пакета App-V с сборками SxS клиент App-V будет проверять наличие сборки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="83c5c-878">During publishing of an App-V package with SxS assemblies the App-V Client will check for the presence of the assembly on the machine.</span></span> <span data-ttu-id="83c5c-879">Если сборка не существует, клиент развернет сборку на компьютере.</span><span class="sxs-lookup"><span data-stu-id="83c5c-879">If the assembly does not exist, the client will deploy the assembly to the machine.</span></span> <span data-ttu-id="83c5c-880">Пакеты, которые являются частью групп соединения, будут основываться на параллельных сборках сборок, которые являются частью основных пакетов, так как группа подключений не содержит сведений об установке сборки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-880">Packages that are part of connection groups will rely on the Side by Side assembly installations that are part of the base packages, as the connection group does not contain any information about assembly installation.</span></span>

<span data-ttu-id="83c5c-881">**Примечание**  Отмена публикации или удаление пакета с помощью сборки не приводит к удалению сборок для этого пакета.</span><span class="sxs-lookup"><span data-stu-id="83c5c-881">**Note** UnPublishing or removing a package with an assembly does not remove the assemblies for that package.</span></span>

 

## <a href="" id="bkmk-client-logging"></a><span data-ttu-id="83c5c-882">Ведение журнала на стороне клиента</span><span class="sxs-lookup"><span data-stu-id="83c5c-882">Client logging</span></span>


<span data-ttu-id="83c5c-883">Клиент App-V заносит данные в журнал событий Windows в стандартном формате ETW.</span><span class="sxs-lookup"><span data-stu-id="83c5c-883">The App-V client logs information to the Windows Event log in standard ETW format.</span></span> <span data-ttu-id="83c5c-884">Определенные события App-V можно найти в средстве просмотра событий в разделе приложения и службы Logs\\Microsoft\\AppV\\Client.</span><span class="sxs-lookup"><span data-stu-id="83c5c-884">The specific App-V events can be found in the event viewer, under Applications and Services Logs\\Microsoft\\AppV\\Client.</span></span>

<span data-ttu-id="83c5c-885">**Примечание**  В приложении App-V 5,0 с пакетом обновления 3 (SP3) некоторые журналы были объединены и перемещены в следующее расположение:</span><span class="sxs-lookup"><span data-stu-id="83c5c-885">**Note** In App-V 5.0 SP3, some logs have been consolidated and moved to the following location:</span></span>

`Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog`

<span data-ttu-id="83c5c-886">Список перемещенных журналов можно найти в разделе [о приложении App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span><span class="sxs-lookup"><span data-stu-id="83c5c-886">For a list of the moved logs, see [About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</span></span>

 

<span data-ttu-id="83c5c-887">Ниже описаны три определенные категории событий.</span><span class="sxs-lookup"><span data-stu-id="83c5c-887">There are three specific categories of events recorded described below.</span></span>

<span data-ttu-id="83c5c-888">**Администратор**: регистрирует события для конфигураций, которые применяются к клиенту App-V и содержат основные предупреждения и ошибки.</span><span class="sxs-lookup"><span data-stu-id="83c5c-888">**Admin**: Logs events for configurations being applied to the App-V Client, and contains the primary warnings and errors.</span></span>

<span data-ttu-id="83c5c-889">**Эксплуатация**: заносит в журнал общее выполнение App-v и использование отдельных компонентов, создавая журнал аудита операций App-v, выполненных в клиенте App-v.</span><span class="sxs-lookup"><span data-stu-id="83c5c-889">**Operational**: Logs the general App-V execution and usage of individual components creating an audit log of the App-V operations that have been completed on the App-V Client.</span></span>

<span data-ttu-id="83c5c-890">**Виртуальное приложение**: журналы записываются виртуальным приложением для запуска и использования подсистем виртуализации.</span><span class="sxs-lookup"><span data-stu-id="83c5c-890">**Virtual Application**: Logs virtual application launches and use of virtualization subsystems.</span></span>






 

 





