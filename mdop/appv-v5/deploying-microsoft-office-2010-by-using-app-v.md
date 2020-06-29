---
title: Развертывание Microsoft Office 2010 с помощью App-V
description: Развертывание Microsoft Office 2010 с помощью App-V
author: dansimp
ms.assetid: 0a9e496e-82a1-4dc0-a496-7b21eaa00f53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 303a44d921e40a411a4c4ea4622f06a76b8ed9c6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814637"
---
# <span data-ttu-id="885ed-103">Развертывание Microsoft Office 2010 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="885ed-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="885ed-104">Пакеты Office 2010 для Application 5,0 Virtualization можно создать с помощью одного из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="885ed-104">You can create Office 2010 packages for Application Virtualization 5.0 using one of the following methods:</span></span>

-   <span data-ttu-id="885ed-105">Секвенсор Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="885ed-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="885ed-106">Ускоритель пакетов для Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="885ed-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="885ed-107">Поддержка App-V для Office 2010</span><span class="sxs-lookup"><span data-stu-id="885ed-107">App-V support for Office 2010</span></span>


<span data-ttu-id="885ed-108">В следующей таблице показаны версии App-V, методы создания пакетов Office, поддерживаемые лицензированные и поддерживаемые развертывания для Office 2010.</span><span class="sxs-lookup"><span data-stu-id="885ed-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="885ed-109">Поддерживаемый элемент</span><span class="sxs-lookup"><span data-stu-id="885ed-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="885ed-110">Уровень поддержки</span><span class="sxs-lookup"><span data-stu-id="885ed-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-111">Поддерживаемые версии App-V</span><span class="sxs-lookup"><span data-stu-id="885ed-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="885ed-112">4,6</span><span class="sxs-lookup"><span data-stu-id="885ed-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="885ed-113">5.0</span><span class="sxs-lookup"><span data-stu-id="885ed-113">5.0</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-114">Создание пакета</span><span class="sxs-lookup"><span data-stu-id="885ed-114">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="885ed-115">Последовательность</span><span class="sxs-lookup"><span data-stu-id="885ed-115">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="885ed-116">Ускоритель пакетов</span><span class="sxs-lookup"><span data-stu-id="885ed-116">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="885ed-117">Комплект средств для развертывания Office</span><span class="sxs-lookup"><span data-stu-id="885ed-117">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-118">Поддерживаемое лицензирование</span><span class="sxs-lookup"><span data-stu-id="885ed-118">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-119">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="885ed-119">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-120">Поддерживаемые развертывания</span><span class="sxs-lookup"><span data-stu-id="885ed-120">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="885ed-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="885ed-121">Desktop</span></span></p></li>
<li><p><span data-ttu-id="885ed-122">Персональный VDI</span><span class="sxs-lookup"><span data-stu-id="885ed-122">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="885ed-123">СЛУЖБ</span><span class="sxs-lookup"><span data-stu-id="885ed-123">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="885ed-124">Создание Office 2010 App-V 5,0 с помощью секвенсора</span><span class="sxs-lookup"><span data-stu-id="885ed-124">Creating Office 2010 App-V 5.0 using the sequencer</span></span>


<span data-ttu-id="885ed-125">Виртуализация Office 2010 — это один из основных методов создания пакета Office 2010 на App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="885ed-125">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.0.</span></span> <span data-ttu-id="885ed-126">Корпорация Майкрософт предоставила подробный рецепт в статье базы знаний.</span><span class="sxs-lookup"><span data-stu-id="885ed-126">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="885ed-127">Чтобы создать пакет Office 2010 для App-V 5,0, ознакомьтесь с подробными инструкциями по следующей ссылке:</span><span class="sxs-lookup"><span data-stu-id="885ed-127">To create an Office 2010 package on App-V 5.0, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="885ed-128">Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="885ed-128">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="885ed-129">Создание пакетов Office 2010 App-V 5,0 с помощью ускорителей пакетов</span><span class="sxs-lookup"><span data-stu-id="885ed-129">Creating Office 2010 App-V 5.0 packages using package accelerators</span></span>


