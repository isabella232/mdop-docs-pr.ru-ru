---
title: Справочник по схемам шаблонов приложений для UE-V 2. x
description: Справочник по схемам шаблонов приложений для UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827409"
---
# <span data-ttu-id="95516-103">Справочник по схемам шаблонов приложений для UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="95516-103">Application Template Schema Reference for UE-V 2.x</span></span>


<span data-ttu-id="95516-104">Виртуализация взаимодействия с пользователем Microsoft (UE-V) 2,0, 2,1 и 2,1 SP1 используют шаблоны расположения XML-параметров для определения параметров классического приложения, а также параметров Windows, которые регистрируются и применяются с UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-104">Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 use XML settings location templates to define the desktop application settings and Windows settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="95516-105">UE-V включает набор шаблонов расположения параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="95516-105">UE-V includes a set of default settings location templates.</span></span> <span data-ttu-id="95516-106">Вы также можете создавать шаблоны расположений с пользовательскими параметрами с помощью генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-106">You can also create custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="95516-107">Опытный пользователь может настроить XML-файл для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-107">An advanced user can customize the XML file for a settings location template.</span></span> <span data-ttu-id="95516-108">В этой статье описана структура XML для шаблонов расположения параметров UE-V 2,1 (SP1) и 2,0, а также инструкции по изменению этих файлов.</span><span class="sxs-lookup"><span data-stu-id="95516-108">This topic details the XML structure of the UE-V 2.1 (SP1) and 2.0 settings location templates and provides guidance for editing these files.</span></span>

## <span data-ttu-id="95516-109">Справочник по схеме шаблонов приложений для UE-V 2,1 и 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="95516-109">UE-V 2.1 and 2.1 SP1 Application Template Schema Reference</span></span>


<span data-ttu-id="95516-110">В этом разделе подробно описана структура XML для шаблона расположения параметров UE-V 2,1 и 2,1 SP1 и приведены инструкции по изменению этого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-110">This section details the XML structure of the UE-V 2.1 and 2.1 SP1 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="95516-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="95516-111">In This Section</span></span>

