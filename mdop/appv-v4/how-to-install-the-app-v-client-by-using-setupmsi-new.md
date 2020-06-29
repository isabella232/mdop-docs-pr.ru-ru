---
title: Установка клиента App-V с помощью Setup.msi
description: Установка клиента App-V с помощью Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817332"
---
# <span data-ttu-id="d496e-103">Установка клиента App-V с помощью Setup.msi</span><span class="sxs-lookup"><span data-stu-id="d496e-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="d496e-104">В этой статье описано, как установить клиент App-V с помощью программы setup.msi.</span><span class="sxs-lookup"><span data-stu-id="d496e-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="d496e-105">Прежде чем устанавливать клиент App-V с помощью программы setup.msi, необходимо сначала определить, нужно ли установить какое-либо необходимое программное обеспечение, а затем установить его.</span><span class="sxs-lookup"><span data-stu-id="d496e-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="d496e-106">Чтобы установить необходимое программное обеспечение, ознакомьтесь с разделом [Установка программного](#prereq-sw) обеспечения, необходимых для этого раздела.</span><span class="sxs-lookup"><span data-stu-id="d496e-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="d496e-107">Чтобы установить клиентское программное обеспечение, ознакомьтесь с разделом [Установка клиента App-V с помощью Setup.msi программы в](#msi-setup) этой статье.</span><span class="sxs-lookup"><span data-stu-id="d496e-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="d496e-108">Установка необходимого программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="d496e-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="d496e-109">Чтобы установить необходимое программное обеспечение, можно воспользоваться приведенными ниже инструкциями.</span><span class="sxs-lookup"><span data-stu-id="d496e-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="d496e-110">Вы можете создать командный файл и выполнить команды из командной строки, а также с помощью языка сценариев, например VBScript или Windows PowerShell, для выполнения команд.</span><span class="sxs-lookup"><span data-stu-id="d496e-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="d496e-111">**Примечание**  Версии x86 следующего программного обеспечения необходимы для версий x86 и x64 клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="d496e-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="d496e-112">Установка распространяемого пакета Microsoft VisualC + + 2005SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="d496e-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="d496e-113">Скачайте пакет программного обеспечения для [пакета обновления Microsoft Visual C++ 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) из центра загрузки Майкрософт ( <https://go.microsoft.com/fwlink/?LinkId=119961> ).</span><span class="sxs-lookup"><span data-stu-id="d496e-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="d496e-114">\ [Значение маркера шаблона \] для версии 4,5 SP2 и более поздних версий клиента App-V Скачайте vcredist\_x86.exe с помощью [распространяемого пакета обновления безопасности ATL для Microsoft Visual C++ 2005](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [значение маркера шаблона])</span><span class="sxs-lookup"><span data-stu-id="d496e-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="d496e-115">Для автоматической установки используйте параметр командной строки "/Q" с vcredist\_x86.exe (например, **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="d496e-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="d496e-116">Чтобы установить программное обеспечение с помощью файла vcredist\_x86.msi, используйте параметр командной строки "/C/T: &lt; fullpathtofolder", &gt; чтобы извлечь файлы vcredist.msi и vcredis1.cab из vcredist\_x86.exe во временную папку.</span><span class="sxs-lookup"><span data-stu-id="d496e-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="d496e-117">Для автоматической установки используйте параметр командной строки/quiet (например, **msiexec/i vcredist.msi** /quiet.</span><span class="sxs-lookup"><span data-stu-id="d496e-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="d496e-118">Установка распространяемого пакета Microsoft VisualC + + 2008SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="d496e-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="d496e-119">**Важно!**  Для версии 4.6 и более поздних версий клиента App-V необходимо также установить обновление безопасности ATL для Microsoft Visual C++ 2008 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d496e-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="d496e-120">Скачайте [распространяемый пакет Microsoft Visual C++ 2008 с пакетом обновления 1 (SP1) для пакета обновления безопасности ATL](https://go.microsoft.com/fwlink/?LinkId=150700) из центра загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="d496e-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="d496e-121">Для автоматической установки используйте параметр командной строки "/Q" с vcredist\_x86.exe (например, **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="d496e-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="d496e-122">Установка Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="d496e-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="d496e-123">Скачайте пакет программного обеспечения [Microsoft Core XML Services (MSXML) 6.0 с пакетом обновления 1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) в центре загрузки Майкрософт ( https://go.microsoft.com/fwlink/?LinkId=63266) .</span><span class="sxs-lookup"><span data-stu-id="d496e-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="d496e-124">Для автоматической установки используйте параметр командной строки/quiet, например **msiexec/i msxml6\_x86.msi/quiet**.</span><span class="sxs-lookup"><span data-stu-id="d496e-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="d496e-125">Установка отчетов об ошибках в приложениях Microsoft</span><span class="sxs-lookup"><span data-stu-id="d496e-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="d496e-126">При установке отчетов об ошибках приложений Microsoft следует использовать параметр *APPGUID* для указания кода продукта App-V.</span><span class="sxs-lookup"><span data-stu-id="d496e-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="d496e-127">Код продукта уникален для каждого типа клиента App-V и версии.</span><span class="sxs-lookup"><span data-stu-id="d496e-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="d496e-128">Выберите правильный код продукта из приведенной ниже таблицы.</span><span class="sxs-lookup"><span data-stu-id="d496e-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="d496e-129">**Важно!**  Для App-V 4.6 SP2 и более поздних версий вам больше не нужно устанавливать отчеты об ошибках приложений Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="d496e-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="d496e-130">Теперь приложение App-V использует отчеты об ошибках Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d496e-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d496e-131">Версия</span><span class="sxs-lookup"><span data-stu-id="d496e-131">Version</span></span></th>
<th align="left"><span data-ttu-id="d496e-132">Код продукта для клиента для настольных систем</span><span class="sxs-lookup"><span data-stu-id="d496e-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="d496e-133">Код продукта для клиента служб удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="d496e-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d496e-134">App-V 4,5 CU1</span><span class="sxs-lookup"><span data-stu-id="d496e-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="d496e-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="d496e-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d496e-137">App-V 4,5 SP1</span><span class="sxs-lookup"><span data-stu-id="d496e-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="d496e-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="d496e-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d496e-140">App-V 4,5 SP2</span><span class="sxs-lookup"><span data-stu-id="d496e-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="d496e-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="d496e-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d496e-143">App-V 4,6 x86</span><span class="sxs-lookup"><span data-stu-id="d496e-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="d496e-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="d496e-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d496e-146">App-V 4,6 x64</span><span class="sxs-lookup"><span data-stu-id="d496e-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="d496e-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="d496e-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d496e-149">App-V 4,6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="d496e-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="d496e-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="d496e-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d496e-152">App-V 4,6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="d496e-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="d496e-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="d496e-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d496e-155">App-V 4,6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="d496e-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="d496e-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="d496e-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d496e-158">App-V 4,6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="d496e-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="d496e-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="d496e-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="d496e-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d496e-161">выпуск пакета App-V "Languages".</span><span class="sxs-lookup"><span data-stu-id="d496e-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="d496e-162">**Примечание**  Если вам нужно найти код продукта, можно воспользоваться редактором базы данных Orca.exe или аналогичным средством для проверки файлов установщика Windows, чтобы найти значение свойства *ProductCode* .</span><span class="sxs-lookup"><span data-stu-id="d496e-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="d496e-163">Дополнительные сведения об использовании Orca.exe можно найти в разделе [средства разработки установщика Windows](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="d496e-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="d496e-164">Найдите программу установки отчетов об ошибках приложений Microsoft, dw20shared.msi, которую можно найти в папке **Support\\Watson** на выпускаемом носителе.</span><span class="sxs-lookup"><span data-stu-id="d496e-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="d496e-165">Чтобы установить программное обеспечение, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d496e-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="d496e-166">Установка клиента App-V с помощью программы Setup.msi</span><span class="sxs-lookup"><span data-stu-id="d496e-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="d496e-167">Чтобы установить клиент App-V, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="d496e-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="d496e-168">Убедитесь, что установлены все необходимые программные компоненты.</span><span class="sxs-lookup"><span data-stu-id="d496e-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="d496e-169">\ [Значение маркера шаблона \] для версии 4.6 и более поздних версий клиента App-V программа setup.msi проверяет систему, а если необходимое программное обеспечение не установлено, генерирует сообщение об ошибке, указывающий на то, что установка не может быть продолжена.</span><span class="sxs-lookup"><span data-stu-id="d496e-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="d496e-170">\ [Значение маркера шаблона \]</span><span class="sxs-lookup"><span data-stu-id="d496e-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="d496e-171">Установка клиента Application Virtualization с помощью Setup.msi</span><span class="sxs-lookup"><span data-stu-id="d496e-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="d496e-172">Убедитесь в том, что вы вошли в систему под учетной записью, обладающей правами администратора на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d496e-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="d496e-173">Откройте окно командной строки с повышенными правами и измените каталог на папку, содержащую установочные файлы.</span><span class="sxs-lookup"><span data-stu-id="d496e-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="d496e-174">При установке версии 4.6 или более поздней версии клиента App-V необходимо использовать правильный установщик для операционной системы компьютера, 32-bit или 64-bit.</span><span class="sxs-lookup"><span data-stu-id="d496e-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="d496e-175">Установка завершится сбоем и появится сообщение об ошибке, если вы используете неправильный установщик.</span><span class="sxs-lookup"><span data-stu-id="d496e-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="d496e-176">Введите командную строку установки в командной строке.</span><span class="sxs-lookup"><span data-stu-id="d496e-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="d496e-177">Кроме того, вы можете создать командный файл и запустить его из командной строки.</span><span class="sxs-lookup"><span data-stu-id="d496e-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="d496e-178">Вы также можете использовать для выполнения команды язык сценариев, например VBScript или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d496e-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="d496e-179">В приведенном ниже примере кода показано, как setup.msi можно использовать с несколькими необязательными параметрами.</span><span class="sxs-lookup"><span data-stu-id="d496e-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="d496e-180">Дополнительные сведения об этих параметрах можно найти в разделе [Параметры командной строки установщика клиента Application Virtualization](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d496e-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="d496e-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "Production System" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "on" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application виртуализация" SWIFSDRIVE = "S",,/q</span><span class="sxs-lookup"><span data-stu-id="d496e-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="d496e-182">Важно.</span><span class="sxs-lookup"><span data-stu-id="d496e-182">Important</span></span>**  
    -   <span data-ttu-id="d496e-183">Для автоматической установки используется параметр установщика Windows "**/q**".</span><span class="sxs-lookup"><span data-stu-id="d496e-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="d496e-184">**%** Символу ""**% HomeDrive%**"должен предшествовать **^** знак" "".</span><span class="sxs-lookup"><span data-stu-id="d496e-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="d496e-185">В противном случае Командная оболочка Windows задает значение для пользователя, который выполняет установку.</span><span class="sxs-lookup"><span data-stu-id="d496e-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="d496e-186">Чтобы включить ведение журнала установки, воспользуйтесь переключателем msiexec **/l\ \* v имя_файла. log**.</span><span class="sxs-lookup"><span data-stu-id="d496e-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="d496e-187">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="d496e-187">Related topics</span></span>


[<span data-ttu-id="d496e-188">Установка клиента с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="d496e-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





