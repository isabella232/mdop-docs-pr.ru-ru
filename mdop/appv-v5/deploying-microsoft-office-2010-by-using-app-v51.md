---
title: Развертывание Microsoft Office 2010 с помощью App-V
description: Развертывание Microsoft Office 2010 с помощью App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814624"
---
# <span data-ttu-id="b5278-103">Развертывание Microsoft Office 2010 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-103">Deploying Microsoft Office 2010 by Using App-V</span></span>


<span data-ttu-id="b5278-104">Пакеты Office 2010 для Microsoft Application Virtualization (App-V) 5,1 можно создать с помощью одного из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="b5278-104">You can create Office 2010 packages for Microsoft Application Virtualization (App-V) 5.1 using one of the following methods:</span></span>

-   <span data-ttu-id="b5278-105">Секвенсор Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="b5278-105">Application Virtualization (App-V) Sequencer</span></span>

-   <span data-ttu-id="b5278-106">Ускоритель пакетов для Application Virtualization (App-V)</span><span class="sxs-lookup"><span data-stu-id="b5278-106">Application Virtualization (App-V) Package Accelerator</span></span>

## <span data-ttu-id="b5278-107">Поддержка App-V для Office 2010</span><span class="sxs-lookup"><span data-stu-id="b5278-107">App-V support for Office 2010</span></span>


<span data-ttu-id="b5278-108">В следующей таблице показаны версии App-V, методы создания пакетов Office, поддерживаемые лицензированные и поддерживаемые развертывания для Office 2010.</span><span class="sxs-lookup"><span data-stu-id="b5278-108">The following table shows the App-V versions, methods of Office package creation, supported licensing, and supported deployments for Office 2010.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5278-109">Поддерживаемый элемент</span><span class="sxs-lookup"><span data-stu-id="b5278-109">Supported item</span></span></th>
<th align="left"><span data-ttu-id="b5278-110">Уровень поддержки</span><span class="sxs-lookup"><span data-stu-id="b5278-110">Level of support</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-111">Поддерживаемые версии App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-111">Supported App-V versions</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b5278-112">4,6</span><span class="sxs-lookup"><span data-stu-id="b5278-112">4.6</span></span></p></li>
<li><p><span data-ttu-id="b5278-113">5.0</span><span class="sxs-lookup"><span data-stu-id="b5278-113">5.0</span></span></p></li>
<li><p><span data-ttu-id="b5278-114">5,1</span><span class="sxs-lookup"><span data-stu-id="b5278-114">5.1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-115">Создание пакета</span><span class="sxs-lookup"><span data-stu-id="b5278-115">Package creation</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b5278-116">Последовательность</span><span class="sxs-lookup"><span data-stu-id="b5278-116">Sequencing</span></span></p></li>
<li><p><span data-ttu-id="b5278-117">Ускоритель пакетов</span><span class="sxs-lookup"><span data-stu-id="b5278-117">Package Accelerator</span></span></p></li>
<li><p><span data-ttu-id="b5278-118">Комплект средств для развертывания Office</span><span class="sxs-lookup"><span data-stu-id="b5278-118">Office Deployment Kit</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-119">Поддерживаемое лицензирование</span><span class="sxs-lookup"><span data-stu-id="b5278-119">Supported licensing</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-120">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="b5278-120">Volume Licensing</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-121">Поддерживаемые развертывания</span><span class="sxs-lookup"><span data-stu-id="b5278-121">Supported deployments</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b5278-122">Desktop</span><span class="sxs-lookup"><span data-stu-id="b5278-122">Desktop</span></span></p></li>
<li><p><span data-ttu-id="b5278-123">Персональный VDI</span><span class="sxs-lookup"><span data-stu-id="b5278-123">Personal VDI</span></span></p></li>
<li><p><span data-ttu-id="b5278-124">СЛУЖБ</span><span class="sxs-lookup"><span data-stu-id="b5278-124">RDS</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b5278-125">Создание Office 2010 App-V 5,1 с помощью секвенсора</span><span class="sxs-lookup"><span data-stu-id="b5278-125">Creating Office 2010 App-V 5.1 using the sequencer</span></span>


