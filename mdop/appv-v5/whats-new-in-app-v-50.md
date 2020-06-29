---
title: Новые возможности в App-V 5.0
description: Новые возможности в App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813221"
---
# <span data-ttu-id="6e3f6-103">Новые возможности в App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6e3f6-103">What's New in App-V 5.0</span></span>


<span data-ttu-id="6e3f6-104">Этот раздел предназначен для пользователей, которые уже знакомы с приложением-V и хотят узнать, какие изменения были внесены в App-V 5,0, если вы еще не знакомы с приложением-V, вы должны ознакомиться с [планированием для App-v 5,0](planning-for-app-v-50-rc.md).</span><span class="sxs-lookup"><span data-stu-id="6e3f6-104">This section is for users who are already familiar with App-V and want to know what has changed in App-V 5.0 If you are not already familiar with App-V, you should start by reading [Planning for App-V 5.0](planning-for-app-v-50-rc.md).</span></span>

## <span data-ttu-id="6e3f6-105">Изменения в стандартных функциях</span><span class="sxs-lookup"><span data-stu-id="6e3f6-105">Changes in Standard Functionality</span></span>


<span data-ttu-id="6e3f6-106">В следующих разделах содержатся сведения об изменениях в стандартных функциях для App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-106">The following sections contain information about the changes in standard functionality for App-V 5.0.</span></span>

### <span data-ttu-id="6e3f6-107">Изменения, вносимые в Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="6e3f6-107">Changes to Supported Operating Systems</span></span>