<span data-ttu-id="885ed-130">Пакеты Office 2010 App-V 5,0 можно создавать с помощью ускорителей пакетов.</span><span class="sxs-lookup"><span data-stu-id="885ed-130">Office 2010 App-V 5.0 packages can be created through package accelerators.</span></span> <span data-ttu-id="885ed-131">Корпорация Майкрософт предоставила ускорители пакетов для создания Office 2010 в Windows 8 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="885ed-131">Microsoft has provided package accelerators for creating Office 2010 on Windows 8 and Windows 7.</span></span> <span data-ttu-id="885ed-132">Чтобы создать пакеты Office 2010 в App-V с помощью ускорителей пакетов, просмотрите следующие страницы, чтобы получить доступ к соответствующему ускорительу пакетов:</span><span class="sxs-lookup"><span data-stu-id="885ed-132">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="885ed-133">Ускоритель пакетов для Office профессиональный плюс 2010 — Windows 8 (App-V 5,0)</span><span class="sxs-lookup"><span data-stu-id="885ed-133">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="885ed-134">Ускоритель пакетов для Office профессиональный плюс 2010 – Windows 7 (App-V 5,0)</span><span class="sxs-lookup"><span data-stu-id="885ed-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="885ed-135">Подробные инструкции по созданию пакетов виртуальных приложений с помощью ускорителей пакетов App-V можно найти в разделе [Создание виртуального пакета приложения с помощью ускорителя пакетов App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span><span class="sxs-lookup"><span data-stu-id="885ed-135">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md).</span></span>

## <span data-ttu-id="885ed-136">Развертывание пакета Microsoft Office для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="885ed-136">Deploying the Microsoft Office package for App-V 5.0</span></span>


<span data-ttu-id="885ed-137">Пакеты Office 2010 можно развертывать с помощью любого из указанных ниже методов развертывания App-V.</span><span class="sxs-lookup"><span data-stu-id="885ed-137">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="885ed-138">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="885ed-138">System Center Configuration Manager</span></span>

-   <span data-ttu-id="885ed-139">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="885ed-139">App-V server</span></span>

-   <span data-ttu-id="885ed-140">Самостоятельная работа с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="885ed-140">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="885ed-141">Управление пакетами и настройка в Office App-V</span><span class="sxs-lookup"><span data-stu-id="885ed-141">Office App-V package management and customization</span></span>


