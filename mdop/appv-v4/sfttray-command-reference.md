---
title: Описание команд SFTTRAY
description: Описание команд SFTTRAY
author: dansimp
ms.assetid: 6fa3a939-b047-4d6c-bd1d-dfb93e065eb2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a664b91ff7edd5f8536f035417cc3b0f52d7ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815352"
---
# <span data-ttu-id="c3be2-103">Описание команд SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="c3be2-103">SFTTRAY Command Reference</span></span>


<span data-ttu-id="c3be2-104">Приложение клиентской панели Microsoft Application Virtualization (App-V), sfttray.exe, — это основной элемент пользовательского интерфейса клиента App-V, с которым пользователи будут взаимодействовать при обычном использовании.</span><span class="sxs-lookup"><span data-stu-id="c3be2-104">The Microsoft Application Virtualization (App-V) Client Tray application, sfttray.exe, is the main user interface element of the App-V Client that users will interact with during normal use.</span></span> <span data-ttu-id="c3be2-105">Эта программа контролирует потоковую передачу и запуск всех виртуальных приложений и доступ к ним можно получить, щелкнув правой кнопкой мыши значок, который отображается в области уведомлений, чтобы отобразить меню клиентских функций.</span><span class="sxs-lookup"><span data-stu-id="c3be2-105">This program controls the streaming and starting of all virtual applications and is accessed by right-clicking the icon displayed in the notification area to display the menu of client functions.</span></span> <span data-ttu-id="c3be2-106">Это меню позволяет загрузить приложения, начать обновление публикации, отменить запрос или перевести клиент в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="c3be2-106">The menu enables the user to load applications, start a publishing refresh, cancel a request, or change the client to offline mode.</span></span> <span data-ttu-id="c3be2-107">Пользователь также может закрыть приложение клиентской панели приложения Application Virtualization и все активные приложения, нажав кнопку **выход**.</span><span class="sxs-lookup"><span data-stu-id="c3be2-107">The user can also close the Application Virtualization Client Tray application and all active applications by clicking **Exit**.</span></span>

<span data-ttu-id="c3be2-108">По умолчанию значок отображается каждый раз, когда запускается виртуальное приложение, несмотря на то что вы можете управлять этим поведением с помощью команд SFTTRAY.</span><span class="sxs-lookup"><span data-stu-id="c3be2-108">By default, the icon is displayed whenever a virtual application is started, although you can control this behavior by using SFTTRAY commands.</span></span> <span data-ttu-id="c3be2-109">Приложение клиентской панели Application Virtualization также отображает индикатор выполнения для каждого запускаемого приложения, а также сообщения о состоянии активных приложений.</span><span class="sxs-lookup"><span data-stu-id="c3be2-109">The Application Virtualization Client Tray application also displays a progress bar for each application that is started, as well as status messages about active applications.</span></span> <span data-ttu-id="c3be2-110">При нажатии на индикатор выполнения отображается сообщение, позволяющее отменить загрузку или запуск приложения.</span><span class="sxs-lookup"><span data-stu-id="c3be2-110">Clicking the progress bar displays a message that allows you to cancel the loading or starting of an application.</span></span>

## <span data-ttu-id="c3be2-111">Команды SFTTRAY</span><span class="sxs-lookup"><span data-stu-id="c3be2-111">SFTTRAY Commands</span></span>


<span data-ttu-id="c3be2-112">Список команд и переключателей командной строки можно отобразить, выполнив следующую команду в командном окне.</span><span class="sxs-lookup"><span data-stu-id="c3be2-112">The list of commands and command-line switches can be displayed by running the following command from a command window.</span></span>

**<span data-ttu-id="c3be2-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c3be2-113">Note</span></span>**  
<span data-ttu-id="c3be2-114">Для каждого контекста пользователя существует только один экземпляр Application Virtualization, поэтому при запуске новой команды SFTTRAY она будет передана в уже запущенную программу.</span><span class="sxs-lookup"><span data-stu-id="c3be2-114">There is only one Application Virtualization Client Tray instance for each user context, so if you start a new SFTTRAY command, it will be passed to the program that is already running.</span></span>



`Sfttray.exe /?`

### <span data-ttu-id="c3be2-115">Использование команд</span><span class="sxs-lookup"><span data-stu-id="c3be2-115">Command Usage</span></span>