<span data-ttu-id="b5278-126">Виртуализация Office 2010 — это один из основных методов создания пакета Office 2010 на App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b5278-126">Sequencing Office 2010 is one of the main methods for creating an Office 2010 package on App-V 5.1.</span></span> <span data-ttu-id="b5278-127">Корпорация Майкрософт предоставила подробный рецепт в статье базы знаний.</span><span class="sxs-lookup"><span data-stu-id="b5278-127">Microsoft has provided a detailed recipe through a Knowledge Base article.</span></span> <span data-ttu-id="b5278-128">Чтобы создать пакет Office 2010 для App-V 5,1, ознакомьтесь с подробными инструкциями по следующей ссылке:</span><span class="sxs-lookup"><span data-stu-id="b5278-128">To create an Office 2010 package on App-V 5.1, refer to the following link for detailed instructions:</span></span>

[<span data-ttu-id="b5278-129">Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b5278-129">How To Sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## <span data-ttu-id="b5278-130">Создание пакетов Office 2010 App-V 5,1 с помощью ускорителей пакетов</span><span class="sxs-lookup"><span data-stu-id="b5278-130">Creating Office 2010 App-V 5.1 packages using package accelerators</span></span>


<span data-ttu-id="b5278-131">Пакеты Office 2010 App-V 5,1 можно создавать с помощью ускорителей пакетов.</span><span class="sxs-lookup"><span data-stu-id="b5278-131">Office 2010 App-V 5.1 packages can be created through package accelerators.</span></span> <span data-ttu-id="b5278-132">Корпорация Майкрософт предоставила акселераторы пакетов для создания Office 2010 в Windows 10, Windows 8 и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5278-132">Microsoft has provided package accelerators for creating Office 2010 on Windows 10, Windows 8 and Windows 7.</span></span> <span data-ttu-id="b5278-133">Чтобы создать пакеты Office 2010 в App-V с помощью ускорителей пакетов, просмотрите следующие страницы, чтобы получить доступ к соответствующему ускорительу пакетов:</span><span class="sxs-lookup"><span data-stu-id="b5278-133">To create Office 2010 packages on App-V using Package accelerators, refer to the following pages to access the appropriate package accelerator:</span></span>

-   [<span data-ttu-id="b5278-134">Ускоритель пакетов для Office профессиональный плюс 2010 — Windows 8 (App-V 5,0)</span><span class="sxs-lookup"><span data-stu-id="b5278-134">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 8</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [<span data-ttu-id="b5278-135">Ускоритель пакетов для Office профессиональный плюс 2010 – Windows 7 (App-V 5,0)</span><span class="sxs-lookup"><span data-stu-id="b5278-135">App-V 5.0 Package Accelerator for Office Professional Plus 2010 – Windows 7</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330678)

<span data-ttu-id="b5278-136">Подробные инструкции по созданию пакетов виртуальных приложений с помощью ускорителей пакетов App-V можно найти в разделе [Создание виртуального пакета приложения с помощью ускорителя пакетов App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span><span class="sxs-lookup"><span data-stu-id="b5278-136">For detailed instructions on how to create virtual application packages using App-V package accelerators, see [How to Create a Virtual Application Package Using an App-V Package Accelerator](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).</span></span>

## <span data-ttu-id="b5278-137">Развертывание пакета Microsoft Office для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b5278-137">Deploying the Microsoft Office package for App-V 5.1</span></span>


<span data-ttu-id="b5278-138">Пакеты Office 2010 можно развертывать с помощью любого из указанных ниже методов развертывания App-V.</span><span class="sxs-lookup"><span data-stu-id="b5278-138">You can deploy Office 2010 packages by using any of the following App-V deployment methods:</span></span>

-   <span data-ttu-id="b5278-139">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b5278-139">System Center Configuration Manager</span></span>

-   <span data-ttu-id="b5278-140">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-140">App-V server</span></span>

-   <span data-ttu-id="b5278-141">Самостоятельная работа с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="b5278-141">Stand-alone through PowerShell commands</span></span>

## <span data-ttu-id="b5278-142">Управление пакетами и настройка в Office App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-142">Office App-V package management and customization</span></span>


<span data-ttu-id="b5278-143">Пакеты Office 2010 могут управляться так же, как и любые другие пакеты App-V 5,1 с помощью стандартных механизмов управления пакетами.</span><span class="sxs-lookup"><span data-stu-id="b5278-143">Office 2010 packages can be managed like any other App-V 5.1 packages through known package management mechanisms.</span></span> <span data-ttu-id="b5278-144">Специальные инструкции не требуются, например, для добавления, публикации, отмены публикации и удаления пакетов Office.</span><span class="sxs-lookup"><span data-stu-id="b5278-144">No special instructions are needed, for example, to add, publish, unpublish, or remove Office packages.</span></span>

## <span data-ttu-id="b5278-145">Интеграция Microsoft Office с Windows</span><span class="sxs-lookup"><span data-stu-id="b5278-145">Microsoft Office integration with Windows</span></span>


<span data-ttu-id="b5278-146">В таблице ниже приведен полный список поддерживаемых точек интеграции для Office 2010.</span><span class="sxs-lookup"><span data-stu-id="b5278-146">The following table provides a full list of supported integration points for Office 2010.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b5278-147">Точка расширения</span><span class="sxs-lookup"><span data-stu-id="b5278-147">Extension Point</span></span></th>
<th align="left"><span data-ttu-id="b5278-148">Описание</span><span class="sxs-lookup"><span data-stu-id="b5278-148">Description</span></span></th>
<th align="left"><span data-ttu-id="b5278-149">Office 2010</span><span class="sxs-lookup"><span data-stu-id="b5278-149">Office 2010</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-150">Плагин присоединения к собранию Lync для Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="b5278-150">Lync meeting Join Plug-in for Firefox and Chrome</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-151">Пользователь может присоединиться к собраниям Lync из Firefox и Chrome</span><span class="sxs-lookup"><span data-stu-id="b5278-151">User can join Lync meetings from Firefox and Chrome</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-152">Отправлено в драйвер печати OneNote</span><span class="sxs-lookup"><span data-stu-id="b5278-152">Sent to OneNote Print Driver</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-153">Пользователь может печатать в OneNote</span><span class="sxs-lookup"><span data-stu-id="b5278-153">User can print to OneNote</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-154">Да</span><span class="sxs-lookup"><span data-stu-id="b5278-154">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-155">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="b5278-155">OneNote Linked Notes</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-156">Связанные заметки OneNote</span><span class="sxs-lookup"><span data-stu-id="b5278-156">OneNote Linked Notes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-157">Надстройка "отправить в OneNote" в Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b5278-157">Send to OneNote Internet Explorer Add-In</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-158">Пользователь может отправлять сообщения в OneNote из браузера Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="b5278-158">User can send to OneNote from IE</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-159">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="b5278-159">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-160">Исключение брандмауэра для Lync и Outlook</span><span class="sxs-lookup"><span data-stu-id="b5278-160">Firewall Exception for Lync and Outlook</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-161">Клиент MAPI</span><span class="sxs-lookup"><span data-stu-id="b5278-161">MAPI Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-162">Встроенные приложения и надстройки могут взаимодействовать с виртуальным приложением Outlook через MAPI</span><span class="sxs-lookup"><span data-stu-id="b5278-162">Native apps and add-ins can interact with virtual Outlook through MAPI</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-163">Подключаемый модуль SharePoint для Firefox</span><span class="sxs-lookup"><span data-stu-id="b5278-163">SharePoint Plugin for Firefox</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-164">Пользователь может использовать возможности SharePoint в Firefox</span><span class="sxs-lookup"><span data-stu-id="b5278-164">User can use SharePoint features in Firefox</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-165">Приложение панели управления "почта"</span><span class="sxs-lookup"><span data-stu-id="b5278-165">Mail Control Panel Applet</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-166">Пользователь получает панель управления "почта" в Outlook</span><span class="sxs-lookup"><span data-stu-id="b5278-166">User gets the mail control panel applet in Outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-167">Да</span><span class="sxs-lookup"><span data-stu-id="b5278-167">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-168">Основные сборки взаимодействия</span><span class="sxs-lookup"><span data-stu-id="b5278-168">Primary Interop Assemblies</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-169">Поддержка управляемых надстроек</span><span class="sxs-lookup"><span data-stu-id="b5278-169">Support managed add-ins</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-170">Обработчик кэша документов Office</span><span class="sxs-lookup"><span data-stu-id="b5278-170">Office Document Cache Handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-171">Разрешение кэша документов для приложений Office</span><span class="sxs-lookup"><span data-stu-id="b5278-171">Allows Document Cache for Office applications</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-172">Обработчик поиска протоколов Outlook</span><span class="sxs-lookup"><span data-stu-id="b5278-172">Outlook Protocol Search handler</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-173">Пользователь может выполнять поиск в Outlook</span><span class="sxs-lookup"><span data-stu-id="b5278-173">User can search in outlook</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-174">Да</span><span class="sxs-lookup"><span data-stu-id="b5278-174">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b5278-175">Элементы управления ActiveX:</span><span class="sxs-lookup"><span data-stu-id="b5278-175">Active X Controls:</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-176">Дополнительные сведения об элементах ActiveX можно найти в <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> справочнике API элементов ActiveX </a> .</span><span class="sxs-lookup"><span data-stu-id="b5278-176">For more information on ActiveX controls, refer to <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)">ActiveX Control API Reference</a>.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-177">Groove. SiteClient</span><span class="sxs-lookup"><span data-stu-id="b5278-177">Groove.SiteClient</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-178">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-178">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-179">PortalConnect.PersonalSite</span><span class="sxs-lookup"><span data-stu-id="b5278-179">PortalConnect.PersonalSite</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-180">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-180">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-181">SharePoint. openDocument</span><span class="sxs-lookup"><span data-stu-id="b5278-181">SharePoint.openDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-182">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-182">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-183">SharePoint. ExportDatabase</span><span class="sxs-lookup"><span data-stu-id="b5278-183">SharePoint.ExportDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-184">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-184">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-185">SharePoint. SpreadSheetLauncher</span><span class="sxs-lookup"><span data-stu-id="b5278-185">SharePoint.SpreadSheetLauncher</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-186">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-186">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-187">SharePoint. StssyncHander</span><span class="sxs-lookup"><span data-stu-id="b5278-187">SharePoint.StssyncHander</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-188">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-188">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-189">SharePoint. DragUploadCtl</span><span class="sxs-lookup"><span data-stu-id="b5278-189">SharePoint.DragUploadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-190">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-190">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-191">SharePoint. DragDownloadCtl</span><span class="sxs-lookup"><span data-stu-id="b5278-191">SharePoint.DragDownloadCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-192">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-192">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-193">SharePoint. OpenXMLDocuments</span><span class="sxs-lookup"><span data-stu-id="b5278-193">Sharpoint.OpenXMLDocuments</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-194">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-194">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-195">SharePoint. ClipboardCtl</span><span class="sxs-lookup"><span data-stu-id="b5278-195">Sharepoint.ClipboardCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-196">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-196">Active X control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-197">WinProj. активатор</span><span class="sxs-lookup"><span data-stu-id="b5278-197">WinProj.Activator</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-198">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-198">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-199">Name. NameCtrl</span><span class="sxs-lookup"><span data-stu-id="b5278-199">Name.NameCtrl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-200">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-200">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-201">STSUPld.CopyCtl</span><span class="sxs-lookup"><span data-stu-id="b5278-201">STSUPld.CopyCtl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-202">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-202">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-203">CommunicatorMeetingJoinAx.JoinManager</span><span class="sxs-lookup"><span data-stu-id="b5278-203">CommunicatorMeetingJoinAx.JoinManager</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-204">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-204">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   <span data-ttu-id="b5278-205">LISTNET. Listnet</span><span class="sxs-lookup"><span data-stu-id="b5278-205">LISTNET.Listnet</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-206">Элемент управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="b5278-206">Active X Control</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   <span data-ttu-id="b5278-207">Вспомогательное приложение браузера OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="b5278-207">OneDrive Pro Browser Helper</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-208">Элемент управления ActiveX]</span><span class="sxs-lookup"><span data-stu-id="b5278-208">Active X Control]</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b5278-209">Наложения значков OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="b5278-209">OneDrive Pro Icon Overlays</span></span></p></td>
<td align="left"><p><span data-ttu-id="b5278-210">Перекрытие значков оболочки в проводнике Windows при просмотре папок в папках OneDrive Pro</span><span class="sxs-lookup"><span data-stu-id="b5278-210">Windows explorer shell icon overlays when users look at folders OneDrive Pro folders</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b5278-211">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b5278-211">Additional resources</span></span>


**<span data-ttu-id="b5278-212">Дополнительные ресурсы в пакетах Office 2013 App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-212">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="b5278-213">Поддерживаемые сценарии для развертывания Microsoft Office в последовательном пакете App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-213">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="b5278-214">Пакеты приложения Office 2010 App-V</span><span class="sxs-lookup"><span data-stu-id="b5278-214">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="b5278-215">Комплект виртуализации Microsoft Office 2010 для Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b5278-215">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="b5278-216">Известные проблемы, возникающие при создании или использовании пакета Office 2010 для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b5278-216">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="b5278-217">Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b5278-217">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="b5278-218">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="b5278-218">Connection Groups</span></span>**

[<span data-ttu-id="b5278-219">Развертывание групп подключений в Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="b5278-219">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="b5278-220">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="b5278-220">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="b5278-221">Динамическая настройка</span><span class="sxs-lookup"><span data-stu-id="b5278-221">Dynamic Configuration</span></span>**

[<span data-ttu-id="b5278-222">Сведения о динамической конфигурации App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b5278-222">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)






 

 