<span data-ttu-id="885ed-142">Пакеты Office 2010 могут управляться так же, как и любые другие пакеты App-V 5,0 с помощью стандартных механизмов управления пакетами.</span><span class="sxs-lookup"><span data-stu-id="885ed-142">Office 2010 packages can be managed like any other App-V 5.0 packages through known package management mechanisms.</span></span> <span data-ttu-id="885ed-143">Специальные инструкции не требуются, например, для добавления, публикации, отмены публикации и удаления пакетов Office.</span><span class="sxs-lookup"><span data-stu-id="885ed-143">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="885ed-144">Интеграция Microsoft Office с Windows</span><span class="sxs-lookup"><span data-stu-id="885ed-144">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="885ed-145">В таблице ниже приведен полный список поддерживаемых точек интеграции для Office 2010.</span><span class="sxs-lookup"><span data-stu-id="885ed-145">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="885ed-146">Точка расширения</span><span class="sxs-lookup"><span data-stu-id="885ed-146">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="885ed-147">Описание</span><span class="sxs-lookup"><span data-stu-id="885ed-147">Description</span></span></th>
<th align="left"><span data-ttu-id="885ed-148">Office 2010</span><span class="sxs-lookup"><span data-stu-id="885ed-148">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-149">Плагин присоединения к собранию Lync для Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="885ed-149">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-150">Пользователь может присоединиться к собраниям Lync из Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="885ed-150">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-151">Отправлено в драйвер печати OneNote</span><span class="sxs-lookup"><span data-stu-id="885ed-151">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-152">Пользователь может печатать в OneNote</span><span class="sxs-lookup"><span data-stu-id="885ed-152">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-153">Да</span><span class="sxs-lookup"><span data-stu-id="885ed-153">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-154">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="885ed-154">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-155">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="885ed-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-156">Надстройка "отправить в OneNote" в Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="885ed-156">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-157">Пользователь может отправлять сообщения в OneNote из браузера Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="885ed-157">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-158">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="885ed-158">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-159">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="885ed-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-160">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="885ed-160">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-161">Встроенные приложения и надстройки могут взаимодействовать с виртуальным приложением Outlook через MAPI</span><span class="sxs-lookup"><span data-stu-id="885ed-161">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-162">Подключаемый модуль SharePoint для Firefox</span><span class="sxs-lookup"><span data-stu-id="885ed-162">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-163">Пользователь может использовать возможности SharePoint в Firefox</span><span class="sxs-lookup"><span data-stu-id="885ed-163">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-164">Приложение панели управления "почта"</span><span class="sxs-lookup"><span data-stu-id="885ed-164">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-165">Пользователь получает панель управления "почта" в Outlook</span><span class="sxs-lookup"><span data-stu-id="885ed-165">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-166">Да</span><span class="sxs-lookup"><span data-stu-id="885ed-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-167">Основные сборки взаимодействия</span><span class="sxs-lookup"><span data-stu-id="885ed-167">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-168">Поддержка управляемых надстроек</span><span class="sxs-lookup"><span data-stu-id="885ed-168">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-169">Обработчик кэша документов Office</span><span class="sxs-lookup"><span data-stu-id="885ed-169">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-170">Разрешение кэша документов для приложений Office</span><span class="sxs-lookup"><span data-stu-id="885ed-170">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-171">Обработчик поиска протоколов Outlook</span><span class="sxs-lookup"><span data-stu-id="885ed-171">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-172">Пользователь может выполнять поиск в Outlook</span><span class="sxs-lookup"><span data-stu-id="885ed-172">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-173">Да</span><span class="sxs-lookup"><span data-stu-id="885ed-173">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="885ed-174">Элементы управления ActiveX:</span><span class="sxs-lookup"><span data-stu-id="885ed-174">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-175">Дополнительные сведения об элементах ActiveX можно найти в <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> справочнике API элементов ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="885ed-175">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-176">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="885ed-176">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-177">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-177">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-178">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="885ed-178">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-179">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-179">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-180">SharePoint. openDocument</span><span class="sxs-lookup"><span data-stu-id="885ed-180">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-181">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-181">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-182">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="885ed-182">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-183">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-183">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-184">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="885ed-184">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-185">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-185">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-186">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="885ed-186">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-187">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-187">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-188">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="885ed-188">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-189">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-189">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-190">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="885ed-190">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-191">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-191">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-192">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="885ed-192">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-193">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-193">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-194">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="885ed-194">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-195">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-195">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-196">WinProj. активатор</span><span class="sxs-lookup"><span data-stu-id="885ed-196">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-197">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-197">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-198">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="885ed-198">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-199">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-199">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-200">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="885ed-200">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-201">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-201">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-202">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="885ed-202">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-203">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-203">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="885ed-204">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="885ed-204">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-205">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="885ed-205">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="885ed-206">Вспомогательное приложение браузера OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="885ed-206">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-207">Элемент управления ActiveX]</span><span class="sxs-lookup"><span data-stu-id="885ed-207">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="885ed-208">Наложения значков OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="885ed-208">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="885ed-209">Перекрытие значков оболочки в проводнике Windows при просмотре папок в папках OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="885ed-209">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="885ed-210">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="885ed-210">Additional resources</span></span>


**<span data-ttu-id="885ed-211">Пакеты Office 2013 App-V 5,0 5,0 дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="885ed-211">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="885ed-212">Поддерживаемые сценарии для развертывания Microsoft Office в последовательном пакете App-V</span><span class="sxs-lookup"><span data-stu-id="885ed-212">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="885ed-213">Пакеты Office 2010 App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="885ed-213">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="885ed-214">Комплект виртуализации Microsoft Office 2010 для Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="885ed-214">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="885ed-215">Известные проблемы, возникающие при создании или использовании пакета Office 2010 для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="885ed-215">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="885ed-216">Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="885ed-216">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="885ed-217">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="885ed-217">Connection Groups</span></span>**

[<span data-ttu-id="885ed-218">Развертывание групп подключений в Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="885ed-218">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="885ed-219">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="885ed-219">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="885ed-220">Динамическая настройка</span><span class="sxs-lookup"><span data-stu-id="885ed-220">Dynamic Configuration</span></span>**

[<span data-ttu-id="885ed-221">Сведения о динамической конфигурации App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="885ed-221">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)






 

 





