---
title: Запуск локально установленного приложения в виртуальной среде с виртуализированными приложениями
description: Запуск локально установленного приложения в виртуальной среде с виртуализированными приложениями
author: dansimp
ms.assetid: a8affa46-f1f7-416c-8125-9595cfbfdbc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 10c0f3f3c8a1b88cf1a98fd64fe8f7f49b597a91
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813312"
---
# <span data-ttu-id="a4786-103">Запуск локально установленного приложения в виртуальной среде с виртуализированными приложениями</span><span class="sxs-lookup"><span data-stu-id="a4786-103">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</span></span>


<span data-ttu-id="a4786-104">Локально установленное приложение можно запускать в виртуальной среде вместе с приложениями, которые были виртуализированы с помощью Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a4786-104">You can run a locally installed application in a virtual environment, alongside applications that have been virtualized by using Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="a4786-105">Это может потребоваться, если:</span><span class="sxs-lookup"><span data-stu-id="a4786-105">You might want to do this if you:</span></span>

-   <span data-ttu-id="a4786-106">Вы хотите установить и запустить приложение локально на клиентских компьютерах, но вы хотите виртуализировать и запустить специальные подключаемые модули, которые работают с этим локальным приложением.</span><span class="sxs-lookup"><span data-stu-id="a4786-106">Want to install and run an application locally on client computers, but want to virtualize and run specific plug-ins that work with that local application.</span></span>

-   <span data-ttu-id="a4786-107">Устранены неполадки с пакетом клиента App-V и нужно открыть локальное приложение в виртуальной среде App-V.</span><span class="sxs-lookup"><span data-stu-id="a4786-107">Are troubleshooting an App-V client package and want to open a local application within the App-V virtual environment.</span></span>

<span data-ttu-id="a4786-108">Используйте один из следующих методов, чтобы открыть локальное приложение в виртуальной среде App-V:</span><span class="sxs-lookup"><span data-stu-id="a4786-108">Use any of the following methods to open a local application inside the App-V virtual environment:</span></span>