`Sfttray.exe [/HIDE | /SHOW]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] [/EXE alternate-exe] /LAUNCH app [args]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOAD app [/SFTFILE sft]`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LOADALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /REFRESHALL`

`Sfttray.exe [/HIDE | /SHOW] [/QUIET] /LAUNCHRESULT <UNIQUE ID>  /LAUNCH app [args]`

`Sfttray.exe /EXIT`

### <span data-ttu-id="c3be2-116">Переключатели командной строки</span><span class="sxs-lookup"><span data-stu-id="c3be2-116">Command-Line Switches</span></span>

<span data-ttu-id="c3be2-117">Параметры командной строки SFTTRAY описаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c3be2-117">The SFTTRAY command-line switches are described in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c3be2-118">Переключатель</span><span class="sxs-lookup"><span data-stu-id="c3be2-118">Switch</span></span></th>
<th align="left"><span data-ttu-id="c3be2-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c3be2-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3be2-120">/HIDE</span><span class="sxs-lookup"><span data-stu-id="c3be2-120">/HIDE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-121">Скрывает значок SFTTRAY в области уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="c3be2-121">Hides the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3be2-122">/SHOW</span><span class="sxs-lookup"><span data-stu-id="c3be2-122">/SHOW</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-123">Отображение значка SFTTRAY в области уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="c3be2-123">Displays the SFTTRAY icon in the Windows notification area.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3be2-124">Параметрами</span><span class="sxs-lookup"><span data-stu-id="c3be2-124">/QUIET</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-125">Поддерживает автоматическое использование, предотвращая ошибки при отображении полей сообщений, требующих подтверждения пользователей.</span><span class="sxs-lookup"><span data-stu-id="c3be2-125">Supports unattended usage by preventing errors from displaying message boxes that require user acknowledgement.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3be2-126">/EXE &lt; альтернативный exe-файл&gt;</span><span class="sxs-lookup"><span data-stu-id="c3be2-126">/EXE &lt;alternate-exe&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-127">Используется с/LAUNCH, чтобы указать, что исполняемая программа должна запускаться в виртуальной среде при запуске виртуального приложения вместо целевого файла, указанного в OSD.</span><span class="sxs-lookup"><span data-stu-id="c3be2-127">Used with /LAUNCH to specify that an executable program is to be started in the virtual environment when a virtual application is started in place of the target file specified in the OSD.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3be2-128">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c3be2-128">Note</span></span></strong><br/><p><span data-ttu-id="c3be2-129">Например, с помощью команды "SFTTRAY.EXE/EXE REGEDIT.EXE &lt; приложение/Launch &gt; " можно просмотреть реестр виртуальной среды, в которой работает приложение.</span><span class="sxs-lookup"><span data-stu-id="c3be2-129">For example, use “SFTTRAY.EXE /EXE REGEDIT.EXE /LAUNCH &lt;app&gt;” to enable you to examine the registry of the virtual environment in which the application is running.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3be2-130">&lt;Приложение/Launch &gt; [ &lt; args &gt; ]</span><span class="sxs-lookup"><span data-stu-id="c3be2-130">/LAUNCH &lt;app&gt; [&lt;args&gt;]</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-131">Запускает виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="c3be2-131">Starts a virtual application.</span></span> <span data-ttu-id="c3be2-132">Укажите имя и версию приложения или путь к OSD – файлу.</span><span class="sxs-lookup"><span data-stu-id="c3be2-132">Specify the name and version of an application or the path to an OSD file.</span></span> <span data-ttu-id="c3be2-133">Кроме того, аргументы командной строки можно передать в виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="c3be2-133">Optionally, command-line arguments can be passed to the virtual application.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3be2-134">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c3be2-134">Note</span></span></strong><br/><p><span data-ttu-id="c3be2-135">Используйте команду "SFTMIME.EXE/QUERY OBJ: APP/SHORT", чтобы получить список имен и версий доступных виртуальных приложений.</span><span class="sxs-lookup"><span data-stu-id="c3be2-135">Use the command “SFTMIME.EXE /QUERY OBJ:APP /SHORT” to obtain a list of the names and versions of available virtual applications.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3be2-136">/LOAD</span><span class="sxs-lookup"><span data-stu-id="c3be2-136">/LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-137">Загружает или импортирует виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="c3be2-137">Loads or imports a virtual application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3be2-138">/LOADALL</span><span class="sxs-lookup"><span data-stu-id="c3be2-138">/LOADALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-139">Загружает все приложения в кэш.</span><span class="sxs-lookup"><span data-stu-id="c3be2-139">Loads all applications into cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3be2-140">/REFRESHALL</span><span class="sxs-lookup"><span data-stu-id="c3be2-140">/REFRESHALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-141">Запускает обновление публикации для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="c3be2-141">Starts a publishing refresh for all applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3be2-142">&lt;уникальный идентификатор/LAUNCHRESULT&gt;</span><span class="sxs-lookup"><span data-stu-id="c3be2-142">/LAUNCHRESULT &lt;UNIQUE ID&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-143">Возвращает код результата запуска для процесса, который запускается sfttray.exe с помощью глобального события и файла, отображенного в памяти, на основе указанного корневого имени для УНИКАЛЬного идентификатора. ¹</span><span class="sxs-lookup"><span data-stu-id="c3be2-143">Returns the launch result code to the process that launches sfttray.exe by using a global event and a memory mapped file that are based on the specified root name for the UNIQUE ID.¹</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3be2-144">/SFTFILE &lt; SFT&gt;</span><span class="sxs-lookup"><span data-stu-id="c3be2-144">/SFTFILE &lt;sft&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-145">Необязательный параметр, используемый с/LOAD, для указания пути к SFT-файлу приложения.</span><span class="sxs-lookup"><span data-stu-id="c3be2-145">Optional switch used with /LOAD to specify the path to the application’s SFT file.</span></span> <span data-ttu-id="c3be2-146">Если задано, приложение импортируется, а не загружается.</span><span class="sxs-lookup"><span data-stu-id="c3be2-146">If specified, the application is imported rather than loaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3be2-147">/EXIT</span><span class="sxs-lookup"><span data-stu-id="c3be2-147">/EXIT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3be2-148">Закрытие программы SFTTRAY и всех активных виртуальных приложений и удаление значка из области уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="c3be2-148">Closes the SFTTRAY program and all active virtual applications and removes the icon from the Windows notification area.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="c3be2-149">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c3be2-149">Note</span></span>**  
<span data-ttu-id="c3be2-150">¹ параметр командной строки */LAUNCHRESULT* предоставляет возможность для процесса, запускающего sfttray.exe, для указания корневого имени глобального события и отображенного в памяти файла, который используется для возврата кода результата запуска в процесс.</span><span class="sxs-lookup"><span data-stu-id="c3be2-150">¹ The */LAUNCHRESULT* command line parameter provides a means for the process that launches sfttray.exe to specify the root name for a global event and a memory mapped file that are used to return the launch result code to the process.</span></span> <span data-ttu-id="c3be2-151">Имя уникального идентификатора должно начинаться с "SFT-", чтобы не допустить, чтобы имя события изнутри, когда запускается процесс запуска в виртуальной среде.</span><span class="sxs-lookup"><span data-stu-id="c3be2-151">The unique identifier name should start with “SFT-” to prevent the event name from getting virtualized when the launching process is invoked within a virtual environment.</span></span> <span data-ttu-id="c3be2-152">Область сопоставленных в памяти размеров будет 64 бит.</span><span class="sxs-lookup"><span data-stu-id="c3be2-152">The memory mapped region will be 64 bits in size.</span></span>

<span data-ttu-id="c3be2-153">Чтобы использовать этот параметр, процесс запуска создает событие с именем " &lt; уникальный идентификатор &gt; -результат \ _Event", сопоставленный файл в памяти с именем "уникальный идентификатор — &lt; &gt; результат \ _Value", а также событие с именем " &lt; уникальный идентификатор &gt; — Завершение \" _Event ", а затем запускается процесс запуска sfttray.exe и ждет, пока событие не будет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="c3be2-153">To use this parameter, the launching process creates an event with the name “&lt;UNIQUE ID&gt;-result\_event”, a memory mapped file with the name “&lt;UNIQUE ID&gt;-result\_value”, and optionally an event with the name “&lt;UNIQUE ID&gt;-shutdown\_event”, and then the launching process launches sfttray.exe and waits on the event to be signaled.</span></span> <span data-ttu-id="c3be2-154">После того как событие " &lt; уникальный идентификатор &gt; — результат \ _Event" будет сигнальным, процесс запуска извлекает код возврата 64-bit из сопоставленной области памяти.</span><span class="sxs-lookup"><span data-stu-id="c3be2-154">After the event “&lt;UNIQUE ID&gt;-result\_event” is signaled, the launching process retrieves the 64-bit return code from the memory mapped region.</span></span>

<span data-ttu-id="c3be2-155">Если необязательное событие " &lt; уникальный идентификатор &gt; — Завершение" — "не_event", когда виртуальное приложение завершает работу, sfttray.exe открывает и сигнализирует о событии.</span><span class="sxs-lookup"><span data-stu-id="c3be2-155">If the optional event “&lt;UNIQUE ID&gt;-shutdown\_event” exists when the virtual application exits, sfttray.exe opens and signals the event.</span></span> <span data-ttu-id="c3be2-156">Процесс запуска ожидает на этом событии завершения работы, если ему нужно определить, когда завершается виртуальное приложение.</span><span class="sxs-lookup"><span data-stu-id="c3be2-156">The launching process waits on this shutdown event if it needs to determine when the virtual application exits.</span></span>











