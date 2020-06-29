---
title: Сведения об App-V 5.0 с пакетом обновления 2 (SP2)
description: Сведения об App-V 5.0 с пакетом обновления 2 (SP2)
author: dansimp
ms.assetid: 16ca8452-cef2-464e-b4b5-c10d4630fa6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9a476f3bf273717b5a85a4244c5796f893b0c617
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814989"
---
# <span data-ttu-id="ee964-103">Сведения об App-V 5.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ee964-103">About App-V 5.0 SP2</span></span>


<span data-ttu-id="ee964-104">App-V 5.0 SP2 обеспечивает улучшенную интегрированную платформу, более гибкую виртуализацию и мощное управление виртуализованными приложениями.</span><span class="sxs-lookup"><span data-stu-id="ee964-104">App-V 5.0SP2 provides an improved integrated platform, more flexible virtualization, and powerful management for virtualized applications.</span></span> <span data-ttu-id="ee964-105">Дополнительные сведения можно найти в [обзоре App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=325265) ( https://go.microsoft.com/fwlink/?LinkId=325265) .</span><span class="sxs-lookup"><span data-stu-id="ee964-105">For more information see, [App-V 5.0 Overview](https://go.microsoft.com/fwlink/p/?LinkId=325265) (https://go.microsoft.com/fwlink/?LinkId=325265).</span></span>

## <span data-ttu-id="ee964-106">Изменения в стандартных функциях App-V 5.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ee964-106">Changes in Standard App-V 5.0SP2 Functionality</span></span>


<span data-ttu-id="ee964-107">В следующих разделах содержатся сведения об изменениях в стандартных функциях для App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="ee964-107">The following sections contain information about the changes in standard functionality for App-V 5.0SP2.</span></span>

### <a href="" id="bkmk-sp2-supported-cfg"></a><span data-ttu-id="ee964-108">Поддержка Windows Server 2012 R2 и Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="ee964-108">Support for Windows Server 2012 R2 and Windows 8.1</span></span>

<span data-ttu-id="ee964-109">Приложение App-V 5,0 включает поддержку для Windows Server 2012 R2 и Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="ee964-109">App-V 5.0 includes support for Windows Server 2012 R2 and Windows 8.1</span></span>

### <a href="" id="-------------app-v-5-0-sp2-now-supports-folder-redirection-for-the-user-s-roaming-appdata-directory"></a> <span data-ttu-id="ee964-110">Приложение App-V 5.0 SP2 теперь поддерживает перенаправление папок для перемещаемой папки AppData пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee964-110">App-V 5.0SP2 now supports folder redirection for the user’s roaming AppData directory</span></span>

<span data-ttu-id="ee964-111">App-V 5.0 SP2 поддерживает перемещаемую AppData (% AppData%) Перенаправление папок.</span><span class="sxs-lookup"><span data-stu-id="ee964-111">App-V 5.0SP2 supports roaming AppData (%AppData%) folder redirection.</span></span> <span data-ttu-id="ee964-112">Дополнительные сведения можно найти в разделе [планирование использования перенаправления папок с приложением App-V](planning-to-use-folder-redirection-with-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="ee964-112">For more information, see the [Planning to Use Folder Redirection with App-V](planning-to-use-folder-redirection-with-app-v.md).</span></span>

### <a href="" id="bkmk-pkg-upgr-pendg-tasks"></a><span data-ttu-id="ee964-113">Улучшенные возможности обновления пакетов и ожидающие задачи</span><span class="sxs-lookup"><span data-stu-id="ee964-113">Package upgrade improvements and pending tasks</span></span>

<span data-ttu-id="ee964-114">В App-V 5.0 SP2 больше не будет предлагаться закрыть запущенное виртуальное приложение при публикации более новой версии пакета или группы подключения.</span><span class="sxs-lookup"><span data-stu-id="ee964-114">In App-V 5.0SP2, you are no longer prompted to close a running virtual application when a newer version of the package or connection group is published.</span></span> <span data-ttu-id="ee964-115">Если при попытке выполнить связанную задачу используется пакет или группа соединения, появится сообщение, показывающее, что объект используется, и что операция будет выполнена позже.</span><span class="sxs-lookup"><span data-stu-id="ee964-115">If a package or connection group is in use when you try to perform a related task, a message displays to indicate that the object is in use, and that the operation will be attempted at a later time.</span></span>

<span data-ttu-id="ee964-116">Задачи, которые были помещены в состояние ожидания, выполняются в соответствии с приведенными ниже правилами.</span><span class="sxs-lookup"><span data-stu-id="ee964-116">Tasks that have been placed in a pending state will be performed according to the following rules:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee964-117">Тип задачи</span><span class="sxs-lookup"><span data-stu-id="ee964-117">Task type</span></span></th>
<th align="left"><span data-ttu-id="ee964-118">Применимое правило</span><span class="sxs-lookup"><span data-stu-id="ee964-118">Applicable rule</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee964-119">Пользовательская задача, например Публикация пакета для пользователя</span><span class="sxs-lookup"><span data-stu-id="ee964-119">User-based task, e.g., publishing a package to a user</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee964-120">Задача будет выполнена после того, как пользователь войдет в систему, а затем снова войдите в нее.</span><span class="sxs-lookup"><span data-stu-id="ee964-120">The pending task will be performed after the user logs off and then logs back on.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee964-121">Глобально на основе задач, например включение глобальной группы подключения</span><span class="sxs-lookup"><span data-stu-id="ee964-121">Globally based task, e.g., enabling a connection group globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee964-122">Задача, ожидающая выполнения, будет выполнена после отключения компьютера и повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="ee964-122">The pending task will be performed when the computer is shut down and then restarted.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ee964-123">Когда задача размещается в состоянии ожидания, клиент App-V также создает раздел реестра для задачи с отложенным вводом, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="ee964-123">When a task is placed in a pending state, the App-V client also generates a registry key for the pending task, as follows:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee964-124">Задача на основе пользователей или глобально</span><span class="sxs-lookup"><span data-stu-id="ee964-124">User-based or globally based task</span></span></th>
<th align="left"><span data-ttu-id="ee964-125">Где создается раздел реестра</span><span class="sxs-lookup"><span data-stu-id="ee964-125">Where the registry key is generated</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee964-126">Пользовательские задачи</span><span class="sxs-lookup"><span data-stu-id="ee964-126">User-based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee964-127">KEY_CURRENT_USER \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="ee964-127">KEY_CURRENT_USER\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee964-128">Глобально на основе задач</span><span class="sxs-lookup"><span data-stu-id="ee964-128">Globally based tasks</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee964-129">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\PendingTasks</span><span class="sxs-lookup"><span data-stu-id="ee964-129">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\PendingTasks</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ee964-130">Виртуализация Microsoft Office 2013 и Microsoft Office 2010 с помощью App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee964-130">Virtualizing Microsoft Office 2013 and Microsoft Office 2010 using App-V 5.0</span></span>

<span data-ttu-id="ee964-131">Ниже приведены ссылки на дополнительные сведения о приложениях App-V 5,0, которые поддерживаются в сценариях Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="ee964-131">Use the following link for more information about App-V 5.0 supported Microsoft Office scenarios.</span></span>

[<span data-ttu-id="ee964-132">Виртуализация Microsoft Office 2013 для Application Virtualization (App-V) 5.0</span><span class="sxs-lookup"><span data-stu-id="ee964-132">Virtualizing Microsoft Office 2013 for Application Virtualization (App-V) 5.0</span></span>](../solutions/virtualizing-microsoft-office-2013-for-application-virtualization--app-v--50-solutions.md)

<span data-ttu-id="ee964-133">**Примечание**  В этом документе рассматривается создание пакета Microsoft Office 2013 App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee964-133">**Note** This document focuses on creating a Microsoft Office 2013 App-V 5.0 Package.</span></span> <span data-ttu-id="ee964-134">Однако она также предоставляет сведения о сценариях для Microsoft Office 2010 с помощью App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee964-134">However, it also provides information about scenarios for Microsoft Office 2010 with App-V 5.0.</span></span>

 

### <a href="" id="-------------app-v-5-0-client-management-user-interface-application"></a> <span data-ttu-id="ee964-135">Приложение пользовательского интерфейса для управления клиентом App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee964-135">App-V 5.0 Client Management User Interface Application</span></span>

<span data-ttu-id="ee964-136">В предыдущих версиях App-V 5,0 пользовательским интерфейсом управления клиентами предоставлена установка клиента App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee964-136">In previous versions of App-V 5.0 the Client Management User Interface (UI) was provided with the App-V 5.0 Client installation.</span></span> <span data-ttu-id="ee964-137">С помощью App-V 5.0 SP2 это уже не так.</span><span class="sxs-lookup"><span data-stu-id="ee964-137">With App-V 5.0SP2 this is no longer the case.</span></span> <span data-ttu-id="ee964-138">Теперь у администраторов есть возможность развернуть клиентский интерфейс приложения App-V 5,0 в качестве виртуального приложения (с использованием всех поддерживаемых конфигураций развертывания App-V) или как установленное приложение.</span><span class="sxs-lookup"><span data-stu-id="ee964-138">Administrators now have the option to deploy the App-V 5.0 Client UI as a Virtual Application (using all supported App-V deployment configurations) or as an installed application.</span></span>

<span data-ttu-id="ee964-139">Дополнительные сведения см. в [приложении клиентского интерфейса клиента Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=386345) ( https://go.microsoft.com/fwlink/?LinkId=386345) .</span><span class="sxs-lookup"><span data-stu-id="ee964-139">For more information see [Microsoft Application Virtualization 5.0 Client UI Application](https://go.microsoft.com/fwlink/p/?LinkId=386345) (https://go.microsoft.com/fwlink/?LinkId=386345).</span></span>

### <span data-ttu-id="ee964-140">Одностороннее (SxS) сборка Автоматическая упаковка и развертывание</span><span class="sxs-lookup"><span data-stu-id="ee964-140">Side-by-Side (SxS) Assembly Automatic Packaging and Deployment</span></span>

<span data-ttu-id="ee964-141">Приложение App-V 5.0 с пакетом обновления 2 (SP2) теперь автоматически определяет параллельные сборки (SxS) и развертывание на компьютере с клиентским приложением App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="ee964-141">App-V 5.0SP2 now automatically detects side-by-side (SxS) assemblies, and deployment on the computer running the App-V 5.0SP2 client.</span></span> <span data-ttu-id="ee964-142">В основном сборка SxS включает в себя зависимости VC + + времени выполнения и MSXML.</span><span class="sxs-lookup"><span data-stu-id="ee964-142">A SxS assembly primarily consists of VC++ run-time dependencies or MSXML.</span></span> <span data-ttu-id="ee964-143">В предыдущих версиях App-V виртуальные приложения, которые применяют зависимости в среде VC, требовали, чтобы эти зависимости находились локально на компьютере с клиентским приложением App-V 5.0 SP2.</span><span class="sxs-lookup"><span data-stu-id="ee964-143">In previous versions of App-V, virtual applications that had dependencies on VC run-times required these dependencies to be locally on the computer running the App-V 5.0SP2 client.</span></span>

<span data-ttu-id="ee964-144">Теперь поддерживаются следующие функциональные возможности:</span><span class="sxs-lookup"><span data-stu-id="ee964-144">The following functionality is now supported:</span></span>

-   <span data-ttu-id="ee964-145">Программа Sequencer App-V 5,0 автоматически захватывает сборку SxS в пакете независимо от того, установлен ли на компьютере, на котором запущено на нем, тестовый запуск VC-среды.</span><span class="sxs-lookup"><span data-stu-id="ee964-145">The App-V 5.0 sequencer automatically captures the SxS assembly in the package regardless of whether the VC run-time has already been installed on the computer running the sequencer.</span></span>

-   <span data-ttu-id="ee964-146">Клиент App-V 5,0 автоматически устанавливает необходимую сборку SxS на компьютер, на котором работает клиент, как требуется во время публикации.</span><span class="sxs-lookup"><span data-stu-id="ee964-146">The App-V 5.0 client automatically installs the required SxS assembly to the computer running the client as required at publishing time.</span></span>

-   <span data-ttu-id="ee964-147">В приложении App-V 5,0 Sequencer выводится зависимость VC-времени выполнения, использующая механизм отчетов Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ee964-147">The App-V 5.0 sequencer reports the VC run-time dependency using the sequencer reporting mechanism.</span></span>

-   <span data-ttu-id="ee964-148">Приложение App-V 5,0 позволяет исключить зависимость времени выполнения VC в том случае, если зависимость уже доступна на компьютере, на котором запущен секвенсор.</span><span class="sxs-lookup"><span data-stu-id="ee964-148">The App-V 5.0 sequencer now allows you to exclude the VC run-time dependency in the event that the dependency is already available on the computer running the sequencer.</span></span>

### <span data-ttu-id="ee964-149">Улучшенные возможности обновления публикации</span><span class="sxs-lookup"><span data-stu-id="ee964-149">Publishing Refresh Improvements</span></span>

<span data-ttu-id="ee964-150">Приложение App-V 5,0 поддерживает несколько функций, позволяющих улучшить общее взаимодействие с обновлением набора приложений для определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee964-150">App-V 5.0 supports several features were added to improve the overall experience of refreshing a set of applications for a specific user.</span></span>

<span data-ttu-id="ee964-151">В списке ниже перечислены улучшения, повышающие качество обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="ee964-151">The following list displays the publishing refresh enhancements:</span></span>

<span data-ttu-id="ee964-152">В приведенном ниже списке содержатся дополнительные сведения о том, как включить новое улучшенное обновление публикации.</span><span class="sxs-lookup"><span data-stu-id="ee964-152">The following list contains more information about how to enable the new publishing refresh improvements.</span></span>

-   <span data-ttu-id="ee964-153">**EnablePublishingRefreshUI** — включает индикатор выполнения обновления публикации для компьютера, на котором запущен клиент App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee964-153">**EnablePublishingRefreshUI** - Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span>

-   <span data-ttu-id="ee964-154">**HideUI** — скрывает индикатор выполнения обновления публикации во время синхронизации вручную.</span><span class="sxs-lookup"><span data-stu-id="ee964-154">**HideUI** - Hides the publishing refresh progress bar during a manual sync.</span></span>

### <span data-ttu-id="ee964-155">Новый параметр конфигурации клиента</span><span class="sxs-lookup"><span data-stu-id="ee964-155">New Client Configuration Setting</span></span>

<span data-ttu-id="ee964-156">Ниже перечислены новые параметры конфигурации клиента, доступные в приложении App-V 5,0 с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="ee964-156">The following new client configuration setting is available with App-V 5.0 SP2:</span></span>

<span data-ttu-id="ee964-157">**EnableDynamicVirtualization** — включает поддерживаемые расширения оболочки, вспомогательные объекты браузера и элементы управления ActiveX, которые должны быть виртуализированы и выполнены с виртуальными приложениями.</span><span class="sxs-lookup"><span data-stu-id="ee964-157">**EnableDynamicVirtualization** - Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span>

<span data-ttu-id="ee964-158">Дополнительные сведения можно найти в разделе [Параметры конфигурации клиента](about-client-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ee964-158">For more information, see [About Client Configuration Settings](about-client-configuration-settings.md).</span></span>

### <a href="" id="-------------app-v-5-0-shell-extensions"></a> <span data-ttu-id="ee964-159">Расширения оболочки App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee964-159">App-V 5.0 Shell extensions</span></span>

<span data-ttu-id="ee964-160">Приложение App-V 5,0 с пакетом обновления 2 (SP2) теперь поддерживает расширения оболочки.</span><span class="sxs-lookup"><span data-stu-id="ee964-160">App-V 5.0 SP2 now supports shell extensions.</span></span>

<span data-ttu-id="ee964-161">Дополнительные сведения содержатся в разделе **Поддержка расширений оболочки App-v 5.0 SP2** для [создания виртуализованных приложений app-v 5,0 и управления ими](creating-and-managing-app-v-50-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ee964-161">For more information see the **App-V 5.0SP2 shell extension support** section of [Creating and Managing App-V 5.0 Virtualized Applications](creating-and-managing-app-v-50-virtualized-applications.md).</span></span>

## <a href="" id="---------app-v-5-0-documentation-updates"></a> <span data-ttu-id="ee964-162">Обновления документации для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee964-162">App-V 5.0 documentation updates</span></span>


<span data-ttu-id="ee964-163">Приложение App-V 5,0 SP2 содержит обновленную документацию по следующим сценариям.</span><span class="sxs-lookup"><span data-stu-id="ee964-163">App-V 5.0 SP2 provides updated documentation for the following scenarios:</span></span>

-   [<span data-ttu-id="ee964-164">Перенос из предыдущей версии</span><span class="sxs-lookup"><span data-stu-id="ee964-164">Migrating from a Previous Version</span></span>](migrating-from-a-previous-version-app-v-50.md)

-   [<span data-ttu-id="ee964-165">Сведения о App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ee964-165">About App-V 5.0</span></span>](about-app-v-50.md)

-   <span data-ttu-id="ee964-166">[Сведения об отчетах App-V 5,0](about-app-v-50-reporting.md) (раздел "часто задаваемые вопросы")</span><span class="sxs-lookup"><span data-stu-id="ee964-166">[About App-V 5.0 Reporting](about-app-v-50-reporting.md) (frequently asked questions section)</span></span>

## <span data-ttu-id="ee964-167">Получение технологий для MDOP</span><span class="sxs-lookup"><span data-stu-id="ee964-167">How to Get MDOP Technologies</span></span>


<span data-ttu-id="ee964-168">Приложение App-V 5,0 является частью пакета оптимизации рабочей среды Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="ee964-168">App-V 5.0 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="ee964-169">MDOP входит в состав Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="ee964-169">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="ee964-170">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в [статьях получение MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="ee964-170">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="ee964-171">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="ee964-171">Related topics</span></span>


[<span data-ttu-id="ee964-172">Заметки о выпуске для App-V 5.0 с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ee964-172">Release Notes for App-V 5.0 SP2</span></span>](release-notes-for-app-v-50-sp2.md)

 

 