-   [<span data-ttu-id="a4786-109">Раздел реестра RunVirtual</span><span class="sxs-lookup"><span data-stu-id="a4786-109">RunVirtual registry key</span></span>](#bkmk-runvirtual-regkey)

-   [<span data-ttu-id="a4786-110">Командлет PowerShell Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="a4786-110">Get-AppvClientPackage PowerShell cmdlet</span></span>](#bkmk-get-appvclientpackage-posh)

-   [<span data-ttu-id="a4786-111">Параметр командной строки/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="a4786-111">Command line switch /appvpid:&lt;PID&gt;</span></span>](#bkmk-cl-switch-appvpid)

-   [<span data-ttu-id="a4786-112">/Appvve переключателя командной строки: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="a4786-112">Command line hook switch /appvve:&lt;GUID&gt;</span></span>](#bkmk-cl-hook-switch-appvve)

<span data-ttu-id="a4786-113">Каждый метод выполняется по сути одной задачи, но некоторые из них могут быть более подходящими для некоторых приложений, чем другие, в зависимости от того, выполняется ли уже виртуализированное приложение.</span><span class="sxs-lookup"><span data-stu-id="a4786-113">Each method accomplishes essentially the same task, but some methods may be better suited for some applications than others, depending on whether the virtualized application is already running.</span></span>

## <a href="" id="bkmk-runvirtual-regkey"></a><span data-ttu-id="a4786-114">Раздел реестра RunVirtual</span><span class="sxs-lookup"><span data-stu-id="a4786-114">RunVirtual registry key</span></span>


<span data-ttu-id="a4786-115">Чтобы добавить локально установленное приложение в пакет или в виртуальную среду для группы подключения, добавьте подраздел в раздел `RunVirtual` реестра в редакторе реестра, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="a4786-115">To add a locally installed application to a package or to a connection group’s virtual environment, you add a subkey to the `RunVirtual` registry key in the Registry Editor, as described in the following sections.</span></span>

<span data-ttu-id="a4786-116">Для управления этим разделом реестра не доступен параметр групповой политики, поэтому необходимо использовать System Center Configuration Manager или другую электронную рассылку программного обеспечения или изменить реестр вручную.</span><span class="sxs-lookup"><span data-stu-id="a4786-116">There is no Group Policy setting available to manage this registry key, so you have to use System Center Configuration Manager or another electronic software distribution (ESD) system, or manually edit the registry.</span></span>

### <a href="" id="bkmk-"></a><span data-ttu-id="a4786-117">Поддерживаемые методы публикации пакетов при использовании RunVirtual</span><span class="sxs-lookup"><span data-stu-id="a4786-117">Supported methods of publishing packages when using RunVirtual</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a4786-118">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="a4786-118">App-V version</span></span></th>
<th align="left"><span data-ttu-id="a4786-119">Поддерживаемые методы публикации</span><span class="sxs-lookup"><span data-stu-id="a4786-119">Supported publishing methods</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a4786-120">App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="a4786-120">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4786-121">Опубликовано глобально или для пользователей</span><span class="sxs-lookup"><span data-stu-id="a4786-121">Published globally or to the user</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a4786-122">App-V 5,0 – App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="a4786-122">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="a4786-123">Опубликовано глобально</span><span class="sxs-lookup"><span data-stu-id="a4786-123">Published globally only</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a4786-124">Действия по созданию подраздела</span><span class="sxs-lookup"><span data-stu-id="a4786-124">Steps to create the subkey</span></span>

1.  <span data-ttu-id="a4786-125">Используя сведения из приведенной ниже таблицы, создайте новый раздел реестра, используя имя исполняемого файла, например **MyApp.exe**.</span><span class="sxs-lookup"><span data-stu-id="a4786-125">Using the information in the following table, create a new registry key using the name of the executable file, for example, **MyApp.exe**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="a4786-126">Метод публикации пакета</span><span class="sxs-lookup"><span data-stu-id="a4786-126">Package publishing method</span></span></th>
    <th align="left"><span data-ttu-id="a4786-127">Создание раздела реестра</span><span class="sxs-lookup"><span data-stu-id="a4786-127">Where to create the registry key</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a4786-128">Опубликовано глобально</span><span class="sxs-lookup"><span data-stu-id="a4786-128">Published globally</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a4786-129">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="a4786-129">HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="a4786-130">Пример </strong> : HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="a4786-130">Example</strong>: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a4786-131">Опубликовано для пользователя</span><span class="sxs-lookup"><span data-stu-id="a4786-131">Published to the user</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a4786-132">HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual</span><span class="sxs-lookup"><span data-stu-id="a4786-132">HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</span></span></p>
    <p><strong><span data-ttu-id="a4786-133">Пример </strong> : HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="a4786-133">Example</strong>: HKEY_CURRENT_USER \SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a4786-134">Группа подключения может содержать:</span><span class="sxs-lookup"><span data-stu-id="a4786-134">Connection group can contain:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="a4786-135">Пакеты, публикуемые только глобально или только для пользователей</span><span class="sxs-lookup"><span data-stu-id="a4786-135">Packages that are published just globally or just to the user</span></span></p></li>
    <li><p><span data-ttu-id="a4786-136">Пакеты, опубликованные глобально и для пользователей</span><span class="sxs-lookup"><span data-stu-id="a4786-136">Packages that are published globally and to the user</span></span></p></li>
    </ul></td>
    <td align="left"><p><span data-ttu-id="a4786-137">HKEY_LOCAL_MACHINE или HKEY_CURRENT_USER Key, но все перечисленные ниже условия должны быть истинными.</span><span class="sxs-lookup"><span data-stu-id="a4786-137">Either HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER key, but all of the following must be true:</span></span></p>
    <ul>
    <li><p><span data-ttu-id="a4786-138">Если вы хотите включить в виртуальную среду несколько пакетов, необходимо включить их в группу разрешенных подключений.</span><span class="sxs-lookup"><span data-stu-id="a4786-138">If you want to include multiple packages in the virtual environment, you must include them in an enabled connection group.</span></span></p></li>
    <li><p><span data-ttu-id="a4786-139">Создайте только один подраздел для одного из пакетов в группе подключение.</span><span class="sxs-lookup"><span data-stu-id="a4786-139">Create only one subkey for one of the packages in the connection group.</span></span> <span data-ttu-id="a4786-140">Например, если у вас есть один пакет, который опубликован глобально, и другой пакет, опубликованный для пользователя, вы можете создать подраздел для любого из этих пакетов, но не оба.</span><span class="sxs-lookup"><span data-stu-id="a4786-140">If, for example, you have one package that is published globally, and another package that is published to the user, you create a subkey for either of these packages, but not both.</span></span> <span data-ttu-id="a4786-141">Несмотря на то, что вы создаете подраздел только для одного из пакетов, все пакеты в группе подключения и локальное приложение будут доступны в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="a4786-141">Although you create a subkey for only one of the packages, all of the packages in the connection group, plus the local application, will be available in the virtual environment.</span></span></p></li>
    <li><p><span data-ttu-id="a4786-142">Ключ, под которым создается подраздел, должен соответствовать методу публикации, который вы использовали для пакета.</span><span class="sxs-lookup"><span data-stu-id="a4786-142">The key under which you create the subkey must match the publishing method you used for the package.</span></span></p>
    <p><span data-ttu-id="a4786-143">Например, если вы опубликовали пакет для пользователя, вы должны создать подраздел в разделе <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code> .</span><span class="sxs-lookup"><span data-stu-id="a4786-143">For example, if you published the package to the user, you must create the subkey under <code>HKEY_CURRENT_USER\SOFTWARE\Microsoft\AppV\Client\RunVirtual</code>.</span></span></p></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

     

2.  <span data-ttu-id="a4786-144">Задайте для нового раздела реестра значение PackageId и VersionId пакета, отделив значения с помощью подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="a4786-144">Set the new registry subkey’s value to the PackageId and VersionId of the package, separating the values with an underscore.</span></span>

    <span data-ttu-id="a4786-145">**Синтаксис**: &lt; PackageId &gt; \ _ &lt; VersionId&gt;</span><span class="sxs-lookup"><span data-stu-id="a4786-145">**Syntax**: &lt;PackageId&gt;\_&lt;VersionId&gt;</span></span>

    <span data-ttu-id="a4786-146">**Пример**: 4c909996-afc9-4352-b606-0b74542a09c1 \ _Be463724-Oct1-48f1-8604-c4bd7ca92fa</span><span class="sxs-lookup"><span data-stu-id="a4786-146">**Example**: 4c909996-afc9-4352-b606-0b74542a09c1\_be463724-Oct1-48f1-8604-c4bd7ca92fa</span></span>

    <span data-ttu-id="a4786-147">Приложение в предыдущем примере создаст файл экспорта реестра (REG-файл), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a4786-147">The application in the previous example would produce a registry export file (.reg file) like the following:</span></span>

    ``` syntax
    Windows Registry Editor Version 5.00 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual] 
    @="" 
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\AppV\Client\RunVirtual\MyApp.exe] 
    @="aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-555555555
    ```

## <a href="" id="bkmk-get-appvclientpackage-posh"></a><span data-ttu-id="a4786-148">Командлет PowerShell Get-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="a4786-148">Get-AppvClientPackage PowerShell cmdlet</span></span>


<span data-ttu-id="a4786-149">С помощью командлета **Start-AppVVirtualProcess** можно получить имя пакета, а затем запустить процесс в виртуальной среде указанного пакета.</span><span class="sxs-lookup"><span data-stu-id="a4786-149">You can use the **Start-AppVVirtualProcess** cmdlet to retrieve the package name and then start a process within the specified package's virtual environment.</span></span> <span data-ttu-id="a4786-150">Этот метод позволяет запускать любую команду в контексте пакета App-V, независимо от того, выполняется ли в данный момент пакет.</span><span class="sxs-lookup"><span data-stu-id="a4786-150">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>

<span data-ttu-id="a4786-151">Используйте приведенный ниже пример синтаксиса и подставьте имя пакета для \*\* &lt; пакета &gt; \*\*:</span><span class="sxs-lookup"><span data-stu-id="a4786-151">Use the following example syntax, and substitute the name of your package for **&lt;Package&gt;**:</span></span>

`$AppVName = Get-AppvClientPackage <Package>`

`Start-AppvVirtualProcess -AppvClientObject $AppVName cmd.exe`

<span data-ttu-id="a4786-152">Если вы не знаете точное имя пакета, вы можете использовать командную строку **Get-AppvClientPackage \ \* executable\\** <em> , где \*\* </em> Executable\* — это имя приложения, например: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="a4786-152">If you don’t know the exact name of your package, you can use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

## <a href="" id="bkmk-cl-switch-appvpid"></a><span data-ttu-id="a4786-153">Параметр командной строки/appvpid: &lt; PID&gt;</span><span class="sxs-lookup"><span data-stu-id="a4786-153">Command line switch /appvpid:&lt;PID&gt;</span></span>


<span data-ttu-id="a4786-154">Вы можете применить к любой команде параметр \*\*/appvpid: &lt; PID &gt; \*\* , который позволяет выполнить эту команду в виртуальном процессе, который вы выбираете, УКАЗАВ его идентификатор (PID).</span><span class="sxs-lookup"><span data-stu-id="a4786-154">You can apply the **/appvpid:&lt;PID&gt;** switch to any command, which enables that command to run within a virtual process that you select by specifying its process ID (PID).</span></span> <span data-ttu-id="a4786-155">При использовании этого метода запускается новый исполняемый файл в той же среде App-V, что и уже запущенный исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="a4786-155">Using this method launches the new executable in the same App-V environment as an executable that is already running.</span></span>

<span data-ttu-id="a4786-156">Пример.</span><span class="sxs-lookup"><span data-stu-id="a4786-156">Example:</span></span> `cmd.exe /appvpid:8108`

<span data-ttu-id="a4786-157">Чтобы найти идентификатор процесса (PID) своего процесса App-V, выполните команду **tasklist.exe** из командной строки с повышенными привилегиями.</span><span class="sxs-lookup"><span data-stu-id="a4786-157">To find the process ID (PID) of your App-V process, run the command **tasklist.exe** from an elevated command prompt.</span></span>

## <a href="" id="bkmk-cl-hook-switch-appvve"></a><span data-ttu-id="a4786-158">/Appvve переключателя командной строки: &lt; GUID&gt;</span><span class="sxs-lookup"><span data-stu-id="a4786-158">Command line hook switch /appvve:&lt;GUID&gt;</span></span>


<span data-ttu-id="a4786-159">С помощью этого переключателя вы можете выполнить локальную команду в виртуальной среде пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="a4786-159">This switch lets you run a local command within the virtual environment of an App-V package.</span></span> <span data-ttu-id="a4786-160">В отличие от ключа **/appvid** , где виртуальная среда должна быть уже запущена, этот параметр позволяет запустить виртуальную среду.</span><span class="sxs-lookup"><span data-stu-id="a4786-160">Unlike the **/appvid** switch, where the virtual environment must already be running, this switch enables you to start the virtual environment.</span></span>

<span data-ttu-id="a4786-161">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4786-161">Syntax:</span></span> `cmd.exe /appvve:<PACKAGEGUID_VERSIONGUID>`

<span data-ttu-id="a4786-162">Пример.</span><span class="sxs-lookup"><span data-stu-id="a4786-162">Example:</span></span> `cmd.exe /appvve:aaaaaaaa-bbbb-cccc-dddd-eeeeeeee_11111111-2222-3333-4444-55555555`

<span data-ttu-id="a4786-163">Чтобы получить GUID пакета и идентификатор GUID версии вашего приложения, выполните командлет **Get-AppvClientPackage** .</span><span class="sxs-lookup"><span data-stu-id="a4786-163">To get the package GUID and version GUID of your application, run the **Get-AppvClientPackage** cmdlet.</span></span> <span data-ttu-id="a4786-164">Объедините переключатель **/appvve** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a4786-164">Concatenate the **/appvve** switch with the following:</span></span>

-   <span data-ttu-id="a4786-165">Двоеточие</span><span class="sxs-lookup"><span data-stu-id="a4786-165">A colon</span></span>

-   <span data-ttu-id="a4786-166">Идентификатор GUID пакета для нужного пакета</span><span class="sxs-lookup"><span data-stu-id="a4786-166">Package GUID of the desired package</span></span>

-   <span data-ttu-id="a4786-167">Подчеркивание</span><span class="sxs-lookup"><span data-stu-id="a4786-167">An underscore</span></span>

-   <span data-ttu-id="a4786-168">НОМЕР версии требуемого пакета</span><span class="sxs-lookup"><span data-stu-id="a4786-168">Version ID of the desired package</span></span>

<span data-ttu-id="a4786-169">Если вы не знаете точное имя пакета, используйте командную строку **Get-AppvClientPackage \ \* executable\\** <em> , где \*\* </em> Executable\* — это имя приложения, например: Get-AppvClientPackage \ \* Word \ \*.</span><span class="sxs-lookup"><span data-stu-id="a4786-169">If you don’t know the exact name of your package, use the command line **Get-AppvClientPackage \*executable\\**<em>, where \**executable</em>* is the name of the application, for example: Get-AppvClientPackage \*Word\*.</span></span>

<span data-ttu-id="a4786-170">Этот метод позволяет запускать любую команду в контексте пакета App-V, независимо от того, выполняется ли в данный момент пакет.</span><span class="sxs-lookup"><span data-stu-id="a4786-170">This method lets you launch any command within the context of an App-V package, regardless of whether the package is currently running.</span></span>






## <span data-ttu-id="a4786-171">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="a4786-171">Related topics</span></span>


[<span data-ttu-id="a4786-172">Технический справочник по App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a4786-172">Technical Reference for App-V 5.0</span></span>](technical-reference-for-app-v-50.md)

 

 