-   [<span data-ttu-id="95516-112">Объявление XML и атрибут кодировки</span><span class="sxs-lookup"><span data-stu-id="95516-112">XML Declaration and Encoding Attribute</span></span>](#xml21)

-   [<span data-ttu-id="95516-113">Пространство имен и корневой элемент</span><span class="sxs-lookup"><span data-stu-id="95516-113">Namespace and Root Element</span></span>](#namespace21)

-   [<span data-ttu-id="95516-114">Типы данных</span><span class="sxs-lookup"><span data-stu-id="95516-114">Data types</span></span>](#data21)

-   [<span data-ttu-id="95516-115">Элемент Name</span><span class="sxs-lookup"><span data-stu-id="95516-115">Name Element</span></span>](#name21)

-   [<span data-ttu-id="95516-116">Элемент ID</span><span class="sxs-lookup"><span data-stu-id="95516-116">ID Element</span></span>](#id21)

-   [<span data-ttu-id="95516-117">Элемент Version</span><span class="sxs-lookup"><span data-stu-id="95516-117">Version Element</span></span>](#version21)

-   [<span data-ttu-id="95516-118">Элемент Author</span><span class="sxs-lookup"><span data-stu-id="95516-118">Author Element</span></span>](#author21)

-   [<span data-ttu-id="95516-119">Обработка и обработка элементов</span><span class="sxs-lookup"><span data-stu-id="95516-119">Processes and Process Element</span></span>](#processes21)

-   [<span data-ttu-id="95516-120">Элемент приложения</span><span class="sxs-lookup"><span data-stu-id="95516-120">Application Element</span></span>](#application21)

-   [<span data-ttu-id="95516-121">Общий элемент</span><span class="sxs-lookup"><span data-stu-id="95516-121">Common Element</span></span>](#common21)

-   [<span data-ttu-id="95516-122">Элемент SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="95516-122">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate21)

-   [<span data-ttu-id="95516-123">Приложение: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="95516-123">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix21)

### <a href="" id="xml21"></a><span data-ttu-id="95516-124">Объявление XML и атрибут кодировки</span><span class="sxs-lookup"><span data-stu-id="95516-124">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="95516-125">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-125">Mandatory: True</span></span>**

**<span data-ttu-id="95516-126">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-126">Type: String</span></span>**

<span data-ttu-id="95516-127">В XML-объявлении должен быть указан атрибут версии 1,0 ( &lt; ? XML Version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="95516-127">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="95516-128">Шаблоны местоположения параметров, созданные генератором UE-V, сохраняются в кодировке UTF-8, хотя кодировка явно не указана.</span><span class="sxs-lookup"><span data-stu-id="95516-128">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="95516-129">Рекомендуется включить в этот элемент атрибут Encoding = "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="95516-129">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="95516-130">Все шаблоны, включенные в продукт, задают этот тег (вы также увидите документы в%ProgramFiles%\\Microsoft взаимодействия с пользователем Virtualization\\Templates для справки).</span><span class="sxs-lookup"><span data-stu-id="95516-130">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="95516-131">Пример</span><span class="sxs-lookup"><span data-stu-id="95516-131">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a><span data-ttu-id="95516-132">Пространство имен и корневой элемент</span><span class="sxs-lookup"><span data-stu-id="95516-132">Namespace and Root Element</span></span>

**<span data-ttu-id="95516-133">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-133">Mandatory: True</span></span>**

**<span data-ttu-id="95516-134">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-134">Type: String</span></span>**

<span data-ttu-id="95516-135">UE-V использует https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate пространство имен для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-135">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="95516-136">SettingsLocationTemplate является корневым элементом и содержит все остальные элементы.</span><span class="sxs-lookup"><span data-stu-id="95516-136">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="95516-137">Ссылка на SettingsLocationTemplate во всех шаблонах, использующих этот тег:</span><span class="sxs-lookup"><span data-stu-id="95516-137">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a><span data-ttu-id="95516-138">Типы данных</span><span class="sxs-lookup"><span data-stu-id="95516-138">Data types</span></span>

<span data-ttu-id="95516-139">Это типы данных для схемы шаблонов приложений UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-139">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="95516-140">**Идентификатор GUID** GUID описывает стандартное выражение глобального уникального идентификатора в форме "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\" [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a – ОС – F0-9 \] {12} \ \} ".</span><span class="sxs-lookup"><span data-stu-id="95516-140">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="95516-141">Используется в элементе Filesetting\\Root\\KnownFolder для проверки форматирования известных папок.</span><span class="sxs-lookup"><span data-stu-id="95516-141">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="95516-142">**FilenameString** FilenameString — имя файла отслеживаемого процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-142">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="95516-143">Его значения ограничены регулярным выражением \ [^ \ \ \ \ \ \ \ \ \ \ \ \ | &lt; &gt; /: \] + (это означает, что они не содержат знаков обратной косой черты, знака звездочки или символа подстановки с вопросительным знаком, символа вертикальной черты, знака "больше или меньше", знаков после запятой или двоеточия).</span><span class="sxs-lookup"><span data-stu-id="95516-143">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="95516-144">**IDString** IDString относится к значению идентификатора элементов приложения, SettingsLocationTemplate и часто используемых элементов (используется для описания наборов приложений с общими параметрами).</span><span class="sxs-lookup"><span data-stu-id="95516-144">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="95516-145">Оно ограничено тем же регулярным выражением, что и FilenameString (\ [^ &lt; &gt; ] /:\]+).</span><span class="sxs-lookup"><span data-stu-id="95516-145">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="95516-146">**TemplateVersion** TemplateVersion — это целочисленное значение, используемое для описания редакции шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-146">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="95516-147">Его значение может находиться в диапазоне от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="95516-147">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="95516-148">**Пустой** Пустой объект ссылается на пустое значение.</span><span class="sxs-lookup"><span data-stu-id="95516-148">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="95516-149">Используется в Process\\ShellProcess, чтобы указать, что отсутствует процесс для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="95516-149">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="95516-150">Это значение не следует использовать ни в каких шаблонах приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-150">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="95516-151">**Автор** Тип данных Author — это сложный тип, который определяет автора шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-151">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="95516-152">Он состоит из двух дочерних элементов: **имя** и **адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="95516-152">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="95516-153">В типе данных Author элемент name является обязательным, а элемент электронной почты — необязательным.</span><span class="sxs-lookup"><span data-stu-id="95516-153">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="95516-154">Этот тип подробно описан в элементе SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="95516-154">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="95516-155">**Range (диапазон** ) Диапазон. определяет целочисленный класс, состоящий из двух дочерних элементов: **минимума** и **максимума**.</span><span class="sxs-lookup"><span data-stu-id="95516-155">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="95516-156">Этот тип данных реализован в типе данных ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-156">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="95516-157">Если задано значение, должно быть включено как минимальное, так и максимальное значения.</span><span class="sxs-lookup"><span data-stu-id="95516-157">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="95516-158">**ProcessVersion** ProcessVersion определяет тип с четырьмя дочерними элементами: **основными**, **дополнительными**, **сборками**и **исправлениями**.</span><span class="sxs-lookup"><span data-stu-id="95516-158">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="95516-159">Этот тип данных используется элементом Process для заполнения его значений ProductVersion и FileVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-159">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="95516-160">Данными для этого типа является значение Range.</span><span class="sxs-lookup"><span data-stu-id="95516-160">The data for this type is a Range value.</span></span> <span data-ttu-id="95516-161">Основной дочерний элемент является обязательным, а остальные являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="95516-161">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="95516-162">**Архитектура** Архитектура перечисляет два возможных значения: **Win32** и **Win64**.</span><span class="sxs-lookup"><span data-stu-id="95516-162">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="95516-163">Эти значения используются для определения архитектуры процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-163">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="95516-164">**Процесс** Тип данных «процесс» — это контейнер, используемый для описания процессов, которые необходимо отслеживать с помощью UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-164">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="95516-165">Он состоит из шести дочерних элементов: **имя файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="95516-165">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="95516-166">В этой таблице подробно описываются соответствующие типы данных каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="95516-166">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95516-167">Элемент</span><span class="sxs-lookup"><span data-stu-id="95516-167">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95516-168">Тип данных</span><span class="sxs-lookup"><span data-stu-id="95516-168">Data Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95516-169">Обязательное</span><span class="sxs-lookup"><span data-stu-id="95516-169">Mandatory</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-170">Файла</span><span class="sxs-lookup"><span data-stu-id="95516-170">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-171">FilenameString</span><span class="sxs-lookup"><span data-stu-id="95516-171">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-172">True</span><span class="sxs-lookup"><span data-stu-id="95516-172">True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-173">Архитектура</span><span class="sxs-lookup"><span data-stu-id="95516-173">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-174">Архитектура</span><span class="sxs-lookup"><span data-stu-id="95516-174">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-175">False</span><span class="sxs-lookup"><span data-stu-id="95516-175">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-176">ProductName</span><span class="sxs-lookup"><span data-stu-id="95516-176">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-177">Строка</span><span class="sxs-lookup"><span data-stu-id="95516-177">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-178">False</span><span class="sxs-lookup"><span data-stu-id="95516-178">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-179">FileDescription</span><span class="sxs-lookup"><span data-stu-id="95516-179">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-180">Строка</span><span class="sxs-lookup"><span data-stu-id="95516-180">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-181">False</span><span class="sxs-lookup"><span data-stu-id="95516-181">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-182">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="95516-182">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-183">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="95516-183">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-184">False</span><span class="sxs-lookup"><span data-stu-id="95516-184">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-185">FileVersion</span><span class="sxs-lookup"><span data-stu-id="95516-185">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-186">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="95516-186">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-187">False</span><span class="sxs-lookup"><span data-stu-id="95516-187">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="95516-188">**Процессы** Тип данных Process представляет контейнер для коллекции из одного или нескольких элементов процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-188">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="95516-189">В типе последовательности процессов поддерживаются два дочерних элемента: **Process** и **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="95516-189">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="95516-190">Процесс — это элемент типа процесс, и ShellProcess имеет пустой тип данных.</span><span class="sxs-lookup"><span data-stu-id="95516-190">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="95516-191">В последовательности должно быть идентифицировано по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="95516-191">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="95516-192">**Path (путь** ) Путь обрабатывается RegistrySetting и FileSetting, чтобы ссылаться на пути к реестру и файлам.</span><span class="sxs-lookup"><span data-stu-id="95516-192">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="95516-193">Этот элемент поддерживает два необязательных атрибута: **recursive** и **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="95516-193">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="95516-194">Для обоих значений задано значение по умолчанию = "ложь".</span><span class="sxs-lookup"><span data-stu-id="95516-194">Both values are set to default=”False”.</span></span>

<span data-ttu-id="95516-195">Recursive указывает на то, что путь и все вложенные папки включены для параметров файла или все дочерние разделы реестра включены в параметры реестра.</span><span class="sxs-lookup"><span data-stu-id="95516-195">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="95516-196">В обоих случаях все элементы на текущем уровне включаются в захваченные данные.</span><span class="sxs-lookup"><span data-stu-id="95516-196">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="95516-197">Для объекта FileSettings все файлы в указанной папке включаются в данные, полученные UE-V, но папки не включаются.</span><span class="sxs-lookup"><span data-stu-id="95516-197">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="95516-198">Для путей в реестре записываются все значения из текущего пути, но дочерние разделы реестра не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="95516-198">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="95516-199">В обоих случаях следует соблюдать осторожность, чтобы избежать захвата больших наборов данных или большого количества элементов.</span><span class="sxs-lookup"><span data-stu-id="95516-199">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="95516-200">Атрибут DeleteIfNotFound удаляет параметр из данных пути к хранилищу параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="95516-200">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="95516-201">Это может быть предпочтительнее в случаях, когда при удалении этих параметров из пакета сохраняется большой объем дискового пространства на сервере файлов с путями хранилища параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-201">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="95516-202">**FileMask** FileMask задает только определенные типы файлов для папки, определенной путем.</span><span class="sxs-lookup"><span data-stu-id="95516-202">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="95516-203">Например, Path может быть `C:\users\username\files` и FileMask может `*.txt` содержать только текстовые файлы.</span><span class="sxs-lookup"><span data-stu-id="95516-203">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="95516-204">**RegistrySetting** RegistrySetting представляет контейнер для разделов реестра и значений, а также соответствующее требуемое поведение в части агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-204">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="95516-205">В этом типе определено четыре дочерних элемента: **path**, **Name**, **Exclude**и последовательность значений **path** и **Name**.</span><span class="sxs-lookup"><span data-stu-id="95516-205">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="95516-206">**FileSetting** FileSetting содержат параметры, связанные с путями к файлам и файлам.</span><span class="sxs-lookup"><span data-stu-id="95516-206">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="95516-207">Определены четыре дочерних элемента: **root**, **path**, **FileMask**и **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="95516-207">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="95516-208">Root является обязательным условием, а другие — необязательными.</span><span class="sxs-lookup"><span data-stu-id="95516-208">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="95516-209">**Параметры** Параметры — это контейнер для всех параметров, которые применяются к определенному шаблону.</span><span class="sxs-lookup"><span data-stu-id="95516-209">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="95516-210">Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="95516-210">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="95516-211">Кроме того, он также может содержать следующие дочерние элементы с описанными ниже поведениями.</span><span class="sxs-lookup"><span data-stu-id="95516-211">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95516-212">Элемент</span><span class="sxs-lookup"><span data-stu-id="95516-212">Element</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95516-213">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-213">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-214">Асинхронная репликация</span><span class="sxs-lookup"><span data-stu-id="95516-214">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-215">Пакеты асинхронных параметров применяются без блокирования запуска приложения, чтобы приложение не заблокировалось во время применения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-215">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="95516-216">Это полезно для параметров, которые можно применять асинхронно, например с <code>get/set</code> помощью API-интерфейса, например SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="95516-216">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-217">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="95516-217">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-218">По умолчанию UE-V сохраняет параметры для приложения только в том случае, если вы закрыли последний экземпляр приложения, использующего этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="95516-218">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="95516-219">Если для этого элемента задано значение false, UE-V экспортирует параметры, даже если запущены другие экземпляры приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-219">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="95516-220">Готовые шаблоны — те, которые включают раздел общего элемента, поставляемый с UE-V. Используйте этот флаг, чтобы разрешить общим параметрам возможность всегда экспортировать при закрытии приложения, а также запретить экспорт параметров приложения, пока не закроется последний экземпляр.</span><span class="sxs-lookup"><span data-stu-id="95516-220">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-221">AlwaysApplySettings</span><span class="sxs-lookup"><span data-stu-id="95516-221">AlwaysApplySettings</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-222">(введено в 2,1)</span><span class="sxs-lookup"><span data-stu-id="95516-222">(introduced in 2.1)</span></span></p>
<p><span data-ttu-id="95516-223">Этот параметр принудительно применяет импортированный пакет параметров, даже если между пакетом и текущим состоянием приложения никаких различий.</span><span class="sxs-lookup"><span data-stu-id="95516-223">This parameter forces an imported settings package to be applied even if there are no differences between the package and the current state of the application.</span></span> <span data-ttu-id="95516-224">Этот параметр следует использовать только в особых случаях, так как он может замедлить импорт параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-224">This parameter should be used only in special cases since it can slow down settings import.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a><span data-ttu-id="95516-225">Элемент Name</span><span class="sxs-lookup"><span data-stu-id="95516-225">Name Element</span></span>

**<span data-ttu-id="95516-226">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-226">Mandatory: True</span></span>**

**<span data-ttu-id="95516-227">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-227">Type: String</span></span>**

<span data-ttu-id="95516-228">Name указывает уникальное имя шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-228">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-229">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-229">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-230">Как правило, не следует ссылаться на сведения о версии, так как это может быть объектом из элемента ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-230">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="95516-231">Например, укажите, `<Name>My Application</Name>` а не `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="95516-231">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="95516-232">**Примечание**  UE-V не ссылается на внешние DTD, поэтому невозможно использовать именованные сущности в шаблоне расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-232">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="95516-233">Например, не используйте &reg; для ссылки на зарегистрированный знак товарного знака®.</span><span class="sxs-lookup"><span data-stu-id="95516-233">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="95516-234">Вместо этого используйте канонические нумерованные ссылки, чтобы включить эти типы специальных знаков, например & \ #174 для символа®.</span><span class="sxs-lookup"><span data-stu-id="95516-234">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="95516-235">Это правило применимо ко всем строковым значениям в этом документе.</span><span class="sxs-lookup"><span data-stu-id="95516-235">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="95516-236"><http://www.w3.org/TR/xhtml1/dtds.html>Для получения полного списка сущностей знаков.</span><span class="sxs-lookup"><span data-stu-id="95516-236">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="95516-237">Документы в кодировке UTF-8 могут содержать символы Юникода напрямую.</span><span class="sxs-lookup"><span data-stu-id="95516-237">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="95516-238">Сохранение шаблонов с помощью UE-V Generator автоматически преобразует сущности знаков в их представления Unicode.</span><span class="sxs-lookup"><span data-stu-id="95516-238">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id21"></a><span data-ttu-id="95516-239">Элемент ID</span><span class="sxs-lookup"><span data-stu-id="95516-239">ID Element</span></span>

**<span data-ttu-id="95516-240">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-240">Mandatory: True</span></span>**

**<span data-ttu-id="95516-241">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-241">Type: String</span></span>**

<span data-ttu-id="95516-242">Идентификатор заполняет уникальный идентификатор для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-242">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-243">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения (например, просмотр выходных данных командлетов PowerShell Get-UevTemplate и Get-UevTemplateProgram).</span><span class="sxs-lookup"><span data-stu-id="95516-243">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="95516-244">В соответствии с соглашением этот тег не должен содержать пробелы, что упрощает сценарии.</span><span class="sxs-lookup"><span data-stu-id="95516-244">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="95516-245">Номера версий приложений должны быть указаны в этом элементе, чтобы можно было легко идентифицировать шаблон, например `<ID>MicrosoftCalculator6</ID>` или `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="95516-245">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version21"></a><span data-ttu-id="95516-246">Элемент Version</span><span class="sxs-lookup"><span data-stu-id="95516-246">Version Element</span></span>

**<span data-ttu-id="95516-247">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-247">Mandatory: True</span></span>**

**<span data-ttu-id="95516-248">Тип: целое число</span><span class="sxs-lookup"><span data-stu-id="95516-248">Type: Integer</span></span>**

**<span data-ttu-id="95516-249">Минимальное значение: 0</span><span class="sxs-lookup"><span data-stu-id="95516-249">Minimum Value: 0</span></span>**

**<span data-ttu-id="95516-250">Максимальное значение: 2147483647</span><span class="sxs-lookup"><span data-stu-id="95516-250">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="95516-251">Version определяет версию шаблона расположения параметров для администрирования отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="95516-251">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="95516-252">Генератор UE-V автоматически получает это количество на единицу каждый раз при сохранении шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-252">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="95516-253">Обратите внимание, что это поле должно быть целым числом. дробные значения, например, `<Version>2.5</Version>` недопустимы.</span><span class="sxs-lookup"><span data-stu-id="95516-253">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="95516-254">**Подсказка:** Вы можете сохранять заметки об изменениях в версии с помощью тегов комментариев XML `<!-- -->` , например:</span><span class="sxs-lookup"><span data-stu-id="95516-254">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

<span data-ttu-id="95516-255">**Важно!**  Это значение запрашивается, чтобы определить, следует ли применять новую версию шаблона к существующему шаблону в следующих экземплярах:</span><span class="sxs-lookup"><span data-stu-id="95516-255">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="95516-256">При выполнении задачи "автоматическое обновление шаблона" в расписании</span><span class="sxs-lookup"><span data-stu-id="95516-256">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="95516-257">При выполнении командлета PowerShell Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95516-257">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="95516-258">Когда метод microsoft\\uev: SettingsLocationTemplate Update вызывается через WMI</span><span class="sxs-lookup"><span data-stu-id="95516-258">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author21"></a><span data-ttu-id="95516-259">Элемент Author</span><span class="sxs-lookup"><span data-stu-id="95516-259">Author Element</span></span>

**<span data-ttu-id="95516-260">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-260">Mandatory: False</span></span>**

**<span data-ttu-id="95516-261">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-261">Type: String</span></span>**

<span data-ttu-id="95516-262">Автор определяет создателя шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-262">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="95516-263">Поддерживаются два необязательных дочерних элемента: **имя** и **адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="95516-263">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="95516-264">Оба атрибута являются необязательными, но если указан дочерний элемент электронной почты, он должен сопровождаться элементом name.</span><span class="sxs-lookup"><span data-stu-id="95516-264">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="95516-265">Автор — это полное имя контакта в шаблоне расположения параметров, а адрес электронной почты должен указывать на адрес электронной почты автора.</span><span class="sxs-lookup"><span data-stu-id="95516-265">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="95516-266">Мы рекомендуем использовать эти сведения в шаблонах, опубликованных в открытых источниках, например в [галерее Templates UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="95516-266">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes21"></a><span data-ttu-id="95516-267">Обработка и обработка элементов</span><span class="sxs-lookup"><span data-stu-id="95516-267">Processes and Process Element</span></span>

**<span data-ttu-id="95516-268">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-268">Mandatory: True</span></span>**

**<span data-ttu-id="95516-269">Тип: элемент</span><span class="sxs-lookup"><span data-stu-id="95516-269">Type: Element</span></span>**

<span data-ttu-id="95516-270">Процессы содержат по крайней мере один `<Process>` элемент, который, в свою очередь, включает следующие дочерние элементы: **имя_файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="95516-270">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="95516-271">Дочерний элемент filename является обязательным, а другие — необязательными.</span><span class="sxs-lookup"><span data-stu-id="95516-271">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="95516-272">Полностью заполненный элемент включает теги, похожие на приведенный ниже.</span><span class="sxs-lookup"><span data-stu-id="95516-272">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="95516-273">Файла</span><span class="sxs-lookup"><span data-stu-id="95516-273">Filename</span></span>

**<span data-ttu-id="95516-274">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-274">Mandatory: True</span></span>**

**<span data-ttu-id="95516-275">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-275">Type: String</span></span>**

<span data-ttu-id="95516-276">Filename указывает фактическое имя исполняемого файла в том виде, в котором оно отображается в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="95516-276">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="95516-277">Этот элемент задает основной критерий, который используется UE-V для оценки того, применяется ли шаблон к процессу или нет.</span><span class="sxs-lookup"><span data-stu-id="95516-277">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="95516-278">Этот элемент должен быть указан в XML-файле шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-278">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="95516-279">Допустимые имена файлов не должны соответствовать регулярному выражению \ [^ \ \ \ \ \? \ \ | &lt; &gt; /: \] +, то есть они не могут содержать символы обратной косой черты, звездочки и знаки подстановки вопросительного знака, символ вертикальной черты, знак "больше или меньше" и знак прямой или двоеточие (\ \?</span><span class="sxs-lookup"><span data-stu-id="95516-279">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="95516-280">\* | &lt; &gt; /или: символы.).</span><span class="sxs-lookup"><span data-stu-id="95516-280">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="95516-281">**Подсказка:** Для проверки строки с помощью этого регулярного выражения используйте командное окно PowerShell и подставьте имя исполняемого файла для **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="95516-281">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="95516-282">Значение **true** указывает на то, что строка содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="95516-282">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="95516-283">Ниже приведены некоторые примеры недопустимых значений.</span><span class="sxs-lookup"><span data-stu-id="95516-283">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="95516-284">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="95516-284">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="95516-285">Программа \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="95516-285">Program\*.exe</span></span>

-   <span data-ttu-id="95516-286">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="95516-286">Pro?ram.exe</span></span>

-   <span data-ttu-id="95516-287">Программа &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="95516-287">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="95516-288">**Примечание**  Генератор UE-V кодирует символы "больше" и "меньше" &gt; и &lt; соответственно.</span><span class="sxs-lookup"><span data-stu-id="95516-288">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="95516-289">В редких случаях значение FileName не обязательно должно включать расширение EXE, но оно должно быть задано как часть значения.</span><span class="sxs-lookup"><span data-stu-id="95516-289">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="95516-290">Например, `<Filename>MyApplictication.exe</Filename>` следует указать вместо `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="95516-290">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="95516-291">Второй пример не применяет шаблон к процессу, если фактическим именем исполняемого файла является "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="95516-291">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="95516-292">Архитектура</span><span class="sxs-lookup"><span data-stu-id="95516-292">Architecture</span></span>

**<span data-ttu-id="95516-293">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-293">Mandatory: False</span></span>**

**<span data-ttu-id="95516-294">Тип: архитектура (строка)</span><span class="sxs-lookup"><span data-stu-id="95516-294">Type: Architecture (String)</span></span>**

<span data-ttu-id="95516-295">Архитектура — это архитектура процессора, для которой был скомпилирован целевой исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="95516-295">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="95516-296">Допустимые значения: Win32 для 32-разрядных приложений или Win64 для 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-296">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="95516-297">Если он есть, этот тег ограничивает применимость шаблона расположения параметров для определенной архитектуры приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-297">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="95516-298">Например, Сравните пользовательский интерфейс%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml и MicrosoftOffice2010Win64.xml файлов, включенных в UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-298">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="95516-299">Это полезно, когда относительные пути меняются между различными версиями исполняемого файла, а также в случае, если параметры были добавлены или удалены при переходе с одной архитектуры процессора на другую.</span><span class="sxs-lookup"><span data-stu-id="95516-299">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="95516-300">Если этот элемент отсутствует, шаблон расположения параметров игнорирует архитектуру процесса и применяется как в 32, так и в 64-разрядных процессах, если применяются имя файла и другие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="95516-300">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="95516-301">**Примечание**  UE-V не поддерживает процессоры ARM в этой версии.</span><span class="sxs-lookup"><span data-stu-id="95516-301">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="95516-302">ProductName</span><span class="sxs-lookup"><span data-stu-id="95516-302">ProductName</span></span>

**<span data-ttu-id="95516-303">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-303">Mandatory: False</span></span>**

**<span data-ttu-id="95516-304">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-304">Type: String</span></span>**

<span data-ttu-id="95516-305">ProductName — это необязательный элемент, используемый для идентификации продукта в целях администрирования или создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="95516-305">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="95516-306">Значение ProductName отличается от имени файла тем, что в нем нет ограничений регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="95516-306">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="95516-307">Это позволяет более понятное описание процесса, в котором имя исполняемого файла может быть очевидным.</span><span class="sxs-lookup"><span data-stu-id="95516-307">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="95516-308">Пример</span><span class="sxs-lookup"><span data-stu-id="95516-308">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="95516-309">FileDescription</span><span class="sxs-lookup"><span data-stu-id="95516-309">FileDescription</span></span>

**<span data-ttu-id="95516-310">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-310">Mandatory: False</span></span>**

**<span data-ttu-id="95516-311">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-311">Type: String</span></span>**

<span data-ttu-id="95516-312">FileDescription — необязательный тег, позволяющий административному описанию исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-312">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="95516-313">Это поле с произвольным текстом, которое может быть полезно при различении нескольких исполняемых файлов в пакете программного обеспечения, где необходимо идентифицировать функцию исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-313">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="95516-314">Например, в подходящем приложении может быть полезно получать напоминания о функции двух исполняемых файлов (MyApplication.exe и MyApplicationHelper.exe), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="95516-314">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="95516-315">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="95516-315">ProductVersion</span></span>

**<span data-ttu-id="95516-316">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-316">Mandatory: False</span></span>**

**<span data-ttu-id="95516-317">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-317">Type: String</span></span>**

<span data-ttu-id="95516-318">ProductVersion — это основная и младшая версии файла, а также сборка и уровень исправлений.</span><span class="sxs-lookup"><span data-stu-id="95516-318">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="95516-319">ProductVersion является необязательным элементом, но, если он указан, он должен содержать по крайней мере основной дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="95516-319">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="95516-320">Значение должно выражать диапазон в форме Minimum = "X" максимум = "Y", где X и Y — целые числа.</span><span class="sxs-lookup"><span data-stu-id="95516-320">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="95516-321">Минимальное и максимальное значения могут быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="95516-321">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="95516-322">Элементы "продукт" и "версия файла" могут остаться не установленными.</span><span class="sxs-lookup"><span data-stu-id="95516-322">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="95516-323">Таким образом, шаблон "зависит от версии", то есть шаблон будет применяться ко всем версиям указанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-323">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="95516-324">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="95516-324">Example 1:</span></span>**

<span data-ttu-id="95516-325">Версия продукта: 1,0, указанная в генераторе UE-V, создает следующий XML-код:</span><span class="sxs-lookup"><span data-stu-id="95516-325">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="95516-326">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="95516-326">Example 2:</span></span>**

<span data-ttu-id="95516-327">Версия файла: 5.0.2.1000, указанная в генераторе UE-V, создает следующий XML-код:</span><span class="sxs-lookup"><span data-stu-id="95516-327">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="95516-328">Недопустимый пример 1 — неполный диапазон:</span><span class="sxs-lookup"><span data-stu-id="95516-328">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="95516-329">Присутствует только атрибут Minimum.</span><span class="sxs-lookup"><span data-stu-id="95516-329">Only the Minimum attribute is present.</span></span> <span data-ttu-id="95516-330">Максимальное значение также должно быть включено в диапазон.</span><span class="sxs-lookup"><span data-stu-id="95516-330">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="95516-331">Недопустимый пример 2 — дополнительный номер без основного элемента:</span><span class="sxs-lookup"><span data-stu-id="95516-331">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="95516-332">Присутствует только младший элемент.</span><span class="sxs-lookup"><span data-stu-id="95516-332">Only the Minor element is present.</span></span> <span data-ttu-id="95516-333">Кроме того, необходимо включить основную версию.</span><span class="sxs-lookup"><span data-stu-id="95516-333">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="95516-334">FileVersion</span><span class="sxs-lookup"><span data-stu-id="95516-334">FileVersion</span></span>

**<span data-ttu-id="95516-335">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-335">Mandatory: False</span></span>**

**<span data-ttu-id="95516-336">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-336">Type: String</span></span>**

<span data-ttu-id="95516-337">FileVersion различает окончательную версию опубликованного приложения и сведения о внутренних сборках для исполняемого компонента.</span><span class="sxs-lookup"><span data-stu-id="95516-337">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="95516-338">Для большинства коммерческих приложений эти номера идентичны.</span><span class="sxs-lookup"><span data-stu-id="95516-338">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="95516-339">Там, где они различаются, версия продукта файла обозначает универсальную версию файла, в то время как версия файла указывает определенную сборку файла (как в случае исправления или обновления).</span><span class="sxs-lookup"><span data-stu-id="95516-339">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="95516-340">Это однозначно определяет файлы без логики обнаружения нарушений.</span><span class="sxs-lookup"><span data-stu-id="95516-340">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="95516-341">Чтобы определить версию продукта и версию файла, щелкните его правой кнопкой мыши в проводнике Windows, выберите пункт Свойства, а затем откройте вкладку сведения.</span><span class="sxs-lookup"><span data-stu-id="95516-341">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="95516-342">Включение элемента FileVersion для приложения позволяет более детально настроить логику обнаружения, но это не требуется для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-342">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="95516-343">Сначала проверяются параметры элемента ProductVersion, а затем FileVersion установлен.</span><span class="sxs-lookup"><span data-stu-id="95516-343">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="95516-344">Будет применяться более строгие настройки.</span><span class="sxs-lookup"><span data-stu-id="95516-344">The more restrictive setting will apply.</span></span>

<span data-ttu-id="95516-345">Дочерние элементы и правила синтаксиса для FileVersion идентичны методам из ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-345">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a><span data-ttu-id="95516-346">Элемент приложения</span><span class="sxs-lookup"><span data-stu-id="95516-346">Application Element</span></span>

<span data-ttu-id="95516-347">Приложение — это контейнер для параметров, которые применяются к определенному приложению.</span><span class="sxs-lookup"><span data-stu-id="95516-347">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="95516-348">Это коллекция указанных ниже полей и типов.</span><span class="sxs-lookup"><span data-stu-id="95516-348">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95516-349">Поле/Тип</span><span class="sxs-lookup"><span data-stu-id="95516-349">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95516-350">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-350">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-351">Name</span><span class="sxs-lookup"><span data-stu-id="95516-351">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-352">Задает уникальное имя для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-352">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-353">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-353">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-354">Дополнительные сведения можно найти в разделе <a href="#name21" data-raw-source="[Name](#name21)"> Name (имя) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-354">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-355">ID</span><span class="sxs-lookup"><span data-stu-id="95516-355">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-356">Заполнение уникального идентификатора для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-356">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-357">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="95516-357">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="95516-358">Дополнительные сведения можно найти в разделе <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-358">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-359">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-359">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-360">Необязательное описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-360">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-361">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="95516-361">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-362">Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-362">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-363">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="95516-363">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-364">Необязательное описание шаблона, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-364">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-365">Версия</span><span class="sxs-lookup"><span data-stu-id="95516-365">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-366">Определяет версию шаблона расположения параметров для администрирования отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="95516-366">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="95516-367">Дополнительные сведения можно найти в разделе <a href="#version21" data-raw-source="[Version](#version21)"> Version (версия) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-367">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-368">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="95516-368">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-369">Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет.</span><span class="sxs-lookup"><span data-stu-id="95516-369">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="95516-370">Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-370">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-371">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="95516-371">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-372">Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365.</span><span class="sxs-lookup"><span data-stu-id="95516-372">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="95516-373">Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-373">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-374">FixedProfile (введено в 2,1)</span><span class="sxs-lookup"><span data-stu-id="95516-374">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-375">Указывает, что этот шаблон может быть связан только с профилем, указанным в этом элементе, и не может быть изменен с помощью WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95516-375">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-376">Процессы</span><span class="sxs-lookup"><span data-stu-id="95516-376">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-377">Контейнер для коллекции из одного или нескольких элементов процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-377">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="95516-378">Дополнительные сведения можно найти в разделе <a href="#processes21" data-raw-source="[Processes](#processes21)"> процессы </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-378">For more information, see <a href="#processes21" data-raw-source="[Processes](#processes21)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-379">Параметры</span><span class="sxs-lookup"><span data-stu-id="95516-379">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-380">Контейнер для всех параметров, которые применяются к определенному шаблону.</span><span class="sxs-lookup"><span data-stu-id="95516-380">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="95516-381">Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction.</span><span class="sxs-lookup"><span data-stu-id="95516-381">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="95516-382">Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data21" data-raw-source="[Data types](#data21)"> типов данных </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-382">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a><span data-ttu-id="95516-383">Общий элемент</span><span class="sxs-lookup"><span data-stu-id="95516-383">Common Element</span></span>

<span data-ttu-id="95516-384">Общие похожи на элементы приложения, но всегда связаны с двумя или более элементами приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-384">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="95516-385">Общий раздел представляет набор параметров, которые совместно используются в этих экземплярах приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-385">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="95516-386">Это коллекция указанных ниже полей и типов.</span><span class="sxs-lookup"><span data-stu-id="95516-386">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95516-387">Поле/Тип</span><span class="sxs-lookup"><span data-stu-id="95516-387">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95516-388">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-388">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-389">Name</span><span class="sxs-lookup"><span data-stu-id="95516-389">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-390">Задает уникальное имя для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-390">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-391">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-391">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-392">Дополнительные сведения можно найти в разделе <a href="#name21" data-raw-source="[Name](#name21)"> Name (имя) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-392">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-393">ID</span><span class="sxs-lookup"><span data-stu-id="95516-393">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-394">Заполнение уникального идентификатора для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-394">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-395">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="95516-395">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="95516-396">Дополнительные сведения можно найти в разделе <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-396">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-397">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-397">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-398">Необязательное описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-398">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-399">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="95516-399">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-400">Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-400">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-401">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="95516-401">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-402">Необязательное описание шаблона, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-402">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-403">Версия</span><span class="sxs-lookup"><span data-stu-id="95516-403">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-404">Определяет версию шаблона расположения параметров для администрирования отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="95516-404">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="95516-405">Дополнительные сведения можно найти в разделе <a href="#version21" data-raw-source="[Version](#version21)"> Version (версия) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-405">For more information, see <a href="#version21" data-raw-source="[Version](#version21)">Version</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-406">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="95516-406">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-407">Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет.</span><span class="sxs-lookup"><span data-stu-id="95516-407">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="95516-408">Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-408">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-409">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="95516-409">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-410">Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365.</span><span class="sxs-lookup"><span data-stu-id="95516-410">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="95516-411">Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-411">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-412">FixedProfile (введено в 2,1)</span><span class="sxs-lookup"><span data-stu-id="95516-412">FixedProfile (Introduced in 2.1)</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-413">Указывает, что этот шаблон может быть связан только с профилем, указанным в этом элементе, и не может быть изменен с помощью WMI или PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95516-413">Specifies that this template can only be associated with the profile specified within this element, and cannot be changed via WMI or PowerShell.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-414">Параметры</span><span class="sxs-lookup"><span data-stu-id="95516-414">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-415">Контейнер для всех параметров, которые применяются к определенному шаблону.</span><span class="sxs-lookup"><span data-stu-id="95516-415">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="95516-416">Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction.</span><span class="sxs-lookup"><span data-stu-id="95516-416">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="95516-417">Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data21" data-raw-source="[Data types](#data21)"> типов данных </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-417">For more information, see <strong>Settings</strong> in <a href="#data21" data-raw-source="[Data types](#data21)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a><span data-ttu-id="95516-418">Элемент SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="95516-418">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="95516-419">Этот элемент определяет параметры отдельного приложения или набора приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-419">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="95516-420">Поле/Тип</span><span class="sxs-lookup"><span data-stu-id="95516-420">Field/Type</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="95516-421">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-421">Description</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-422">Name</span><span class="sxs-lookup"><span data-stu-id="95516-422">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-423">Задает уникальное имя для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-423">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-424">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-424">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-425">Дополнительные сведения можно найти в разделе <a href="#name21" data-raw-source="[Name](#name21)"> Name (имя) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-425">For more information, see <a href="#name21" data-raw-source="[Name](#name21)">Name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-426">ID</span><span class="sxs-lookup"><span data-stu-id="95516-426">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-427">Заполнение уникального идентификатора для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-427">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-428">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="95516-428">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="95516-429">Дополнительные сведения можно найти в разделе <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-429">For more information, see <a href="#id21" data-raw-source="[ID](#id21)">ID</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-430">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-430">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-431">Необязательное описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-431">An optional description of the template.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-432">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="95516-432">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-433">Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-433">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-434">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="95516-434">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-435">Необязательное описание шаблона, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-435">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a><span data-ttu-id="95516-436">Приложение: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="95516-436">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="95516-437">Ниже приведен пример файла SettingsLocationTemplate. xsd, в котором показаны элементы, дочерние элементы, атрибуты и параметры.</span><span class="sxs-lookup"><span data-stu-id="95516-437">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## <span data-ttu-id="95516-438">Справочник по схемам шаблонов приложений UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="95516-438">UE-V 2.0 Application Template Schema Reference</span></span>


<span data-ttu-id="95516-439">В этом разделе описана структура XML для шаблона расположения параметров UE-V 2,0 и приведены инструкции по изменению этого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-439">This section details the XML structure of the UE-V 2.0 settings location template and provides guidance for editing this file.</span></span>

### <span data-ttu-id="95516-440">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="95516-440">In This Section</span></span>

-   [<span data-ttu-id="95516-441">Объявление XML и атрибут кодировки</span><span class="sxs-lookup"><span data-stu-id="95516-441">XML Declaration and Encoding Attribute</span></span>](#xml)

-   [<span data-ttu-id="95516-442">Пространство имен и корневой элемент</span><span class="sxs-lookup"><span data-stu-id="95516-442">Namespace and Root Element</span></span>](#namespace)

-   [<span data-ttu-id="95516-443">Типы данных</span><span class="sxs-lookup"><span data-stu-id="95516-443">Data types</span></span>](#data)

-   [<span data-ttu-id="95516-444">Элемент Name</span><span class="sxs-lookup"><span data-stu-id="95516-444">Name Element</span></span>](#name)

-   [<span data-ttu-id="95516-445">Элемент ID</span><span class="sxs-lookup"><span data-stu-id="95516-445">ID Element</span></span>](#id)

-   [<span data-ttu-id="95516-446">Элемент Version</span><span class="sxs-lookup"><span data-stu-id="95516-446">Version Element</span></span>](#version)

-   [<span data-ttu-id="95516-447">Элемент Author</span><span class="sxs-lookup"><span data-stu-id="95516-447">Author Element</span></span>](#author)

-   [<span data-ttu-id="95516-448">Обработка и обработка элементов</span><span class="sxs-lookup"><span data-stu-id="95516-448">Processes and Process Element</span></span>](#processes)

-   [<span data-ttu-id="95516-449">Элемент приложения</span><span class="sxs-lookup"><span data-stu-id="95516-449">Application Element</span></span>](#application)

-   [<span data-ttu-id="95516-450">Общий элемент</span><span class="sxs-lookup"><span data-stu-id="95516-450">Common Element</span></span>](#common)

-   [<span data-ttu-id="95516-451">Элемент SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="95516-451">SettingsLocationTemplate Element</span></span>](#settingslocationtemplate)

-   [<span data-ttu-id="95516-452">Приложение: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="95516-452">Appendix: SettingsLocationTemplate.xsd</span></span>](#appendix)

### <a href="" id="xml"></a><span data-ttu-id="95516-453">Объявление XML и атрибут кодировки</span><span class="sxs-lookup"><span data-stu-id="95516-453">XML Declaration and Encoding Attribute</span></span>

**<span data-ttu-id="95516-454">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-454">Mandatory: True</span></span>**

**<span data-ttu-id="95516-455">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-455">Type: String</span></span>**

<span data-ttu-id="95516-456">В XML-объявлении должен быть указан атрибут версии 1,0 ( &lt; ? XML Version = "1.0" &gt; ).</span><span class="sxs-lookup"><span data-stu-id="95516-456">The XML declaration must specify the XML version 1.0 attribute (&lt;?xml version="1.0"&gt;).</span></span> <span data-ttu-id="95516-457">Шаблоны местоположения параметров, созданные генератором UE-V, сохраняются в кодировке UTF-8, хотя кодировка явно не указана.</span><span class="sxs-lookup"><span data-stu-id="95516-457">Settings location templates created by the UE-V Generator are saved in UTF-8 encoding, although the encoding is not explicitly specified.</span></span> <span data-ttu-id="95516-458">Рекомендуется включить в этот элемент атрибут Encoding = "UTF-8".</span><span class="sxs-lookup"><span data-stu-id="95516-458">We recommend that you include the encoding="UTF-8" attribute in this element as a best practice.</span></span> <span data-ttu-id="95516-459">Все шаблоны, включенные в продукт, задают этот тег (вы также увидите документы в%ProgramFiles%\\Microsoft взаимодействия с пользователем Virtualization\\Templates для справки).</span><span class="sxs-lookup"><span data-stu-id="95516-459">All templates included with the product specify this tag as well (see the documents in %ProgramFiles%\\Microsoft User Experience Virtualization\\Templates for reference).</span></span> <span data-ttu-id="95516-460">Пример</span><span class="sxs-lookup"><span data-stu-id="95516-460">For example:</span></span>

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a><span data-ttu-id="95516-461">Пространство имен и корневой элемент</span><span class="sxs-lookup"><span data-stu-id="95516-461">Namespace and Root Element</span></span>

**<span data-ttu-id="95516-462">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-462">Mandatory: True</span></span>**

**<span data-ttu-id="95516-463">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-463">Type: String</span></span>**

<span data-ttu-id="95516-464">UE-V использует https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate пространство имен для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-464">UE-V uses the https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate namespace for all applications.</span></span> <span data-ttu-id="95516-465">SettingsLocationTemplate является корневым элементом и содержит все остальные элементы.</span><span class="sxs-lookup"><span data-stu-id="95516-465">SettingsLocationTemplate is the root element and contains all other elements.</span></span> <span data-ttu-id="95516-466">Ссылка на SettingsLocationTemplate во всех шаблонах, использующих этот тег:</span><span class="sxs-lookup"><span data-stu-id="95516-466">Reference SettingsLocationTemplate in all templates using this tag:</span></span>

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a><span data-ttu-id="95516-467">Типы данных</span><span class="sxs-lookup"><span data-stu-id="95516-467">Data types</span></span>

<span data-ttu-id="95516-468">Это типы данных для схемы шаблонов приложений UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-468">These are the data types for the UE-V application template schema.</span></span>

<a href="" id="guid"></a><span data-ttu-id="95516-469">**Идентификатор GUID** GUID описывает стандартное выражение глобального уникального идентификатора в форме "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\" [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a – ОС – F0-9 \] {12} \ \} ".</span><span class="sxs-lookup"><span data-stu-id="95516-469">**GUID** GUID describes a standard globally unique identifier regular expression in the form "\\{\[a-fA-F0-9\]{8}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{4}-\[a-fA-F0-9\]{12}\\}".</span></span> <span data-ttu-id="95516-470">Используется в элементе Filesetting\\Root\\KnownFolder для проверки форматирования известных папок.</span><span class="sxs-lookup"><span data-stu-id="95516-470">This is used in the Filesetting\\Root\\KnownFolder element to verify the formatting of well-known folders.</span></span>

<a href="" id="filenamestring"></a><span data-ttu-id="95516-471">**FilenameString** FilenameString — имя файла отслеживаемого процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-471">**FilenameString** FilenameString refers to the file name of a process to be monitored.</span></span> <span data-ttu-id="95516-472">Его значения ограничены регулярным выражением \ [^ \ \ \ \ \ \ \ \ \ \ \ \ | &lt; &gt; /: \] + (это означает, что они не содержат знаков обратной косой черты, знака звездочки или символа подстановки с вопросительным знаком, символа вертикальной черты, знака "больше или меньше", знаков после запятой или двоеточия).</span><span class="sxs-lookup"><span data-stu-id="95516-472">Its values are restricted by the regex \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, (that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon characters).</span></span>

<a href="" id="idstring"></a><span data-ttu-id="95516-473">**IDString** IDString относится к значению идентификатора элементов приложения, SettingsLocationTemplate и часто используемых элементов (используется для описания наборов приложений с общими параметрами).</span><span class="sxs-lookup"><span data-stu-id="95516-473">**IDString** IDString refers to the ID value of Application elements, SettingsLocationTemplate, and Common elements (used to describe application suites that share common settings).</span></span> <span data-ttu-id="95516-474">Оно ограничено тем же регулярным выражением, что и FilenameString (\ [^ &lt; &gt; ] /:\]+).</span><span class="sxs-lookup"><span data-stu-id="95516-474">It is restricted by the same regex as FilenameString (\[^\\\\\\?\\\*\\|&lt;&gt;/:\]+).</span></span>

<a href="" id="templateversion"></a><span data-ttu-id="95516-475">**TemplateVersion** TemplateVersion — это целочисленное значение, используемое для описания редакции шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-475">**TemplateVersion** TemplateVersion is an integer value used to describe the revision of the settings location template.</span></span> <span data-ttu-id="95516-476">Его значение может находиться в диапазоне от 0 до 2147483647.</span><span class="sxs-lookup"><span data-stu-id="95516-476">Its value may range from 0 to 2147483647.</span></span>

<a href="" id="empty"></a><span data-ttu-id="95516-477">**Пустой** Пустой объект ссылается на пустое значение.</span><span class="sxs-lookup"><span data-stu-id="95516-477">**Empty** Empty refers to a null value.</span></span> <span data-ttu-id="95516-478">Используется в Process\\ShellProcess, чтобы указать, что отсутствует процесс для отслеживания.</span><span class="sxs-lookup"><span data-stu-id="95516-478">This is used in Process\\ShellProcess to indicate that there is no process to monitor.</span></span> <span data-ttu-id="95516-479">Это значение не следует использовать ни в каких шаблонах приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-479">This value should not be used in any application templates.</span></span>

<a href="" id="author"></a><span data-ttu-id="95516-480">**Автор** Тип данных Author — это сложный тип, который определяет автора шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-480">**Author** The Author data type is a complex type that identifies the author of a template.</span></span> <span data-ttu-id="95516-481">Он состоит из двух дочерних элементов: **имя** и **адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="95516-481">It contains two child elements: **Name** and **Email**.</span></span> <span data-ttu-id="95516-482">В типе данных Author элемент name является обязательным, а элемент электронной почты — необязательным.</span><span class="sxs-lookup"><span data-stu-id="95516-482">Within the Author data type, the Name element is mandatory while the Email element is optional.</span></span> <span data-ttu-id="95516-483">Этот тип подробно описан в элементе SettingsLocationTemplate.</span><span class="sxs-lookup"><span data-stu-id="95516-483">This type is described in more detail under the SettingsLocationTemplate element.</span></span>

<a href="" id="range"></a><span data-ttu-id="95516-484">**Range (диапазон** ) Диапазон. определяет целочисленный класс, состоящий из двух дочерних элементов: **минимума** и **максимума**.</span><span class="sxs-lookup"><span data-stu-id="95516-484">**Range** Range defines an integer class consisting of two child elements: **Minimum** and **Maximum**.</span></span> <span data-ttu-id="95516-485">Этот тип данных реализован в типе данных ProcessVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-485">This data type is implemented in the ProcessVersion data type.</span></span> <span data-ttu-id="95516-486">Если задано значение, должно быть включено как минимальное, так и максимальное значения.</span><span class="sxs-lookup"><span data-stu-id="95516-486">If specified, both Minimum and Maximum values must be included.</span></span>

<a href="" id="processversion"></a><span data-ttu-id="95516-487">**ProcessVersion** ProcessVersion определяет тип с четырьмя дочерними элементами: **основными**, **дополнительными**, **сборками**и **исправлениями**.</span><span class="sxs-lookup"><span data-stu-id="95516-487">**ProcessVersion** ProcessVersion defines a type with four child elements: **Major**, **Minor**, **Build**, and **Patch**.</span></span> <span data-ttu-id="95516-488">Этот тип данных используется элементом Process для заполнения его значений ProductVersion и FileVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-488">This data type is used by the Process element to populate its ProductVersion and FileVersion values.</span></span> <span data-ttu-id="95516-489">Данными для этого типа является значение Range.</span><span class="sxs-lookup"><span data-stu-id="95516-489">The data for this type is a Range value.</span></span> <span data-ttu-id="95516-490">Основной дочерний элемент является обязательным, а остальные являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="95516-490">The Major child element is mandatory and the others are optional.</span></span>

<a href="" id="architecture"></a><span data-ttu-id="95516-491">**Архитектура** Архитектура перечисляет два возможных значения: **Win32** и **Win64**.</span><span class="sxs-lookup"><span data-stu-id="95516-491">**Architecture** Architecture enumerates two possible values: **Win32** and **Win64**.</span></span> <span data-ttu-id="95516-492">Эти значения используются для определения архитектуры процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-492">These values are used to specify process architecture.</span></span>

<a href="" id="process"></a><span data-ttu-id="95516-493">**Процесс** Тип данных «процесс» — это контейнер, используемый для описания процессов, которые необходимо отслеживать с помощью UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-493">**Process** The Process data type is a container used to describe processes to be monitored by UE-V.</span></span> <span data-ttu-id="95516-494">Он состоит из шести дочерних элементов: **имя файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="95516-494">It contains six child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="95516-495">В этой таблице подробно описываются соответствующие типы данных каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="95516-495">This table details each element’s respective data type:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95516-496">Элемент</span><span class="sxs-lookup"><span data-stu-id="95516-496">Element</span></span></th>
<th align="left"><span data-ttu-id="95516-497">Тип данных</span><span class="sxs-lookup"><span data-stu-id="95516-497">Data Type</span></span></th>
<th align="left"><span data-ttu-id="95516-498">Обязательное</span><span class="sxs-lookup"><span data-stu-id="95516-498">Mandatory</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-499">Файла</span><span class="sxs-lookup"><span data-stu-id="95516-499">Filename</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-500">FilenameString</span><span class="sxs-lookup"><span data-stu-id="95516-500">FilenameString</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-501">True</span><span class="sxs-lookup"><span data-stu-id="95516-501">True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-502">Архитектура</span><span class="sxs-lookup"><span data-stu-id="95516-502">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-503">Архитектура</span><span class="sxs-lookup"><span data-stu-id="95516-503">Architecture</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-504">False</span><span class="sxs-lookup"><span data-stu-id="95516-504">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-505">ProductName</span><span class="sxs-lookup"><span data-stu-id="95516-505">ProductName</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-506">Строка</span><span class="sxs-lookup"><span data-stu-id="95516-506">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-507">False</span><span class="sxs-lookup"><span data-stu-id="95516-507">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-508">FileDescription</span><span class="sxs-lookup"><span data-stu-id="95516-508">FileDescription</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-509">Строка</span><span class="sxs-lookup"><span data-stu-id="95516-509">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-510">False</span><span class="sxs-lookup"><span data-stu-id="95516-510">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-511">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="95516-511">ProductVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-512">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="95516-512">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-513">False</span><span class="sxs-lookup"><span data-stu-id="95516-513">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-514">FileVersion</span><span class="sxs-lookup"><span data-stu-id="95516-514">FileVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-515">ProcessVersion</span><span class="sxs-lookup"><span data-stu-id="95516-515">ProcessVersion</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-516">False</span><span class="sxs-lookup"><span data-stu-id="95516-516">False</span></span></p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a><span data-ttu-id="95516-517">**Процессы** Тип данных Process представляет контейнер для коллекции из одного или нескольких элементов процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-517">**Processes** The Processes data type represents a container for a collection of one or more Process elements.</span></span> <span data-ttu-id="95516-518">В типе последовательности процессов поддерживаются два дочерних элемента: **Process** и **ShellProcess**.</span><span class="sxs-lookup"><span data-stu-id="95516-518">Two child elements are supported in the Processes sequence type: **Process** and **ShellProcess**.</span></span> <span data-ttu-id="95516-519">Процесс — это элемент типа процесс, и ShellProcess имеет пустой тип данных.</span><span class="sxs-lookup"><span data-stu-id="95516-519">Process is an element of type Process and ShellProcess is of data type Empty.</span></span> <span data-ttu-id="95516-520">В последовательности должно быть идентифицировано по крайней мере один элемент.</span><span class="sxs-lookup"><span data-stu-id="95516-520">At least one item must be identified in the sequence.</span></span>

<a href="" id="path"></a><span data-ttu-id="95516-521">**Path (путь** ) Путь обрабатывается RegistrySetting и FileSetting, чтобы ссылаться на пути к реестру и файлам.</span><span class="sxs-lookup"><span data-stu-id="95516-521">**Path** Path is consumed by RegistrySetting and FileSetting to refer to registry and file paths.</span></span> <span data-ttu-id="95516-522">Этот элемент поддерживает два необязательных атрибута: **recursive** и **DeleteIfNotFound**.</span><span class="sxs-lookup"><span data-stu-id="95516-522">This element supports two optional attributes: **Recursive** and **DeleteIfNotFound**.</span></span> <span data-ttu-id="95516-523">Для обоих значений задано значение по умолчанию = "ложь".</span><span class="sxs-lookup"><span data-stu-id="95516-523">Both values are set to default=”False”.</span></span>

<span data-ttu-id="95516-524">Recursive указывает на то, что путь и все вложенные папки включены для параметров файла или все дочерние разделы реестра включены в параметры реестра.</span><span class="sxs-lookup"><span data-stu-id="95516-524">Recursive indicates that the path and all subfolders are included for file settings or that all child registry keys are included for registry settings.</span></span> <span data-ttu-id="95516-525">В обоих случаях все элементы на текущем уровне включаются в захваченные данные.</span><span class="sxs-lookup"><span data-stu-id="95516-525">In both cases, all items at the current level are included in the data captured.</span></span> <span data-ttu-id="95516-526">Для объекта FileSettings все файлы в указанной папке включаются в данные, полученные UE-V, но папки не включаются.</span><span class="sxs-lookup"><span data-stu-id="95516-526">For a FileSettings object, all files within the specified folder are included in the data captured by UE-V but folders are not included.</span></span> <span data-ttu-id="95516-527">Для путей в реестре записываются все значения из текущего пути, но дочерние разделы реестра не фиксируются.</span><span class="sxs-lookup"><span data-stu-id="95516-527">For registry paths, all values in the current path are captured but child registry keys are not captured.</span></span> <span data-ttu-id="95516-528">В обоих случаях следует соблюдать осторожность, чтобы избежать захвата больших наборов данных или большого количества элементов.</span><span class="sxs-lookup"><span data-stu-id="95516-528">In both cases, care should be taken to avoid capturing large data sets or large numbers of items.</span></span>

<span data-ttu-id="95516-529">Атрибут DeleteIfNotFound удаляет параметр из данных пути к хранилищу параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="95516-529">The DeleteIfNotFound attribute removes the setting from the user’s settings storage path data.</span></span> <span data-ttu-id="95516-530">Это может быть предпочтительнее в случаях, когда при удалении этих параметров из пакета сохраняется большой объем дискового пространства на сервере файлов с путями хранилища параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-530">This may be desirable in cases where removing these settings from the package will save a large amount of disk space on the settings storage path file server.</span></span>

<a href="" id="filemask"></a><span data-ttu-id="95516-531">**FileMask** FileMask задает только определенные типы файлов для папки, определенной путем.</span><span class="sxs-lookup"><span data-stu-id="95516-531">**FileMask** FileMask specifies only certain file types for the folder that is defined by Path.</span></span> <span data-ttu-id="95516-532">Например, Path может быть `C:\users\username\files` и FileMask может `*.txt` содержать только текстовые файлы.</span><span class="sxs-lookup"><span data-stu-id="95516-532">For example, Path might be `C:\users\username\files` and FileMask could be `*.txt` to include only text files.</span></span>

<a href="" id="registrysetting"></a><span data-ttu-id="95516-533">**RegistrySetting** RegistrySetting представляет контейнер для разделов реестра и значений, а также соответствующее требуемое поведение в части агента UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-533">**RegistrySetting** RegistrySetting represents a container for registry keys and values and the associated desired behavior on the part of the UE-V Agent.</span></span> <span data-ttu-id="95516-534">В этом типе определено четыре дочерних элемента: **path**, **Name**, **Exclude**и последовательность значений **path** и **Name**.</span><span class="sxs-lookup"><span data-stu-id="95516-534">Four child elements are defined within this type: **Path**, **Name**, **Exclude**, and a sequence of the values **Path** and **Name**.</span></span>

<a href="" id="filesetting"></a><span data-ttu-id="95516-535">**FileSetting** FileSetting содержат параметры, связанные с путями к файлам и файлам.</span><span class="sxs-lookup"><span data-stu-id="95516-535">**FileSetting** FileSetting contains parameters associated with files and files paths.</span></span> <span data-ttu-id="95516-536">Определены четыре дочерних элемента: **root**, **path**, **FileMask**и **Exclude**.</span><span class="sxs-lookup"><span data-stu-id="95516-536">Four child elements are defined: **Root**, **Path**, **FileMask**, and **Exclude**.</span></span> <span data-ttu-id="95516-537">Root является обязательным условием, а другие — необязательными.</span><span class="sxs-lookup"><span data-stu-id="95516-537">Root is mandatory and the others are optional.</span></span>

<a href="" id="settings"></a><span data-ttu-id="95516-538">**Параметры** Параметры — это контейнер для всех параметров, которые применяются к определенному шаблону.</span><span class="sxs-lookup"><span data-stu-id="95516-538">**Settings** Settings is a container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="95516-539">Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="95516-539">It contains instances of the Registry, File, SystemParameter, and CustomAction settings described earlier.</span></span> <span data-ttu-id="95516-540">Кроме того, он также может содержать следующие дочерние элементы с описанными ниже поведениями.</span><span class="sxs-lookup"><span data-stu-id="95516-540">In addition, it can also contain the following child elements with behaviors described:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95516-541">Элемент</span><span class="sxs-lookup"><span data-stu-id="95516-541">Element</span></span></th>
<th align="left"><span data-ttu-id="95516-542">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-542">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-543">Асинхронная репликация</span><span class="sxs-lookup"><span data-stu-id="95516-543">Asynchronous</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-544">Пакеты асинхронных параметров применяются без блокирования запуска приложения, чтобы приложение не заблокировалось во время применения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-544">Asynchronous settings packages are applied without blocking the application startup so that the application start proceeds while the settings are still being applied.</span></span> <span data-ttu-id="95516-545">Это полезно для параметров, которые можно применять асинхронно, например с <code>get/set</code> помощью API-интерфейса, например SystemParameterSetting.</span><span class="sxs-lookup"><span data-stu-id="95516-545">This is useful for settings that can be applied asynchronously, such as those <code>get/set</code> through an API, like SystemParameterSetting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-546">PreventOverlappingSynchronization</span><span class="sxs-lookup"><span data-stu-id="95516-546">PreventOverlappingSynchronization</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-547">По умолчанию UE-V сохраняет параметры для приложения только в том случае, если вы закрыли последний экземпляр приложения, использующего этот шаблон.</span><span class="sxs-lookup"><span data-stu-id="95516-547">By default, UE-V only saves settings for an application when the last instance of an application using the template is closed.</span></span> <span data-ttu-id="95516-548">Если для этого элемента задано значение false, UE-V экспортирует параметры, даже если запущены другие экземпляры приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-548">When this element is set to ‘false’, UE-V exports the settings even if other instances of an application are running.</span></span> <span data-ttu-id="95516-549">Готовые шаблоны — те, которые включают раздел общего элемента, поставляемый с UE-V. Используйте этот флаг, чтобы разрешить общим параметрам возможность всегда экспортировать при закрытии приложения, а также запретить экспорт параметров приложения, пока не закроется последний экземпляр.</span><span class="sxs-lookup"><span data-stu-id="95516-549">Suited templates – those that include a Common element section– that are shipped with UE-V use this flag to enable shared settings to always export on application close, while preventing application-specific settings from exporting until the last instance is closed.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a><span data-ttu-id="95516-550">Элемент Name</span><span class="sxs-lookup"><span data-stu-id="95516-550">Name Element</span></span>

**<span data-ttu-id="95516-551">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-551">Mandatory: True</span></span>**

**<span data-ttu-id="95516-552">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-552">Type: String</span></span>**

<span data-ttu-id="95516-553">Name указывает уникальное имя шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-553">Name specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-554">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-554">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-555">Как правило, не следует ссылаться на сведения о версии, так как это может быть объектом из элемента ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-555">In general, avoid referencing version information, as this can be objected from the ProductVersion element.</span></span> <span data-ttu-id="95516-556">Например, укажите, `<Name>My Application</Name>` а не `<Name>My Application 1.1</Name>` .</span><span class="sxs-lookup"><span data-stu-id="95516-556">For example, specify `<Name>My Application</Name>` rather than `<Name>My Application 1.1</Name>`.</span></span>

<span data-ttu-id="95516-557">**Примечание**  UE-V не ссылается на внешние DTD, поэтому невозможно использовать именованные сущности в шаблоне расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-557">**Note** UE-V does not reference external DTDs, so it is not possible to use named entities in a settings location template.</span></span> <span data-ttu-id="95516-558">Например, не используйте &reg; для ссылки на зарегистрированный знак товарного знака®.</span><span class="sxs-lookup"><span data-stu-id="95516-558">For example, do not use &reg; to refer to the registered trade mark sign ®.</span></span> <span data-ttu-id="95516-559">Вместо этого используйте канонические нумерованные ссылки, чтобы включить эти типы специальных знаков, например & \ #174 для символа®.</span><span class="sxs-lookup"><span data-stu-id="95516-559">Instead, use canonical numbered references to include these types of special characters, for example, &\#174 for the ® character.</span></span> <span data-ttu-id="95516-560">Это правило применимо ко всем строковым значениям в этом документе.</span><span class="sxs-lookup"><span data-stu-id="95516-560">This rule applies to all string values in this document.</span></span>

<span data-ttu-id="95516-561"><http://www.w3.org/TR/xhtml1/dtds.html>Для получения полного списка сущностей знаков.</span><span class="sxs-lookup"><span data-stu-id="95516-561">See <http://www.w3.org/TR/xhtml1/dtds.html> for a complete list of character entities.</span></span> <span data-ttu-id="95516-562">Документы в кодировке UTF-8 могут содержать символы Юникода напрямую.</span><span class="sxs-lookup"><span data-stu-id="95516-562">UTF-8-encoded documents may include the Unicode characters directly.</span></span> <span data-ttu-id="95516-563">Сохранение шаблонов с помощью UE-V Generator автоматически преобразует сущности знаков в их представления Unicode.</span><span class="sxs-lookup"><span data-stu-id="95516-563">Saving templates through the UE-V Generator converts character entities to their Unicode representations automatically.</span></span>

 

### <a href="" id="id"></a><span data-ttu-id="95516-564">Элемент ID</span><span class="sxs-lookup"><span data-stu-id="95516-564">ID Element</span></span>

**<span data-ttu-id="95516-565">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-565">Mandatory: True</span></span>**

**<span data-ttu-id="95516-566">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-566">Type: String</span></span>**

<span data-ttu-id="95516-567">Идентификатор заполняет уникальный идентификатор для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-567">ID populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-568">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения (например, просмотр выходных данных командлетов PowerShell Get-UevTemplate и Get-UevTemplateProgram).</span><span class="sxs-lookup"><span data-stu-id="95516-568">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime (for example, see the output of the Get-UevTemplate and Get-UevTemplateProgram PowerShell cmdlets).</span></span> <span data-ttu-id="95516-569">В соответствии с соглашением этот тег не должен содержать пробелы, что упрощает сценарии.</span><span class="sxs-lookup"><span data-stu-id="95516-569">By convention, this tag should not contain any spaces, which simplifies scripting.</span></span> <span data-ttu-id="95516-570">Номера версий приложений должны быть указаны в этом элементе, чтобы можно было легко идентифицировать шаблон, например `<ID>MicrosoftCalculator6</ID>` или `<ID>MicrosoftOffice2010Win64</ID>` .</span><span class="sxs-lookup"><span data-stu-id="95516-570">Version numbers of applications should be specified in this element to allow for easy identification of the template, such as `<ID>MicrosoftCalculator6</ID>` or `<ID>MicrosoftOffice2010Win64</ID>`.</span></span>

### <a href="" id="version"></a><span data-ttu-id="95516-571">Элемент Version</span><span class="sxs-lookup"><span data-stu-id="95516-571">Version Element</span></span>

**<span data-ttu-id="95516-572">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-572">Mandatory: True</span></span>**

**<span data-ttu-id="95516-573">Тип: целое число</span><span class="sxs-lookup"><span data-stu-id="95516-573">Type: Integer</span></span>**

**<span data-ttu-id="95516-574">Минимальное значение: 0</span><span class="sxs-lookup"><span data-stu-id="95516-574">Minimum Value: 0</span></span>**

**<span data-ttu-id="95516-575">Максимальное значение: 2147483647</span><span class="sxs-lookup"><span data-stu-id="95516-575">Maximum Value: 2147483647</span></span>**

<span data-ttu-id="95516-576">Version определяет версию шаблона расположения параметров для администрирования отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="95516-576">Version identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="95516-577">Генератор UE-V автоматически получает это количество на единицу каждый раз при сохранении шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-577">The UE-V Generator automatically increments this number by one each time the template is saved.</span></span> <span data-ttu-id="95516-578">Обратите внимание, что это поле должно быть целым числом. дробные значения, например, `<Version>2.5</Version>` недопустимы.</span><span class="sxs-lookup"><span data-stu-id="95516-578">Notice that this field must be a whole number integer; fractional values, such as `<Version>2.5</Version>` are not allowed.</span></span>

<span data-ttu-id="95516-579">**Подсказка:** Вы можете сохранять заметки об изменениях в версии с помощью тегов комментариев XML `<!-- -->` , например:</span><span class="sxs-lookup"><span data-stu-id="95516-579">**Hint:** You can save notes about version changes using XML comment tags `<!-- -->`, for example:</span></span>

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

<span data-ttu-id="95516-580">**Важно!**  Это значение запрашивается, чтобы определить, следует ли применять новую версию шаблона к существующему шаблону в следующих экземплярах:</span><span class="sxs-lookup"><span data-stu-id="95516-580">**Important** This value is queried to determine if a new version of a template should be applied to an existing template in these instances:</span></span>

-   <span data-ttu-id="95516-581">При выполнении задачи "автоматическое обновление шаблона" в расписании</span><span class="sxs-lookup"><span data-stu-id="95516-581">When the scheduled Template Auto Update task executes</span></span>

-   <span data-ttu-id="95516-582">При выполнении командлета PowerShell Update-UevTemplate</span><span class="sxs-lookup"><span data-stu-id="95516-582">When the Update-UevTemplate PowerShell cmdlet is executed</span></span>

-   <span data-ttu-id="95516-583">Когда метод microsoft\\uev: SettingsLocationTemplate Update вызывается через WMI</span><span class="sxs-lookup"><span data-stu-id="95516-583">When the microsoft\\uev:SettingsLocationTemplate Update method is called through WMI</span></span>

 

### <a href="" id="author"></a><span data-ttu-id="95516-584">Элемент Author</span><span class="sxs-lookup"><span data-stu-id="95516-584">Author Element</span></span>

**<span data-ttu-id="95516-585">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-585">Mandatory: False</span></span>**

**<span data-ttu-id="95516-586">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-586">Type: String</span></span>**

<span data-ttu-id="95516-587">Автор определяет создателя шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-587">Author identifies the creator of the settings location template.</span></span> <span data-ttu-id="95516-588">Поддерживаются два необязательных дочерних элемента: **имя** и **адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="95516-588">Two optional child elements are supported: **Name** and **Email**.</span></span> <span data-ttu-id="95516-589">Оба атрибута являются необязательными, но если указан дочерний элемент электронной почты, он должен сопровождаться элементом name.</span><span class="sxs-lookup"><span data-stu-id="95516-589">Both attributes are optional, but, if the Email child element is specified, it must be accompanied by the Name element.</span></span> <span data-ttu-id="95516-590">Автор — это полное имя контакта в шаблоне расположения параметров, а адрес электронной почты должен указывать на адрес электронной почты автора.</span><span class="sxs-lookup"><span data-stu-id="95516-590">Author refers to the full name of the contact for the settings location template, and email should refer to an email address for the author.</span></span> <span data-ttu-id="95516-591">Мы рекомендуем использовать эти сведения в шаблонах, опубликованных в открытых источниках, например в [галерее Templates UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span><span class="sxs-lookup"><span data-stu-id="95516-591">We recommend that you include this information in templates published publicly, for example, on the [UE-V Template Gallery](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).</span></span>

### <a href="" id="processes"></a><span data-ttu-id="95516-592">Обработка и обработка элементов</span><span class="sxs-lookup"><span data-stu-id="95516-592">Processes and Process Element</span></span>

**<span data-ttu-id="95516-593">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-593">Mandatory: True</span></span>**

**<span data-ttu-id="95516-594">Тип: элемент</span><span class="sxs-lookup"><span data-stu-id="95516-594">Type: Element</span></span>**

<span data-ttu-id="95516-595">Процессы содержат по крайней мере один `<Process>` элемент, который, в свою очередь, включает следующие дочерние элементы: **имя_файла**, **архитектура**, **ProductName**, **FileDescription**, **ProductVersion**и **FileVersion**.</span><span class="sxs-lookup"><span data-stu-id="95516-595">Processes contains at least one `<Process>` element, which in turn contains the following child elements: **Filename**, **Architecture**, **ProductName**, **FileDescription**, **ProductVersion**, and **FileVersion**.</span></span> <span data-ttu-id="95516-596">Дочерний элемент filename является обязательным, а другие — необязательными.</span><span class="sxs-lookup"><span data-stu-id="95516-596">The Filename child element is mandatory and the others are optional.</span></span> <span data-ttu-id="95516-597">Полностью заполненный элемент включает теги, похожие на приведенный ниже.</span><span class="sxs-lookup"><span data-stu-id="95516-597">A fully populated element contains tags similar to this example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### <span data-ttu-id="95516-598">Файла</span><span class="sxs-lookup"><span data-stu-id="95516-598">Filename</span></span>

**<span data-ttu-id="95516-599">Обязательно: истина</span><span class="sxs-lookup"><span data-stu-id="95516-599">Mandatory: True</span></span>**

**<span data-ttu-id="95516-600">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-600">Type: String</span></span>**

<span data-ttu-id="95516-601">Filename указывает фактическое имя исполняемого файла в том виде, в котором оно отображается в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="95516-601">Filename refers to the actual file name of the executable as it appears in the file system.</span></span> <span data-ttu-id="95516-602">Этот элемент задает основной критерий, который используется UE-V для оценки того, применяется ли шаблон к процессу или нет.</span><span class="sxs-lookup"><span data-stu-id="95516-602">This element specifies the primary criterion that UE-V uses to evaluate whether a template applies to a process or not.</span></span> <span data-ttu-id="95516-603">Этот элемент должен быть указан в XML-файле шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-603">This element must be specified in the settings location template XML.</span></span>

<span data-ttu-id="95516-604">Допустимые имена файлов не должны соответствовать регулярному выражению \ [^ \ \ \ \ \? \ \ | &lt; &gt; /: \] +, то есть они не могут содержать символы обратной косой черты, звездочки и знаки подстановки вопросительного знака, символ вертикальной черты, знак "больше или меньше" и знак прямой или двоеточие (\ \?</span><span class="sxs-lookup"><span data-stu-id="95516-604">Valid filenames must not match the regular expression \[^\\\\\\?\\\*\\|&lt;&gt;/:\]+, that is, they may not contain backslash characters, asterisk or question mark wild-card characters, the pipe character, the greater than or less than sign, forward slash, or colon (the \\ ?</span></span> <span data-ttu-id="95516-605">\* | &lt; &gt; /или: символы.).</span><span class="sxs-lookup"><span data-stu-id="95516-605">\* | &lt; &gt; / or : characters.).</span></span>

<span data-ttu-id="95516-606">**Подсказка:** Для проверки строки с помощью этого регулярного выражения используйте командное окно PowerShell и подставьте имя исполняемого файла для **YourFileName**:</span><span class="sxs-lookup"><span data-stu-id="95516-606">**Hint:** To test a string against this regex, use a PowerShell command window and substitute your executable’s name for **YourFileName**:</span></span>

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

<span data-ttu-id="95516-607">Значение **true** указывает на то, что строка содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="95516-607">A value of **True** indicates that the string contains illegal characters.</span></span> <span data-ttu-id="95516-608">Ниже приведены некоторые примеры недопустимых значений.</span><span class="sxs-lookup"><span data-stu-id="95516-608">Here are some examples of illegal values:</span></span>

-   <span data-ttu-id="95516-609">\\\\server\\share\\program.exe</span><span class="sxs-lookup"><span data-stu-id="95516-609">\\\\server\\share\\program.exe</span></span>

-   <span data-ttu-id="95516-610">Программа \ \*. exe</span><span class="sxs-lookup"><span data-stu-id="95516-610">Program\*.exe</span></span>

-   <span data-ttu-id="95516-611">Pro? ram.exe</span><span class="sxs-lookup"><span data-stu-id="95516-611">Pro?ram.exe</span></span>

-   <span data-ttu-id="95516-612">Программа &lt; 1 &gt; . exe</span><span class="sxs-lookup"><span data-stu-id="95516-612">Program&lt;1&gt;.exe</span></span>

<span data-ttu-id="95516-613">**Примечание**  Генератор UE-V кодирует символы "больше" и "меньше" &gt; и &lt; соответственно.</span><span class="sxs-lookup"><span data-stu-id="95516-613">**Note** The UE-V Generator encodes the greater than and less than characters as &gt; and &lt; respectively.</span></span>

 

<span data-ttu-id="95516-614">В редких случаях значение FileName не обязательно должно включать расширение EXE, но оно должно быть задано как часть значения.</span><span class="sxs-lookup"><span data-stu-id="95516-614">In rare circumstances, the FileName value will not necessarily include the .exe extension, but it should be specified as part of the value.</span></span> <span data-ttu-id="95516-615">Например, `<Filename>MyApplictication.exe</Filename>` следует указать вместо `<Filename>MyApplictication</Filename>` .</span><span class="sxs-lookup"><span data-stu-id="95516-615">For example, `<Filename>MyApplictication.exe</Filename>` should be specified instead of `<Filename>MyApplictication</Filename>`.</span></span> <span data-ttu-id="95516-616">Второй пример не применяет шаблон к процессу, если фактическим именем исполняемого файла является "MyApplication.exe".</span><span class="sxs-lookup"><span data-stu-id="95516-616">The second example will not apply the template to the process if the actual name of the executable file is “MyApplication.exe”.</span></span>

### <span data-ttu-id="95516-617">Архитектура</span><span class="sxs-lookup"><span data-stu-id="95516-617">Architecture</span></span>

**<span data-ttu-id="95516-618">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-618">Mandatory: False</span></span>**

**<span data-ttu-id="95516-619">Тип: архитектура (строка)</span><span class="sxs-lookup"><span data-stu-id="95516-619">Type: Architecture (String)</span></span>**

<span data-ttu-id="95516-620">Архитектура — это архитектура процессора, для которой был скомпилирован целевой исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="95516-620">Architecture refers to the processor architecture for which the target executable was compiled.</span></span> <span data-ttu-id="95516-621">Допустимые значения: Win32 для 32-разрядных приложений или Win64 для 64-разрядных приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-621">Valid values are Win32 for 32-bit applications or Win64 for 64-bit applications.</span></span> <span data-ttu-id="95516-622">Если он есть, этот тег ограничивает применимость шаблона расположения параметров для определенной архитектуры приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-622">If present, this tag limits the applicability of the settings location template to a particular application architecture.</span></span> <span data-ttu-id="95516-623">Например, Сравните пользовательский интерфейс%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml и MicrosoftOffice2010Win64.xml файлов, включенных в UE-V.</span><span class="sxs-lookup"><span data-stu-id="95516-623">For an example of this, compare the %ProgramFiles%\\Microsoft User Experience Virtualization\\templates\\ MicrosoftOffice2010Win32.xml and MicrosoftOffice2010Win64.xml files included with UE-V.</span></span> <span data-ttu-id="95516-624">Это полезно, когда относительные пути меняются между различными версиями исполняемого файла, а также в случае, если параметры были добавлены или удалены при переходе с одной архитектуры процессора на другую.</span><span class="sxs-lookup"><span data-stu-id="95516-624">This is useful when relative paths change between different versions of an executable or if settings have been added or removed when moving from one processor architecture to another.</span></span>

<span data-ttu-id="95516-625">Если этот элемент отсутствует, шаблон расположения параметров игнорирует архитектуру процесса и применяется как в 32, так и в 64-разрядных процессах, если применяются имя файла и другие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="95516-625">If this element is absent, the settings location template ignores the process’ architecture and applies to both 32 and 64-bit processes if the file name and other attributes apply.</span></span>

<span data-ttu-id="95516-626">**Примечание**  UE-V не поддерживает процессоры ARM в этой версии.</span><span class="sxs-lookup"><span data-stu-id="95516-626">**Note** UE-V does not support ARM processors in this version.</span></span>

 

### <span data-ttu-id="95516-627">ProductName</span><span class="sxs-lookup"><span data-stu-id="95516-627">ProductName</span></span>

**<span data-ttu-id="95516-628">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-628">Mandatory: False</span></span>**

**<span data-ttu-id="95516-629">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-629">Type: String</span></span>**

<span data-ttu-id="95516-630">ProductName — это необязательный элемент, используемый для идентификации продукта в целях администрирования или создания отчетов.</span><span class="sxs-lookup"><span data-stu-id="95516-630">ProductName is an optional element used to identify a product for administrative purposes or reporting.</span></span> <span data-ttu-id="95516-631">Значение ProductName отличается от имени файла тем, что в нем нет ограничений регулярных выражений.</span><span class="sxs-lookup"><span data-stu-id="95516-631">ProductName differs from Filename in that there are no regular expression restrictions on its value.</span></span> <span data-ttu-id="95516-632">Это позволяет более понятное описание процесса, в котором имя исполняемого файла может быть очевидным.</span><span class="sxs-lookup"><span data-stu-id="95516-632">This allows for more easily understood descriptions of a process where the executable name may not be obvious.</span></span> <span data-ttu-id="95516-633">Пример</span><span class="sxs-lookup"><span data-stu-id="95516-633">For example:</span></span>

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### <span data-ttu-id="95516-634">FileDescription</span><span class="sxs-lookup"><span data-stu-id="95516-634">FileDescription</span></span>

**<span data-ttu-id="95516-635">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-635">Mandatory: False</span></span>**

**<span data-ttu-id="95516-636">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-636">Type: String</span></span>**

<span data-ttu-id="95516-637">FileDescription — необязательный тег, позволяющий административному описанию исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-637">FileDescription is an optional tag that allows for an administrative description of the executable file.</span></span> <span data-ttu-id="95516-638">Это поле с произвольным текстом, которое может быть полезно при различении нескольких исполняемых файлов в пакете программного обеспечения, где необходимо идентифицировать функцию исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-638">This is a free text field and can be useful in distinguishing multiple executables within a software package where there is a need to identify the function of the executable.</span></span>

<span data-ttu-id="95516-639">Например, в подходящем приложении может быть полезно получать напоминания о функции двух исполняемых файлов (MyApplication.exe и MyApplicationHelper.exe), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="95516-639">For example, in a suited application, it might be useful to provide reminders about the function of two executables (MyApplication.exe and MyApplicationHelper.exe), as shown here:</span></span>

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### <span data-ttu-id="95516-640">ProductVersion</span><span class="sxs-lookup"><span data-stu-id="95516-640">ProductVersion</span></span>

**<span data-ttu-id="95516-641">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-641">Mandatory: False</span></span>**

**<span data-ttu-id="95516-642">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-642">Type: String</span></span>**

<span data-ttu-id="95516-643">ProductVersion — это основная и младшая версии файла, а также сборка и уровень исправлений.</span><span class="sxs-lookup"><span data-stu-id="95516-643">ProductVersion refers to the major and minor product versions of a file, as well as a build and patch level.</span></span> <span data-ttu-id="95516-644">ProductVersion является необязательным элементом, но, если он указан, он должен содержать по крайней мере основной дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="95516-644">ProductVersion is an optional element, but if specified, it must contain at least the Major child element.</span></span> <span data-ttu-id="95516-645">Значение должно выражать диапазон в форме Minimum = "X" максимум = "Y", где X и Y — целые числа.</span><span class="sxs-lookup"><span data-stu-id="95516-645">The value must express a range in the form Minimum="X" Maximum="Y" where X and Y are integers.</span></span> <span data-ttu-id="95516-646">Минимальное и максимальное значения могут быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="95516-646">The Minimum and Maximum values can be identical.</span></span>

<span data-ttu-id="95516-647">Элементы "продукт" и "версия файла" могут остаться не установленными.</span><span class="sxs-lookup"><span data-stu-id="95516-647">The product and file version elements may be left unspecified.</span></span> <span data-ttu-id="95516-648">Таким образом, шаблон "зависит от версии", то есть шаблон будет применяться ко всем версиям указанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="95516-648">Doing so makes the template “version agnostic”, meaning that the template will apply to all versions of the specified executable.</span></span>

**<span data-ttu-id="95516-649">Пример 1:</span><span class="sxs-lookup"><span data-stu-id="95516-649">Example 1:</span></span>**

<span data-ttu-id="95516-650">Версия продукта: 1,0, указанная в генераторе UE-V, создает следующий XML-код:</span><span class="sxs-lookup"><span data-stu-id="95516-650">Product version: 1.0 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**<span data-ttu-id="95516-651">Пример 2:</span><span class="sxs-lookup"><span data-stu-id="95516-651">Example 2:</span></span>**

<span data-ttu-id="95516-652">Версия файла: 5.0.2.1000, указанная в генераторе UE-V, создает следующий XML-код:</span><span class="sxs-lookup"><span data-stu-id="95516-652">File version: 5.0.2.1000 specified in the UE-V Generator produces the following XML:</span></span>

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**<span data-ttu-id="95516-653">Недопустимый пример 1 — неполный диапазон:</span><span class="sxs-lookup"><span data-stu-id="95516-653">Incorrect Example 1 – incomplete range:</span></span>**

<span data-ttu-id="95516-654">Присутствует только атрибут Minimum.</span><span class="sxs-lookup"><span data-stu-id="95516-654">Only the Minimum attribute is present.</span></span> <span data-ttu-id="95516-655">Максимальное значение также должно быть включено в диапазон.</span><span class="sxs-lookup"><span data-stu-id="95516-655">Maximum must be included in a range as well.</span></span>

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**<span data-ttu-id="95516-656">Недопустимый пример 2 — дополнительный номер без основного элемента:</span><span class="sxs-lookup"><span data-stu-id="95516-656">Incorrect Example 2 – Minor specified without Major element:</span></span>**

<span data-ttu-id="95516-657">Присутствует только младший элемент.</span><span class="sxs-lookup"><span data-stu-id="95516-657">Only the Minor element is present.</span></span> <span data-ttu-id="95516-658">Кроме того, необходимо включить основную версию.</span><span class="sxs-lookup"><span data-stu-id="95516-658">Major must be included as well.</span></span>

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### <span data-ttu-id="95516-659">FileVersion</span><span class="sxs-lookup"><span data-stu-id="95516-659">FileVersion</span></span>

**<span data-ttu-id="95516-660">Обязательно: ложь</span><span class="sxs-lookup"><span data-stu-id="95516-660">Mandatory: False</span></span>**

**<span data-ttu-id="95516-661">Тип: строка</span><span class="sxs-lookup"><span data-stu-id="95516-661">Type: String</span></span>**

<span data-ttu-id="95516-662">FileVersion различает окончательную версию опубликованного приложения и сведения о внутренних сборках для исполняемого компонента.</span><span class="sxs-lookup"><span data-stu-id="95516-662">FileVersion differentiates between the release version of a published application and the internal build details of a component executable.</span></span> <span data-ttu-id="95516-663">Для большинства коммерческих приложений эти номера идентичны.</span><span class="sxs-lookup"><span data-stu-id="95516-663">For the majority of commercial applications, these numbers are identical.</span></span> <span data-ttu-id="95516-664">Там, где они различаются, версия продукта файла обозначает универсальную версию файла, в то время как версия файла указывает определенную сборку файла (как в случае исправления или обновления).</span><span class="sxs-lookup"><span data-stu-id="95516-664">Where they vary, the product version of a file indicates a generic version identification of a file, while file version indicates a specific build of a file (as in the case of a hotfix or update).</span></span> <span data-ttu-id="95516-665">Это однозначно определяет файлы без логики обнаружения нарушений.</span><span class="sxs-lookup"><span data-stu-id="95516-665">This uniquely identifies files without breaking detection logic.</span></span>

<span data-ttu-id="95516-666">Чтобы определить версию продукта и версию файла, щелкните его правой кнопкой мыши в проводнике Windows, выберите пункт Свойства, а затем откройте вкладку сведения.</span><span class="sxs-lookup"><span data-stu-id="95516-666">To determine the product version and file version of a particular executable, right-click on the file in Windows Explorer, select Properties, then click on the Details tab.</span></span>

<span data-ttu-id="95516-667">Включение элемента FileVersion для приложения позволяет более детально настроить логику обнаружения, но это не требуется для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-667">Including a FileVersion element for an application allows for more granular fine-tuning detection logic, but is not necessary for most applications.</span></span> <span data-ttu-id="95516-668">Сначала проверяются параметры элемента ProductVersion, а затем FileVersion установлен.</span><span class="sxs-lookup"><span data-stu-id="95516-668">The ProductVersion element settings are checked first, and then FileVersion is checked.</span></span> <span data-ttu-id="95516-669">Будет применяться более строгие настройки.</span><span class="sxs-lookup"><span data-stu-id="95516-669">The more restrictive setting will apply.</span></span>

<span data-ttu-id="95516-670">Дочерние элементы и правила синтаксиса для FileVersion идентичны методам из ProductVersion.</span><span class="sxs-lookup"><span data-stu-id="95516-670">The child elements and syntax rules for FileVersion are identical to those of ProductVersion.</span></span>

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a><span data-ttu-id="95516-671">Элемент приложения</span><span class="sxs-lookup"><span data-stu-id="95516-671">Application Element</span></span>

<span data-ttu-id="95516-672">Приложение — это контейнер для параметров, которые применяются к определенному приложению.</span><span class="sxs-lookup"><span data-stu-id="95516-672">Application is a container for settings that apply to a particular application.</span></span> <span data-ttu-id="95516-673">Это коллекция указанных ниже полей и типов.</span><span class="sxs-lookup"><span data-stu-id="95516-673">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95516-674">Поле/Тип</span><span class="sxs-lookup"><span data-stu-id="95516-674">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="95516-675">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-675">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-676">Name</span><span class="sxs-lookup"><span data-stu-id="95516-676">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-677">Задает уникальное имя для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-677">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-678">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-678">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-679">Дополнительные сведения можно найти в разделе <a href="#name" data-raw-source="[Name](#name)"> Name (имя) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-679">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-680">ID</span><span class="sxs-lookup"><span data-stu-id="95516-680">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-681">Заполнение уникального идентификатора для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-681">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-682">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="95516-682">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="95516-683">Дополнительные сведения можно найти в разделе <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-683">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-684">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-684">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-685">Необязательное описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-685">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-686">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="95516-686">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-687">Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-687">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-688">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="95516-688">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-689">Необязательное описание шаблона, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-689">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-690">Версия</span><span class="sxs-lookup"><span data-stu-id="95516-690">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-691">Определяет версию шаблона расположения параметров для администрирования отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="95516-691">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="95516-692">Дополнительные сведения можно найти в разделе <a href="#version" data-raw-source="[Version](#version)"> Version (версия) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-692">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-693">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="95516-693">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-694">Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет.</span><span class="sxs-lookup"><span data-stu-id="95516-694">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="95516-695">Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-695">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-696">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="95516-696">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-697">Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365.</span><span class="sxs-lookup"><span data-stu-id="95516-697">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="95516-698">Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-698">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-699">Процессы</span><span class="sxs-lookup"><span data-stu-id="95516-699">Processes</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-700">Контейнер для коллекции из одного или нескольких элементов процесса.</span><span class="sxs-lookup"><span data-stu-id="95516-700">A container for a collection of one or more Process elements.</span></span> <span data-ttu-id="95516-701">Дополнительные сведения можно найти в разделе <a href="#processes" data-raw-source="[Processes](#processes)"> процессы </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-701">For more information, see <a href="#processes" data-raw-source="[Processes](#processes)">Processes</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-702">Параметры</span><span class="sxs-lookup"><span data-stu-id="95516-702">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-703">Контейнер для всех параметров, которые применяются к определенному шаблону.</span><span class="sxs-lookup"><span data-stu-id="95516-703">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="95516-704">Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction.</span><span class="sxs-lookup"><span data-stu-id="95516-704">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="95516-705">Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data" data-raw-source="[Data types](#data)"> типов данных </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-705">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a><span data-ttu-id="95516-706">Общий элемент</span><span class="sxs-lookup"><span data-stu-id="95516-706">Common Element</span></span>

<span data-ttu-id="95516-707">Общие похожи на элементы приложения, но всегда связаны с двумя или более элементами приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-707">Common is similar to an Application element, but it is always associated with two or more Application elements.</span></span> <span data-ttu-id="95516-708">Общий раздел представляет набор параметров, которые совместно используются в этих экземплярах приложения.</span><span class="sxs-lookup"><span data-stu-id="95516-708">The Common section represents the set of settings that are shared between those Application instances.</span></span> <span data-ttu-id="95516-709">Это коллекция указанных ниже полей и типов.</span><span class="sxs-lookup"><span data-stu-id="95516-709">It is a collection of the following fields/types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95516-710">Поле/Тип</span><span class="sxs-lookup"><span data-stu-id="95516-710">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="95516-711">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-711">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-712">Name</span><span class="sxs-lookup"><span data-stu-id="95516-712">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-713">Задает уникальное имя для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-713">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-714">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-714">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-715">Дополнительные сведения можно найти в разделе <a href="#name" data-raw-source="[Name](#name)"> Name (имя) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-715">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-716">ID</span><span class="sxs-lookup"><span data-stu-id="95516-716">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-717">Заполнение уникального идентификатора для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-717">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-718">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="95516-718">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="95516-719">Дополнительные сведения можно найти в разделе <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-719">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-720">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-720">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-721">Необязательное описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-721">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-722">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="95516-722">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-723">Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-723">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-724">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="95516-724">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-725">Необязательное описание шаблона, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-725">An optional template description localized by a language locale.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-726">Версия</span><span class="sxs-lookup"><span data-stu-id="95516-726">Version</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-727">Определяет версию шаблона расположения параметров для администрирования отслеживания изменений.</span><span class="sxs-lookup"><span data-stu-id="95516-727">Identifies the version of the settings location template for administrative tracking of changes.</span></span> <span data-ttu-id="95516-728">Дополнительные сведения можно найти в разделе <a href="#version" data-raw-source="[Version](#version)"> Version (версия) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-728">For more information, see <a href="#version" data-raw-source="[Version](#version)">Version</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-729">DeferToMSAccount</span><span class="sxs-lookup"><span data-stu-id="95516-729">DeferToMSAccount</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-730">Определяет, включен ли этот шаблон в сочетании с учетной записью Майкрософт или нет.</span><span class="sxs-lookup"><span data-stu-id="95516-730">Controls whether this template is enabled in conjunction with a Microsoft account or not.</span></span> <span data-ttu-id="95516-731">Если для пользователя на компьютере включена синхронизация MSA, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-731">If MSA syncing is enabled for a user on a machine, then this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-732">DeferToOffice365</span><span class="sxs-lookup"><span data-stu-id="95516-732">DeferToOffice365</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-733">Так же, как и MSA, это определяет, включен ли этот шаблон в сочетании с Office365.</span><span class="sxs-lookup"><span data-stu-id="95516-733">Similar to MSA, this controls whether this template is enabled in conjunction with Office365.</span></span> <span data-ttu-id="95516-734">Если для синхронизации параметров используется Office 365, этот шаблон будет автоматически отключен.</span><span class="sxs-lookup"><span data-stu-id="95516-734">If Office 365 is being used to sync settings, this template will automatically be disabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-735">Параметры</span><span class="sxs-lookup"><span data-stu-id="95516-735">Settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-736">Контейнер для всех параметров, которые применяются к определенному шаблону.</span><span class="sxs-lookup"><span data-stu-id="95516-736">A container for all the settings that apply to a particular template.</span></span> <span data-ttu-id="95516-737">Она включает в себя экземпляры параметров реестра, файлов, SystemParameter и CustomAction.</span><span class="sxs-lookup"><span data-stu-id="95516-737">It contains instances of the Registry, File, SystemParameter, and CustomAction settings.</span></span> <span data-ttu-id="95516-738">Дополнительные сведения можно найти <strong> в разделе </strong> Параметры <a href="#data" data-raw-source="[Data types](#data)"> типов данных </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-738">For more information, see <strong>Settings</strong> in <a href="#data" data-raw-source="[Data types](#data)">Data types</a>.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a><span data-ttu-id="95516-739">Элемент SettingsLocationTemplate</span><span class="sxs-lookup"><span data-stu-id="95516-739">SettingsLocationTemplate Element</span></span>

<span data-ttu-id="95516-740">Этот элемент определяет параметры отдельного приложения или набора приложений.</span><span class="sxs-lookup"><span data-stu-id="95516-740">This element defines the settings for a single application or a suite of applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="95516-741">Поле/Тип</span><span class="sxs-lookup"><span data-stu-id="95516-741">Field/Type</span></span></th>
<th align="left"><span data-ttu-id="95516-742">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-742">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-743">Name</span><span class="sxs-lookup"><span data-stu-id="95516-743">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-744">Задает уникальное имя для шаблона расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="95516-744">Specifies a unique name for the settings location template.</span></span> <span data-ttu-id="95516-745">Этот элемент используется для отображения в целях создания ссылки на шаблон в WMI, PowerShell, просмотре событий и журналах отладки.</span><span class="sxs-lookup"><span data-stu-id="95516-745">This is used for display purposes when referencing the template in WMI, PowerShell, Event Viewer and debug logs.</span></span> <span data-ttu-id="95516-746">Дополнительные сведения можно найти в разделе <a href="#name" data-raw-source="[Name](#name)"> Name (имя) </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-746">For more information, see <a href="#name" data-raw-source="[Name](#name)">Name</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-747">ID</span><span class="sxs-lookup"><span data-stu-id="95516-747">ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-748">Заполнение уникального идентификатора для определенного шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-748">Populates a unique identifier for a particular template.</span></span> <span data-ttu-id="95516-749">Этот тег становится основным идентификатором, который агент UE-V использует для ссылки на шаблон во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="95516-749">This tag becomes the primary identifier that the UE-V Agent uses to reference the template at runtime.</span></span> <span data-ttu-id="95516-750">Дополнительные сведения можно найти в разделе <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</span><span class="sxs-lookup"><span data-stu-id="95516-750">For more information, see <a href="#id" data-raw-source="[ID](#id)">ID</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-751">Описание</span><span class="sxs-lookup"><span data-stu-id="95516-751">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-752">Необязательное описание шаблона.</span><span class="sxs-lookup"><span data-stu-id="95516-752">An optional description of the template.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="95516-753">LocalizedNames</span><span class="sxs-lookup"><span data-stu-id="95516-753">LocalizedNames</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-754">Необязательное имя, отображаемое в пользовательском интерфейсе, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-754">An optional name displayed in the UI, localized by a language locale.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="95516-755">LocalizedDescriptions</span><span class="sxs-lookup"><span data-stu-id="95516-755">LocalizedDescriptions</span></span></p></td>
<td align="left"><p><span data-ttu-id="95516-756">Необязательное описание шаблона, локализованное на языковой стандарт.</span><span class="sxs-lookup"><span data-stu-id="95516-756">An optional template description localized by a language locale.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a><span data-ttu-id="95516-757">Приложение: SettingsLocationTemplate. xsd</span><span class="sxs-lookup"><span data-stu-id="95516-757">Appendix: SettingsLocationTemplate.xsd</span></span>

<span data-ttu-id="95516-758">Ниже приведен пример файла SettingsLocationTemplate. xsd, в котором показаны элементы, дочерние элементы, атрибуты и параметры.</span><span class="sxs-lookup"><span data-stu-id="95516-758">Here is the SettingsLocationTemplate.xsd file showing its elements, child elements, attributes, and parameters:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## <span data-ttu-id="95516-759">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="95516-759">Related topics</span></span>


[<span data-ttu-id="95516-760">Работа с пользовательскими шаблонами UE-V 2. x и генератором UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="95516-760">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[<span data-ttu-id="95516-761">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="95516-761">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