<span data-ttu-id="6e3f6-108">Дополнительные сведения можно найти в разделе [Поддерживаемые конфигурации App-V 5,0](app-v-50-supported-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="6e3f6-108">For more information, see [App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md).</span></span>

## <span data-ttu-id="6e3f6-109">Изменения в секвенсоре</span><span class="sxs-lookup"><span data-stu-id="6e3f6-109">Changes to the sequencer</span></span>


<span data-ttu-id="6e3f6-110">В следующих разделах содержатся сведения об изменениях в секвенсоре App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-110">The following sections contain information about the changes in the App-V 5.0 sequencer.</span></span>

### <span data-ttu-id="6e3f6-111">Определенные изменения в секвенсоре</span><span class="sxs-lookup"><span data-stu-id="6e3f6-111">Specific change to the sequencer</span></span>

<span data-ttu-id="6e3f6-112">В следующей таблице представлены сведения о том, что изменилось с помощью секвенсора App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-112">The following table displays information about what has changed with the App-V 5.0 sequencer</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6e3f6-113">Функция Sequencer</span><span class="sxs-lookup"><span data-stu-id="6e3f6-113">Sequencer Feature</span></span></th>
<th align="left"><span data-ttu-id="6e3f6-114">Функция Sequencer App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6e3f6-114">App-V 5.0 Sequencer Functionality</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-115">Обработка после перезагрузки</span><span class="sxs-lookup"><span data-stu-id="6e3f6-115">Reboot processing</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-116">Когда приложение запрашивает перезагрузку, необходимо разрешить приложению перезапустить компьютер, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-116">When an application prompts for a restart, you should allow the application to restart the computer running the sequencer.</span></span> <span data-ttu-id="6e3f6-117">Компьютер, на котором работает программа Sequencer, перезагрузится, и секвенсор продолжит работу в режиме наблюдения.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-117">The computer running the sequencer will restart and the sequencer will resume in monitoring mode.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-118">Указание каталога виртуальных приложений</span><span class="sxs-lookup"><span data-stu-id="6e3f6-118">Specifying the virtual application directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-119">Виртуальный каталог приложений является обязательным параметром.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-119">Virtual Application Directory is a mandatory parameter.</span></span> <span data-ttu-id="6e3f6-120">Для достижения наилучших результатов он должен совпадать с каталогом установки установщика приложений.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-120">For best results, it should match the installation directory of the application installer.</span></span> <span data-ttu-id="6e3f6-121">Это приводит к более оптимальной производительности и совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-121">This results in more optimal performance and application compatibility.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-122">Редактирование сочетаний клавиш и FTAs</span><span class="sxs-lookup"><span data-stu-id="6e3f6-122">Editing shortcuts/FTAs</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-123"><strong>После завершения работы мастера упорядочивания страница "ярлыки и FTA" находится на странице "Расширенные возможности </strong> редактирования".</span><span class="sxs-lookup"><span data-stu-id="6e3f6-123">The Shortcuts/FTA page is on the <strong>Advanced</strong> editing page after the sequencing wizard has completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-124">Вкладка "Журнал изменений"</span><span class="sxs-lookup"><span data-stu-id="6e3f6-124">Change History Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-125">Вкладка "журнал изменений" была удалена для App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-125">The Change History tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-126">Вкладка "OSD"</span><span class="sxs-lookup"><span data-stu-id="6e3f6-126">OSD Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-127">Вкладка OSD была удалена для App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-127">The OSD tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-128">Вкладка "Виртуальные службы"</span><span class="sxs-lookup"><span data-stu-id="6e3f6-128">Virtual Services Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-129">Вкладка виртуальных служб была удалена для App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-129">The virtual services tab has been removed for App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-130">Вкладка "файлы и виртуальная файловая система"</span><span class="sxs-lookup"><span data-stu-id="6e3f6-130">Files/Virtual File System Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-131">Эти вкладки объединяются и позволяют изменять файлы пакетов.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-131">These tabs are combined and allow you to modify package files.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-132">Вкладка "Развертывание"</span><span class="sxs-lookup"><span data-stu-id="6e3f6-132">Deployment Tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-133">Больше нет параметров для настройки URL-адреса сервера в пакетах.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-133">There are no longer options to configure the server URL in the packages.</span></span> <span data-ttu-id="6e3f6-134">Этот параметр следует настроить сейчас с помощью конфигурации развертывания или сервера управления.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-134">You should configure this now using deployment configuration, or the management server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-135">Средство преобразователя пакетов</span><span class="sxs-lookup"><span data-stu-id="6e3f6-135">Package Converter Tool</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-136">С помощью PowerShell можно преобразовывать пакеты, созданные в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-136">You can now use PowerShell to convert packages created in previous versions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-137">Надстройка/промежуточный по</span><span class="sxs-lookup"><span data-stu-id="6e3f6-137">Add-on/Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-138">Вы можете развернуть родительские пакеты при упорядочении приложения для надстройки или промежуточного слоя.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-138">You can expand parent packages when you are sequencing an Add-On or Middleware application.</span></span> <span data-ttu-id="6e3f6-139">Надстройки и пакеты промежуточного программного обеспечения должны быть подключены с помощью групп подключений в App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-139">Add-ons and Middleware packages must be connected using connection groups in App-V 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-140">Вывод файлов</span><span class="sxs-lookup"><span data-stu-id="6e3f6-140">Files output</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-141">Следующие файлы создаются с помощью App-V 5,0, установщика Windows (MSI), AppV Configuration, конфигурации развертывания, конфигурации пользователя и Report.XML.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-141">The following files are created with App-V 5.0, Windows Installer (.msi), .appv, deployment configuration, user configuration, and the Report.XML.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-142">Дескрипторы сжатия и безопасности/пакеты MSI</span><span class="sxs-lookup"><span data-stu-id="6e3f6-142">Compression/Security descriptors/MSI packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-143">Сжатие и создание файла установщика Windows (MSI) выполняются автоматически для всех пакетов, и вы больше не сможете переопределять дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-143">Compression and the creation of a Windows Installer (.msi) file are automatic for all packages and you can no longer override security descriptors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-144">Сервис/параметры</span><span class="sxs-lookup"><span data-stu-id="6e3f6-144">Tools / Options</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-145">Окно диагностики удалено и еще несколько параметров.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-145">The Diagnostics window has been removed as well as several other settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-146">Установочный диск</span><span class="sxs-lookup"><span data-stu-id="6e3f6-146">Installation Drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-147">После установки приложения установочный диск больше не требуется.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-147">An installation drive is no longer required when you install an application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6e3f6-148">Потоковая передача OOS</span><span class="sxs-lookup"><span data-stu-id="6e3f6-148">OOS Streaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="6e3f6-149">Если оптимизация потока не выполнена, пакеты не помещаются в потоке, когда они запрашиваются компьютерами, на которых запущен клиент App-V 5,0, пока они не смогут запуститься.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-149">If no stream optimization is performed, packages are stream faulted when they are requested by computers running the App-V 5.0 client until they can launch.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6e3f6-150">Q: &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="6e3f6-150">Q:&lt;/p&gt;</span></span></td>
<td align="left"><p><span data-ttu-id="6e3f6-151">Приложение App-V 5,0 использует собственную файловую систему и больше не требует Q:.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-151">App-V 5.0 uses the native file system and no longer requires a Q:.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6e3f6-152">Обнаружение ошибок в последовательности</span><span class="sxs-lookup"><span data-stu-id="6e3f6-152">Sequencing error detection</span></span>


<span data-ttu-id="6e3f6-153">Программа Sequencer App-V 5,0 может определять распространенные проблемы, связанные с упорядочиванием, в процессе выполнения последовательности.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-153">The App-V 5.0 sequencer can detect common sequencing issues during sequencing.</span></span> <span data-ttu-id="6e3f6-154">На странице **отчета об установке** в конце мастера последовательностей отображаются диагностические сообщения, отнесенные на **ошибки**, **предупреждения**и **сведения** в зависимости от серьезности проблемы.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-154">The **Installation Report** page at the end of the sequencing wizard displays diagnostic messages categorized into **Errors**, **Warnings**, and **Info** depending on the severity of the issue.</span></span>

<span data-ttu-id="6e3f6-155">Чтобы просмотреть более подробные сведения о событии, дважды щелкните элемент, который вы хотите просмотреть в отчете.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-155">To display more detailed information about an event, double-click the item you want to review in the report.</span></span> <span data-ttu-id="6e3f6-156">Проблемы с упорядочиванием, а также предложения по устранению проблем отображаются.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-156">The sequencing issues, as well as suggestions about how to resolve the issues are displayed.</span></span> <span data-ttu-id="6e3f6-157">Сведения из системного отчета о подготовке системы и отчета об установке обрабатываются по завершении создания пакета.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-157">Information from the system preparation report and the installation report are summarized when you have finished creating a package.</span></span> <span data-ttu-id="6e3f6-158">Ниже перечислены типы проблем, которые можно просмотреть в отчете.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-158">The following list displays the types of issues available in the report:</span></span>

-   <span data-ttu-id="6e3f6-159">Исключенные файлы.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-159">Excluded files.</span></span>

-   <span data-ttu-id="6e3f6-160">Сведения о драйвере.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-160">Driver information.</span></span>

-   <span data-ttu-id="6e3f6-161">Различия в системе COM+.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-161">COM+ system differences.</span></span>

-   <span data-ttu-id="6e3f6-162">Конфликты параллельной (SxS) разрядом.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-162">Side-by-side (SxS) conflicts.</span></span>

-   <span data-ttu-id="6e3f6-163">Расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-163">Shell Extensions.</span></span>

-   <span data-ttu-id="6e3f6-164">Сведения о неподдерживаемых службах.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-164">Information about unsupported services.</span></span>

-   <span data-ttu-id="6e3f6-165">Настройка.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-165">DCOM.</span></span>

## <span data-ttu-id="6e3f6-166">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="6e3f6-166">Connection Groups</span></span>


<span data-ttu-id="6e3f6-167">Функция App-V, ранее известная как **композиция динамического набора** , теперь называется **группами подключений** в App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-167">The App-V feature formerly known as **Dynamic Suite Composition** is now referred to as **Connection Groups** in App-V 5.0.</span></span> <span data-ttu-id="6e3f6-168">Дополнительные сведения об использовании групп подключений можно найти в разделе [Управление группами подключений](managing-connection-groups.md).</span><span class="sxs-lookup"><span data-stu-id="6e3f6-168">For more information about using Connection Groups see [Managing Connection Groups](managing-connection-groups.md).</span></span>

## <span data-ttu-id="6e3f6-169">Функции лицензирования и оценки</span><span class="sxs-lookup"><span data-stu-id="6e3f6-169">Licensing and Metering Functionality</span></span>


<span data-ttu-id="6e3f6-170">Приложение и функция лицензирования удалены в App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-170">The application and licensing functionality has been removed in App-V 5.0.</span></span> <span data-ttu-id="6e3f6-171">Актуальные положения лицензий в вашей среде зависят от конкретного лицензионного соглашения и прав на использование, предоставленных условиями лицензии.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-171">The actual license positions in your environment depend on the specific software title license and usage rights granted by the associated license terms.</span></span>

## <span data-ttu-id="6e3f6-172">Кэш файлов и приложений</span><span class="sxs-lookup"><span data-stu-id="6e3f6-172">File and Application Cache</span></span>


<span data-ttu-id="6e3f6-173">В App-V 5,0 нет доступного файла или кэша приложений.</span><span class="sxs-lookup"><span data-stu-id="6e3f6-173">There is no file or application cache available with App-V 5.0.</span></span>






## <span data-ttu-id="6e3f6-174">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6e3f6-174">Related topics</span></span>


[<span data-ttu-id="6e3f6-175">Сведения о App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6e3f6-175">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





