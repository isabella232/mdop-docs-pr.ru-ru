---
title: Подготовка к развертыванию UE-V 2. x
description: Подготовка к развертыванию UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826422"
---
# <span data-ttu-id="64ee6-103">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="64ee6-103">Prepare a UE-V 2.x Deployment</span></span>


<span data-ttu-id="64ee6-104">Перед развертыванием Microsoft User Experience Virtualization (UE-V) 2,0 или 2,1 в качестве решения для синхронизации параметров между устройствами, доступными для пользователей в вашей организации, необходимо выполнить некоторые планирование и подготовку.</span><span class="sxs-lookup"><span data-stu-id="64ee6-104">There is some planning and preparation to do before you deploy Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1 as a solution for synchronizing settings between devices that users access in your enterprise.</span></span> <span data-ttu-id="64ee6-105">В этой статье объясняется, как определить тип развертывания и подготовиться к развертыванию, чтобы выполнить развертывание успешно.</span><span class="sxs-lookup"><span data-stu-id="64ee6-105">This topic helps you determine what type of deployment you'll be doing and what preparation you can make beforehand so that your deployment is successful.</span></span>

<span data-ttu-id="64ee6-106">Для начала рассмотрим задачи, которые нужно выполнить для развертывания UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-106">First, let’s look at the tasks you’ll do to deploy UE-V:</span></span>

-   <span data-ttu-id="64ee6-107">Планирование развертывания UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-107">Plan your UE-V Deployment</span></span>

    <span data-ttu-id="64ee6-108">Перед развертыванием любого из них лучше всего выполнить планирование, чтобы можно было определить, какие компоненты UE-V вы будете развертывать.</span><span class="sxs-lookup"><span data-stu-id="64ee6-108">Before you deploy anything, a good first step is to do a little bit of planning so that you can determine which UE-V features you’ll deploy.</span></span> <span data-ttu-id="64ee6-109">Поэтому, если вы покинете эту страницу, убедитесь, что вы вернулись назад и прочтите сведения о планировании ниже.</span><span class="sxs-lookup"><span data-stu-id="64ee6-109">So if you leave this page, make sure you come back and read through the planning information below.</span></span>

-   [<span data-ttu-id="64ee6-110">Развертывание необходимых компонентов для UE-v 2.x</span><span class="sxs-lookup"><span data-stu-id="64ee6-110">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    <span data-ttu-id="64ee6-111">Для каждого развертывания UE-V требуются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="64ee6-111">Every UE-V deployment requires these activities:</span></span>

    -   [<span data-ttu-id="64ee6-112">Определение места хранения параметров</span><span class="sxs-lookup"><span data-stu-id="64ee6-112">Define a settings storage location</span></span>](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [<span data-ttu-id="64ee6-113">Определение способа развертывания агента UE-V и управление конфигурациями UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-113">Decide how to deploy the UE-V Agent and manage UE-V configurations</span></span>](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   <span data-ttu-id="64ee6-114">[Установка агента UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) на всех компьютерах пользователей, для которых требуется синхронизация параметров</span><span class="sxs-lookup"><span data-stu-id="64ee6-114">[Install the UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) on every user computer that needs settings synchronized</span></span>

-   <span data-ttu-id="64ee6-115">Кроме того, вы можете [развернуть UE-V 2. x для настраиваемых приложений](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span><span class="sxs-lookup"><span data-stu-id="64ee6-115">Optionally, you can [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)</span></span>

    <span data-ttu-id="64ee6-116">Планирование поможет вам определить, поддерживает ли UE-V синхронизацию параметров для настраиваемых приложений (сторонние или бизнес-версии), для которой требуются следующие возможности UE-V:</span><span class="sxs-lookup"><span data-stu-id="64ee6-116">Planning will help you figure out whether you want UE-V to support the synchronization of settings for custom applications (third-party or line-of-business), which requires these UE-V features:</span></span>

    -   <span data-ttu-id="64ee6-117">[Установить генератор UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) , чтобы можно было создавать, изменять и проверять пользовательские шаблоны расположений параметров, необходимые для синхронизации настраиваемых параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-117">[Install the UEV Generator](https://technet.microsoft.com/library/dn458942.aspx#uevgen) so you can create, edit, and validate the custom settings location templates required to synchronize custom application settings</span></span>

    -   <span data-ttu-id="64ee6-118">[Создание настраиваемых шаблонов расположений параметров](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) с помощью UE-V Generator</span><span class="sxs-lookup"><span data-stu-id="64ee6-118">[Create custom settings location templates](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) by using the UE-V Generator</span></span>

    -   <span data-ttu-id="64ee6-119">[Развертывание каталога шаблонов параметров ue-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) , который используется для хранения настраиваемых шаблонов расположения личных параметров</span><span class="sxs-lookup"><span data-stu-id="64ee6-119">[Deploy a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) that you use to store your custom settings location templates</span></span>

<span data-ttu-id="64ee6-120">Эта схема рабочего процесса предоставляет общее представление о развертывании UE-V и решениях, которые определяют, как развертывается UE-V на предприятии.</span><span class="sxs-lookup"><span data-stu-id="64ee6-120">This workflow diagram provides a high-level understanding of a UE-V deployment and the decisions that determine how you deploy UE-V in your enterprise.</span></span>

![deploymentworkflow](images/deploymentworkflow.png)

<span data-ttu-id="64ee6-122">**Планирование развертывания UE-V:** Прежде всего, вам нужно немного планировать, чтобы вы могли определять, какие компоненты UE-V вы будете развертывать.</span><span class="sxs-lookup"><span data-stu-id="64ee6-122">**Planning a UE-V deployment:** First, you want to do a little bit of planning so that you can determine which UE-V components you’ll be deploying.</span></span> <span data-ttu-id="64ee6-123">Планирование развертывания UE-V включает в себя следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="64ee6-123">Planning a UE-V deployment involves these things:</span></span>

-   [<span data-ttu-id="64ee6-124">Решите, нужно ли синхронизировать параметры для настраиваемых приложений.</span><span class="sxs-lookup"><span data-stu-id="64ee6-124">Decide whether to synchronize settings for custom applications</span></span>](#deciding)

    <span data-ttu-id="64ee6-125">Этот параметр определяет, будет ли при развертывании устанавливаться генератор UE-V, что позволяет создавать пользовательские шаблоны расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-125">This determines whether you will install the UE-V Generator during deployment, which lets you create custom settings location templates.</span></span> <span data-ttu-id="64ee6-126">Она включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="64ee6-126">It involves the following:</span></span>

    <span data-ttu-id="64ee6-127">Проверьте [Параметры, которые автоматически синхронизируются в развертывании UE-V](#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="64ee6-127">Review the [settings that are synchronized automatically in a UE-V deployment](#autosyncsettings).</span></span>

    <span data-ttu-id="64ee6-128">[Определите, нужно ли синхронизировать параметры для других приложений](#determinesettingssync).</span><span class="sxs-lookup"><span data-stu-id="64ee6-128">[Determine whether you need settings synchronized for other applications](#determinesettingssync).</span></span>

-   <span data-ttu-id="64ee6-129">Ознакомьтесь с [другими замечаниями по развертыванию UE-V](#considerations), например с высокой степенью доступности и планированием мощностей.</span><span class="sxs-lookup"><span data-stu-id="64ee6-129">Review [other considerations for deploying UE-V](#considerations), such as high availability and capacity planning.</span></span>

-   [<span data-ttu-id="64ee6-130">Подтверждение предварительных требований и поддерживаемых конфигураций для UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-130">Confirm prerequisites and supported configurations for UE-V</span></span>](#prereqs)

## <a href="" id="deciding"></a><span data-ttu-id="64ee6-131">Решите, нужно ли синхронизировать параметры для настраиваемых приложений.</span><span class="sxs-lookup"><span data-stu-id="64ee6-131">Decide Whether to Synchronize Settings for Custom Applications</span></span>


<span data-ttu-id="64ee6-132">В развертывании UE-V многие параметры синхронизируются автоматически.</span><span class="sxs-lookup"><span data-stu-id="64ee6-132">In a UE-V deployment, many settings are automatically synchronized.</span></span> <span data-ttu-id="64ee6-133">Но вы также можете настроить UE-V для синхронизации параметров для других приложений, таких как бизнес-и сторонние приложения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-133">But you can also customize UE-V to synchronize settings for other applications, such as line-of-business and third-party apps.</span></span>

<span data-ttu-id="64ee6-134">Если вы решите, что UE-V должен синхронизировать параметры для настраиваемых приложений, скорее всего, это является наиболее важной частью планирования развертывания UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-134">Deciding if you want UE-V to synchronize settings for custom applications is probably the most important part of planning your UE-V deployment.</span></span> <span data-ttu-id="64ee6-135">Этот раздел поможет вам принять решение.</span><span class="sxs-lookup"><span data-stu-id="64ee6-135">The topics in this section will help you make that decision.</span></span>

### <a href="" id="autosyncsettings"></a><span data-ttu-id="64ee6-136">Параметры, которые автоматически синхронизируются в развертывании UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-136">Settings that are automatically synchronized in a UE-V deployment</span></span>

<span data-ttu-id="64ee6-137">Этот раздел содержит сведения о параметрах, которые синхронизируются по умолчанию в UE-V, в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="64ee6-137">This section provides information about the settings that are synchronized by default in UE-V, including the following:</span></span>

<span data-ttu-id="64ee6-138">Классических приложениях, параметры которых синхронизируются по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64ee6-138">Desktop applications whose settings are synchronized by default</span></span>

<span data-ttu-id="64ee6-139">Параметры рабочего стола Windows, синхронизированные по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64ee6-139">Windows desktop settings that are synchronized by default</span></span>

<span data-ttu-id="64ee6-140">Выписка о поддержке синхронизации параметров приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-140">A statement of support for Windows app setting synchronization</span></span>

<span data-ttu-id="64ee6-141">В разделе [Шаблоны параметров виртуализации взаимодействия с пользователем (UE-v) для Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) можно скачать полный список определенных параметров для microsoft Office 2013, Microsoft Office 2010 и Microsoft Office 2007, которые синхронизируются с UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-141">See [User Experience Virtualization (UE-V) settings templates for Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) to download a complete list of the specific Microsoft Office 2013, Microsoft Office 2010, and Microsoft Office 2007 settings that are synchronized by UE-V.</span></span>

### <span data-ttu-id="64ee6-142">Классических приложений, синхронизированных по умолчанию в UE-V 2,1 и UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="64ee6-142">Desktop applications synchronized by default in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="64ee6-143">При установке агента UE-V 2,1 или 2,1 с пакетом обновления 1 (SP1) он регистрирует стандартную группу шаблонов расположений параметров, которые захватывают значения параметров для этих распространенных приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64ee6-143">When you install the UE-V 2.1 or 2.1 SP1 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="64ee6-144">Совет</span><span class="sxs-lookup"><span data-stu-id="64ee6-144">Tip</span></span>**  
<span data-ttu-id="64ee6-145">**Синхронизация параметров Microsoft Office 2007** — в UE-V 2,1 и 2,1 SP1 шаблон расположений параметров больше не включается по умолчанию для приложений Office 2007.</span><span class="sxs-lookup"><span data-stu-id="64ee6-145">**Microsoft Office 2007 Settings Synchronization** – In UE-V 2.1 and 2.1 SP1, a settings location template is no longer included by default for Office 2007 applications.</span></span> <span data-ttu-id="64ee6-146">Однако вы по-прежнему можете использовать шаблоны Office 2007 с UE-V 2,0 или более ранней версии, чтобы получить доступ к шаблонам из [коллекции шаблонов UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="64ee6-146">However, you can still use Office 2007 templates from UE-V 2.0 or earlier and can get the templates from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="64ee6-147">Категория приложения</span><span class="sxs-lookup"><span data-stu-id="64ee6-147">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-148">Описание</span><span class="sxs-lookup"><span data-stu-id="64ee6-148">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-149">Приложения Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-149">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="64ee6-150">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</span><span class="sxs-lookup"><span data-stu-id="64ee6-150">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-151">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-151">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="64ee6-152">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-152">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="64ee6-153">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-153">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="64ee6-154">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-154">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="64ee6-155">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-155">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="64ee6-156">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-156">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="64ee6-157">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-157">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="64ee6-158">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-158">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="64ee6-159">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-159">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="64ee6-160">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-160">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="64ee6-161">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-161">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="64ee6-162">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-162">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="64ee6-163">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-163">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-164">Приложения Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-164">Microsoft Office 2013 applications</span></span></p>
<p><span data-ttu-id="64ee6-165">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</span><span class="sxs-lookup"><span data-stu-id="64ee6-165">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-166">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-166">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="64ee6-167">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-167">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="64ee6-168">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-168">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="64ee6-169">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-169">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="64ee6-170">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-170">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="64ee6-171">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-171">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="64ee6-172">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-172">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="64ee6-173">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-173">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="64ee6-174">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-174">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="64ee6-175">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-175">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="64ee6-176">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-176">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="64ee6-177">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-177">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="64ee6-178">Центр отправки Microsoft Office 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-178">Microsoft Office 2013 Upload Center</span></span></p>
<p><span data-ttu-id="64ee6-179">Microsoft OneDrive для бизнеса 2013</span><span class="sxs-lookup"><span data-stu-id="64ee6-179">Microsoft OneDrive for Business 2013</span></span></p>
<p><span data-ttu-id="64ee6-180">Шаблоны расположения параметров UE-V 2,1 и 2,1 SP1 Microsoft Office 2013 включают улучшенную поддержку подписей в Outlook.</span><span class="sxs-lookup"><span data-stu-id="64ee6-180">The UE-V 2.1 and 2.1 SP1 Microsoft Office 2013 settings location templates include improved Outlook signature support.</span></span> <span data-ttu-id="64ee6-181">Добавлена синхронизация параметров подписи по умолчанию для новых, ответных и пересылаемых сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="64ee6-181">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="64ee6-182">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-182">Note</span></span></strong><br/><p><span data-ttu-id="64ee6-183">Профиль Outlook должен быть создан для любого устройства, на котором пользователь хочет синхронизировать свою подпись Outlook.</span><span class="sxs-lookup"><span data-stu-id="64ee6-183">An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="64ee6-184">Если профиль еще не создан, пользователь может создать его, а затем перезапустить Outlook на этом устройстве, чтобы включить синхронизацию подписей.</span><span class="sxs-lookup"><span data-stu-id="64ee6-184">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-185">Параметры браузера: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 и Internet Explorer 11</span><span class="sxs-lookup"><span data-stu-id="64ee6-185">Browser options: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10, and Internet Explorer 11</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-186">Избранное, Домашняя страница, вкладки и панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="64ee6-186">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="64ee6-187">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-187">Note</span></span></strong><br/><p><span data-ttu-id="64ee6-188">UE-V не перемещайте параметры для файлов cookie браузера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="64ee6-188">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-189">Аксессуары для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-189">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-190">Microsoft калькулятор, Блокнот, WordPad.</span><span class="sxs-lookup"><span data-stu-id="64ee6-190">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="64ee6-191">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-191">Note</span></span>**  
<span data-ttu-id="64ee6-192">UE-V 2,1 SP1 не синхронизирует параметры между Microsoft Calculator в Windows 10 и калькулятором Microsoft в предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="64ee6-192">UE-V 2.1 SP1 does not synchronize settings between the Microsoft Calculator in Windows 10 and the Microsoft Calculator in previous operating systems.</span></span>



### <span data-ttu-id="64ee6-193">Классических приложений, синхронизированных по умолчанию в UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="64ee6-193">Desktop applications synchronized by default in UE-V 2.0</span></span>

<span data-ttu-id="64ee6-194">При установке агента UE-V 2,0 он регистрирует стандартную группу шаблонов расположений параметров, которые захватывают значения параметров для этих распространенных приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="64ee6-194">When you install the UE-V 2.0 Agent, it registers a default group of settings location templates that capture settings values for these common Microsoft applications.</span></span>

**<span data-ttu-id="64ee6-195">Совет</span><span class="sxs-lookup"><span data-stu-id="64ee6-195">Tip</span></span>**  
<span data-ttu-id="64ee6-196">**Синхронизация параметров Microsoft Office 2013** — в UE-v 2,0 шаблон расположений параметров не включается по умолчанию для приложений Office 2013, но доступен для скачивания из [коллекции шаблонов UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="64ee6-196">**Microsoft Office 2013 Settings Synchronization** – In UE-V 2.0, a settings location template is not included by default for Office 2013 applications, but is available for download from the [UE-V template gallery](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span> <span data-ttu-id="64ee6-197">[Синхронизация Office 2013 с UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) содержит подробные сведения о поддерживаемых шаблонах, которые синхронизируют параметры Office 2013.</span><span class="sxs-lookup"><span data-stu-id="64ee6-197">[Synchronizing Office 2013 with UE-V 2.0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) provides details about the supported templates that synchronize Office 2013 settings.</span></span>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="64ee6-198">Категория приложения</span><span class="sxs-lookup"><span data-stu-id="64ee6-198">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-199">Описание</span><span class="sxs-lookup"><span data-stu-id="64ee6-199">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-200">Приложения Microsoft Office 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-200">Microsoft Office 2007 applications</span></span></p>
<p><span data-ttu-id="64ee6-201">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</span><span class="sxs-lookup"><span data-stu-id="64ee6-201">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-202">Microsoft Access 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-202">Microsoft Access 2007</span></span></p>
<p><span data-ttu-id="64ee6-203">Microsoft Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-203">Microsoft Communicator 2007</span></span></p>
<p><span data-ttu-id="64ee6-204">Microsoft Excel 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-204">Microsoft Excel 2007</span></span></p>
<p><span data-ttu-id="64ee6-205">Microsoft InfoPath 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-205">Microsoft InfoPath 2007</span></span></p>
<p><span data-ttu-id="64ee6-206">Microsoft OneNote 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-206">Microsoft OneNote 2007</span></span></p>
<p><span data-ttu-id="64ee6-207">Microsoft Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-207">Microsoft Outlook 2007</span></span></p>
<p><span data-ttu-id="64ee6-208">Microsoft PowerPoint 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-208">Microsoft PowerPoint 2007</span></span></p>
<p><span data-ttu-id="64ee6-209">Microsoft Project 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-209">Microsoft Project 2007</span></span></p>
<p><span data-ttu-id="64ee6-210">Microsoft Publisher 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-210">Microsoft Publisher 2007</span></span></p>
<p><span data-ttu-id="64ee6-211">Microsoft SharePoint Designer 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-211">Microsoft SharePoint Designer 2007</span></span></p>
<p><span data-ttu-id="64ee6-212">Microsoft Visio 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-212">Microsoft Visio 2007</span></span></p>
<p><span data-ttu-id="64ee6-213">Microsoft Word 2007</span><span class="sxs-lookup"><span data-stu-id="64ee6-213">Microsoft Word 2007</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-214">Приложения Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-214">Microsoft Office 2010 applications</span></span></p>
<p><span data-ttu-id="64ee6-215">( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</span><span class="sxs-lookup"><span data-stu-id="64ee6-215">(<a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)">Download a list of all settings synced</a>)</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-216">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-216">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="64ee6-217">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-217">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="64ee6-218">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-218">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="64ee6-219">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-219">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="64ee6-220">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-220">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="64ee6-221">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-221">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="64ee6-222">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-222">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="64ee6-223">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-223">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="64ee6-224">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-224">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="64ee6-225">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-225">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="64ee6-226">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-226">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="64ee6-227">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-227">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="64ee6-228">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="64ee6-228">Microsoft SharePoint Designer 2010</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-229">Параметры браузера: Internet Explorer 8, Internet Explorer 9 и Internet Explorer 10</span><span class="sxs-lookup"><span data-stu-id="64ee6-229">Browser options: Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-230">Избранное, Домашняя страница, вкладки и панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="64ee6-230">Favorites, home page, tabs, and toolbars.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="64ee6-231">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-231">Note</span></span></strong><br/><p><span data-ttu-id="64ee6-232">UE-V не перемещайте параметры для файлов cookie браузера Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="64ee6-232">UE-V does not roam settings for Internet Explorer cookies.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-233">Аксессуары для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-233">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-234">Microsoft калькулятор, Блокнот, WordPad.</span><span class="sxs-lookup"><span data-stu-id="64ee6-234">Microsoft Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a><span data-ttu-id="64ee6-235">Параметры Windows, синхронизированные по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64ee6-235">Windows settings synchronized by default</span></span>

<span data-ttu-id="64ee6-236">UE-V включает шаблоны расположений параметров, которые захватывают значения параметров для этих параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-236">UE-V includes settings location templates that capture settings values for these Windows settings.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64ee6-237">Параметры Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-237">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="64ee6-238">Описание</span><span class="sxs-lookup"><span data-stu-id="64ee6-238">Description</span></span></th>
<th align="left"><span data-ttu-id="64ee6-239">Применять</span><span class="sxs-lookup"><span data-stu-id="64ee6-239">Apply on</span></span></th>
<th align="left"><span data-ttu-id="64ee6-240">Экспорт включен</span><span class="sxs-lookup"><span data-stu-id="64ee6-240">Export on</span></span></th>
<th align="left"><span data-ttu-id="64ee6-241">Состояние по умолчанию</span><span class="sxs-lookup"><span data-stu-id="64ee6-241">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-242">Фон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="64ee6-242">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-243">Текущий активный фон рабочего стола или фоновый рисунок.</span><span class="sxs-lookup"><span data-stu-id="64ee6-243">Currently active desktop background or wallpaper.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-244">Вход, разблокировка, удаленное подключение, события запланированной задачи.</span><span class="sxs-lookup"><span data-stu-id="64ee6-244">Logon, unlock, remote connect, Scheduled Task events.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-245">Выход, блокировка, удаленное отключение, пользователь нажимает кнопку " <strong> Синхронизировать" </strong> в центре настройки компании или интервал запланированных задач</span><span class="sxs-lookup"><span data-stu-id="64ee6-245">Logoff, lock, remote disconnect, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-246">Включено</span><span class="sxs-lookup"><span data-stu-id="64ee6-246">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-247">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="64ee6-247">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-248">Специальные возможности и параметры ввода, экранная лупа, Экранный диктор и экранная клавиатура.</span><span class="sxs-lookup"><span data-stu-id="64ee6-248">Accessibility and input settings, Microsoft Magnifier, Narrator, and on-Screen Keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-249">Только вход.</span><span class="sxs-lookup"><span data-stu-id="64ee6-249">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-250">Выход из системы, пользователь нажимает кнопку " <strong> Синхронизировать" </strong> в центре параметров компании или интервале запланированной задачи</span><span class="sxs-lookup"><span data-stu-id="64ee6-250">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task interval</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-251">Включено</span><span class="sxs-lookup"><span data-stu-id="64ee6-251">Enabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-252">Параметры рабочего стола</span><span class="sxs-lookup"><span data-stu-id="64ee6-252">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-253">Параметры меню "Пуск" и панели задач, параметры папки, значки рабочего стола по умолчанию, дополнительные часы, параметры региона и языка.</span><span class="sxs-lookup"><span data-stu-id="64ee6-253">Start menu and Taskbar settings, Folder options, Default desktop icons, Additional clocks, and Region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-254">Только вход.</span><span class="sxs-lookup"><span data-stu-id="64ee6-254">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-255">Выход из системы, пользователь нажимает кнопку " <strong> Синхронизировать" </strong> в центре параметров компании или запланированной задачи</span><span class="sxs-lookup"><span data-stu-id="64ee6-255">Logoff, user clicking <strong>Sync Now</strong> in Company Settings Center, or scheduled task</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-256">Включено</span><span class="sxs-lookup"><span data-stu-id="64ee6-256">Enabled</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="64ee6-257">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-257">Note</span></span>**  
<span data-ttu-id="64ee6-258">Начиная с Windows 8, UE-V не перемещайте параметры, связанные с начальным экраном, такими как элементы и места.</span><span class="sxs-lookup"><span data-stu-id="64ee6-258">Starting in Windows 8, UE-V does not roam settings related to the Start screen, such as items and locations.</span></span> <span data-ttu-id="64ee6-259">Кроме того, UE-V не поддерживает синхронизацию закрепленных элементов панели задач или ярлыков файлов Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-259">In addition, UE-V does not support synchronization of pinned taskbar items or Windows file shortcuts.</span></span>



**<span data-ttu-id="64ee6-260">Важно.</span><span class="sxs-lookup"><span data-stu-id="64ee6-260">Important</span></span>**  
<span data-ttu-id="64ee6-261">UE-V 2,1 SP1 перемещает параметры панели задач между устройствами с Windows 10.</span><span class="sxs-lookup"><span data-stu-id="64ee6-261">UE-V 2.1 SP1 roams taskbar settings between Windows 10 devices.</span></span> <span data-ttu-id="64ee6-262">Однако UE-V не синхронизирует параметры панели задач между устройствами и устройствами с Windows 10, работающими на предыдущих операционных системах.</span><span class="sxs-lookup"><span data-stu-id="64ee6-262">However, UE-V does not synchronize taskbar settings between Windows 10 devices and devices running previous operating systems.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="64ee6-263">Группа параметров</span><span class="sxs-lookup"><span data-stu-id="64ee6-263">Settings group</span></span></th>
<th align="left"><span data-ttu-id="64ee6-264">Категория</span><span class="sxs-lookup"><span data-stu-id="64ee6-264">Category</span></span></th>
<th align="left"><span data-ttu-id="64ee6-265">Собирает</span><span class="sxs-lookup"><span data-stu-id="64ee6-265">Capture</span></span></th>
<th align="left"><span data-ttu-id="64ee6-266">Подать заявку</span><span class="sxs-lookup"><span data-stu-id="64ee6-266">Apply</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64ee6-267">Параметры приложения</span><span class="sxs-lookup"><span data-stu-id="64ee6-267">Application Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64ee6-268">Приложения для Windows  </span><span class="sxs-lookup"><span data-stu-id="64ee6-268">Windows apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-269">Закрыть приложение</span><span class="sxs-lookup"><span data-stu-id="64ee6-269">Close app</span></span></p>
<p><span data-ttu-id="64ee6-270">Событие изменения параметров приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-270">Windows app settings change event</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-271">Запуск монитора приложений UE-V при запуске</span><span class="sxs-lookup"><span data-stu-id="64ee6-271">Start the UE-V App Monitor at startup</span></span></p>
<p><span data-ttu-id="64ee6-272">Открыть приложение</span><span class="sxs-lookup"><span data-stu-id="64ee6-272">Open app</span></span></p>
<p><span data-ttu-id="64ee6-273">Событие изменения параметров приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-273">Windows App Settings change event</span></span></p>
<p><span data-ttu-id="64ee6-274">Получение пакета параметров</span><span class="sxs-lookup"><span data-stu-id="64ee6-274">Arrival of a settings package</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="64ee6-275">Классические приложения</span><span class="sxs-lookup"><span data-stu-id="64ee6-275">Desktop applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-276">Приложение закрывается</span><span class="sxs-lookup"><span data-stu-id="64ee6-276">Application closes</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-277">Откроется и закрывается приложение</span><span class="sxs-lookup"><span data-stu-id="64ee6-277">Application opens and closes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="64ee6-278">Параметры рабочего стола</span><span class="sxs-lookup"><span data-stu-id="64ee6-278">Desktop settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="64ee6-279">Фон рабочего стола</span><span class="sxs-lookup"><span data-stu-id="64ee6-279">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-280">Блокировка и выход из системы</span><span class="sxs-lookup"><span data-stu-id="64ee6-280">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-281">Вход, разблокировка, удаленное подключение, уведомление о поступлении нового пакета, пользователь нажимает кнопку <strong> Синхронизировать сейчас </strong> в центре настройки компании или запускается запланированная задача.</span><span class="sxs-lookup"><span data-stu-id="64ee6-281">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="64ee6-282">Простота доступа (обычное — специальные возможности, Экранный диктор, экранная лупа, экранная клавиатура)</span><span class="sxs-lookup"><span data-stu-id="64ee6-282">Ease of Access (Common – Accessibility, Narrator, Magnifier, On-Screen-Keyboard)</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-283">Блокировка и выход из системы</span><span class="sxs-lookup"><span data-stu-id="64ee6-283">Lock or Logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-284">Вторич</span><span class="sxs-lookup"><span data-stu-id="64ee6-284">Logon</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="64ee6-285">Специальные возможности (оболочки-звуковая, доступ, клавиатура, мышь)</span><span class="sxs-lookup"><span data-stu-id="64ee6-285">Ease of Access (Shell - Audio, Accessibility, Keyboard, Mouse)</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-286">Блокировка и выход из системы</span><span class="sxs-lookup"><span data-stu-id="64ee6-286">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-287">Вход, разблокировка, удаленное подключение, уведомление о поступлении нового пакета, пользователь нажимает кнопку " <strong> Синхронизировать сейчас" </strong> в центре параметров компании или запускается запланированное задание</span><span class="sxs-lookup"><span data-stu-id="64ee6-287">Logon, unlock, remote connect, notification of new package arrival, user clicks <strong>Sync Now</strong> in Company Settings Center, or scheduled task runs</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="64ee6-288">Параметры рабочего стола</span><span class="sxs-lookup"><span data-stu-id="64ee6-288">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-289">Блокировка и выход из системы</span><span class="sxs-lookup"><span data-stu-id="64ee6-289">Lock or logoff</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-290">Вторич</span><span class="sxs-lookup"><span data-stu-id="64ee6-290">Logon</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="64ee6-291">Поддержка UE-V для приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-291">UE-V-support for Windows Apps</span></span>

<span data-ttu-id="64ee6-292">Для приложений для Windows разработчик приложения определяет Синхронизируемые параметры.</span><span class="sxs-lookup"><span data-stu-id="64ee6-292">For Windows apps, the app developer specifies the settings that are synchronized.</span></span> <span data-ttu-id="64ee6-293">Вы можете указать, для каких приложений Windows разрешена синхронизация параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-293">You can specify which Windows apps are enabled for settings synchronization.</span></span>

<span data-ttu-id="64ee6-294">Чтобы отобразить список приложений для Windows, которые могут синхронизировать параметры на компьютере с именем семейства пакетов, включенным состоянием и включенным источником, в командной строке Windows PowerShell введите:</span><span class="sxs-lookup"><span data-stu-id="64ee6-294">To display a list of Windows apps that can synchronize settings on a computer with their package family name, enabled status, and enabled source, at a Windows PowerShell command prompt, enter:</span></span> `Get-UevAppxPackage`

**<span data-ttu-id="64ee6-295">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-295">Note</span></span>**  
<span data-ttu-id="64ee6-296">В Windows 8 UE-V не синхронизирует параметры приложения для Windows, если пользователь домена связывает свои учетные данные для входа с учетной записью Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="64ee6-296">As of Windows 8, UE-V does not synchronize Windows app settings if the domain user links their sign-in credentials to their Microsoft Account.</span></span> <span data-ttu-id="64ee6-297">Это связывание синхронизирует параметры в Microsoft OneDrive, так что UE-V отключает синхронизацию параметров приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-297">This linking synchronizes settings to Microsoft OneDrive so UE-V, which disables synchronization of Windows app settings.</span></span>



### <span data-ttu-id="64ee6-298">UE-V-поддержка для перемещаемых принтеров</span><span class="sxs-lookup"><span data-stu-id="64ee6-298">UE-V-support for Roaming Printers</span></span>

<span data-ttu-id="64ee6-299">UE-V 2,1 SP1 позволяет сетевым принтерам перемещаться между устройствами, чтобы пользователь получил доступ к своим сетевым принтерам при входе на любое устройство в сети.</span><span class="sxs-lookup"><span data-stu-id="64ee6-299">UE-V 2.1 SP1 lets network printers roam between devices so that a user has access to their network printers when logged on to any device on the network.</span></span> <span data-ttu-id="64ee6-300">Это включает в себя перемещающий принтер, который они задали по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64ee6-300">This includes roaming the printer that they set as the default.</span></span>

<span data-ttu-id="64ee6-301">Для перемещения принтеров в UE-V требуется один из следующих сценариев:</span><span class="sxs-lookup"><span data-stu-id="64ee6-301">Printer roaming in UE-V requires one of these scenarios:</span></span>

-   <span data-ttu-id="64ee6-302">Сервер печати может загрузить требуемый драйвер при перемещении на новое устройство.</span><span class="sxs-lookup"><span data-stu-id="64ee6-302">The print server can download the required driver when it roams to a new device.</span></span>

-   <span data-ttu-id="64ee6-303">Драйвер для перемещаемого сетевого принтера предварительно установлен на любом устройстве, которому нужен доступ к сетевому принтеру.</span><span class="sxs-lookup"><span data-stu-id="64ee6-303">The driver for the roaming network printer is pre-installed on any device that needs to access that network printer.</span></span>

-   <span data-ttu-id="64ee6-304">Драйвер принтера можно получить из центра обновления Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-304">The printer driver can be obtained from Windows Update.</span></span>

**<span data-ttu-id="64ee6-305">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-305">Note</span></span>**  
<span data-ttu-id="64ee6-306">Функция роуминга принтеров UE-V **не** позволяет перемещать параметры принтера или настройки, например двустороннюю печать.</span><span class="sxs-lookup"><span data-stu-id="64ee6-306">The UE-V printer roaming feature does **not** roam printer settings or preferences, such as printing double-sided.</span></span>



### <a href="" id="determinesettingssync"></a><span data-ttu-id="64ee6-307">Определение того, нужно ли синхронизировать параметры для других приложений</span><span class="sxs-lookup"><span data-stu-id="64ee6-307">Determine whether you need settings synchronized for other applications</span></span>

<span data-ttu-id="64ee6-308">После того как вы просматриваете параметры, которые автоматически синхронизируются в развертывании UE-V, вам нужно решить, нужно ли синхронизировать параметры для других приложений, так как это будет определять способ развертывания UE-V для всего предприятия.</span><span class="sxs-lookup"><span data-stu-id="64ee6-308">After you have reviewed the settings that are synchronized automatically in a UE-V deployment, you want to decide whether you will synchronize settings for other applications since this determines how you deploy UE-V throughout your enterprise.</span></span>

<span data-ttu-id="64ee6-309">Если вы решите, какие из классических приложений следует включить в решение UE-V, вы можете определить, какие параметры можно настраивать для пользователей, а также как и где хранятся параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-309">As an administrator, when you consider which desktop applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="64ee6-310">Не во всех классических приложениях есть параметры, которые можно настроить или настроить для пользователей.</span><span class="sxs-lookup"><span data-stu-id="64ee6-310">Not all desktop applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="64ee6-311">Кроме того, не все параметры приложений для настольных компьютеров можно безопасно синхронизировать на нескольких компьютерах или в разных средах.</span><span class="sxs-lookup"><span data-stu-id="64ee6-311">In addition, not all desktop applications settings can safely be synchronized across multiple computers or environments.</span></span>

<span data-ttu-id="64ee6-312">Как правило, вы можете синхронизировать параметры, отвечающие указанным ниже критериям.</span><span class="sxs-lookup"><span data-stu-id="64ee6-312">In general, you can synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="64ee6-313">Параметры, которые хранятся в расположениях, доступных пользователям.</span><span class="sxs-lookup"><span data-stu-id="64ee6-313">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="64ee6-314">Например, не следует синхронизировать параметры, которые хранятся в папке System32 или в разделе HKEY \ _CURRENT \ _USER (HKCU) реестра.</span><span class="sxs-lookup"><span data-stu-id="64ee6-314">For example, do not synchronize settings that are stored in System32 or outside the HKEY\_CURRENT\_USER (HKCU) section of the registry.</span></span>

-   <span data-ttu-id="64ee6-315">Параметры, не связанные с конкретным компьютером.</span><span class="sxs-lookup"><span data-stu-id="64ee6-315">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="64ee6-316">Например, можно исключить конфигурацию сети или оборудования.</span><span class="sxs-lookup"><span data-stu-id="64ee6-316">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="64ee6-317">Параметры, которые можно синхронизировать между компьютерами без риска повреждения данных.</span><span class="sxs-lookup"><span data-stu-id="64ee6-317">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="64ee6-318">Например, не используйте параметры, которые хранятся в файле базы данных.</span><span class="sxs-lookup"><span data-stu-id="64ee6-318">For example, do not use settings that are stored in a database file.</span></span>

### <a href="" id="checklistsettingssync"></a><span data-ttu-id="64ee6-319">Контрольный список для оценки настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="64ee6-319">Checklist for evaluating custom applications</span></span>

<span data-ttu-id="64ee6-320">Если вы решили, что вам нужны параметры, синхронизированные с другими приложениями, вы можете использовать этот контрольный список, чтобы узнать, какие приложения вы будете включать.</span><span class="sxs-lookup"><span data-stu-id="64ee6-320">If you’ve decided that you need settings synchronized for other applications, you can use this checklist to help figure out which applications you’ll include.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="64ee6-321">Описание</span><span class="sxs-lookup"><span data-stu-id="64ee6-321">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-322">Содержит ли приложение параметры, доступные пользователю для настройки?</span><span class="sxs-lookup"><span data-stu-id="64ee6-322">Does this application contain settings that the user can customize?</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-323">Важно ли пользователю, что эти параметры синхронизированы?</span><span class="sxs-lookup"><span data-stu-id="64ee6-323">Is it important for the user that these settings are synchronized?</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-324">Параметры пользователя уже управляются решением политики управления приложениями или параметрами.</span><span class="sxs-lookup"><span data-stu-id="64ee6-324">Are these user settings already managed by an application management or settings policy solution?</span></span> <span data-ttu-id="64ee6-325">UE-V применяет параметры приложения при запуске приложения и параметры Windows при входе, разблокировании или удаленном подключении.</span><span class="sxs-lookup"><span data-stu-id="64ee6-325">UE-V applies application settings at application startup and Windows settings at logon, unlock, or remote connect events.</span></span> <span data-ttu-id="64ee6-326">Если вы используете UE-V с другими настройками решений для совместного использования, пользователи могут столкнуться с несогласованностью в синхронизированных параметрах.</span><span class="sxs-lookup"><span data-stu-id="64ee6-326">If you use UE-V with other settings sharing solutions, users might experience inconsistency across synchronized settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-327">Специфичны ли параметры приложения для компьютера?</span><span class="sxs-lookup"><span data-stu-id="64ee6-327">Are the application settings specific to the computer?</span></span> <span data-ttu-id="64ee6-328">Настройки приложения и настройки, связанные с оборудованием или конкретными конфигурациями компьютера, не всегда синхронизируются в разных сеансах и могут привести к плохому взаимодействию с приложением.</span><span class="sxs-lookup"><span data-stu-id="64ee6-328">Application preferences and customizations that are associated with hardware or specific computer configurations do not consistently synchronize across sessions and can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-329">Параметры магазина приложений находятся в каталоге Program Files или в каталоге файлов, расположенном в каталоге <strong> Users </strong> [User Name] &lt; strong &gt; </strong> &lt; &gt; LocalLow </strong> Directory.</span><span class="sxs-lookup"><span data-stu-id="64ee6-329">Does the application store settings in the Program Files directory or in the file directory that is located in the <strong>Users</strong>[User name]&lt;strong&gt;AppData</strong>&lt;strong&gt;LocalLow</strong> directory?</span></span> <span data-ttu-id="64ee6-330">Данные приложения, которые хранятся в одном из этих расположений, обычно не синхронизируются с пользователем, так как эти данные являются специфическими для компьютера, или данные слишком велики для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="64ee6-330">Application data that is stored in either of these locations usually should not synchronize with the user, because this data is specific to the computer or because the data is too large to synchronize.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-331">Сохраняет ли приложение все параметры в файле, которые содержат другие данные приложения, которые не должны синхронизироваться?</span><span class="sxs-lookup"><span data-stu-id="64ee6-331">Does the application store any settings in a file that contains other application data that should not synchronize?</span></span> <span data-ttu-id="64ee6-332">UE-V синхронизирует файлы как единый блок.</span><span class="sxs-lookup"><span data-stu-id="64ee6-332">UE-V synchronizes files as a single unit.</span></span> <span data-ttu-id="64ee6-333">Если параметры хранятся в файлах, которые содержат данные приложения, отличные от параметров, то синхронизация этих дополнительных данных может привести к плохому взаимодействию с приложением.</span><span class="sxs-lookup"><span data-stu-id="64ee6-333">If settings are stored in files that include application data other than settings, then synchronizing this additional data can cause a poor application experience.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="64ee6-334">Насколько велики файлы, содержащие параметры?</span><span class="sxs-lookup"><span data-stu-id="64ee6-334">How large are the files that contain the settings?</span></span> <span data-ttu-id="64ee6-335">Производительность синхронизации параметров может зависеть от больших файлов.</span><span class="sxs-lookup"><span data-stu-id="64ee6-335">The performance of the settings synchronization can be affected by large files.</span></span> <span data-ttu-id="64ee6-336">Включение больших файлов может повлиять на производительность синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-336">Including large files can affect the performance of settings synchronization.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a><span data-ttu-id="64ee6-337">Другие факторы, касающиеся подготовки развертывания UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-337">Other Considerations when Preparing a UE-V Deployment</span></span>


<span data-ttu-id="64ee6-338">Вы также должны принимать во время подготовки к развертыванию UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-338">You should also consider these things when you are preparing to deploy UE-V:</span></span>

-   [<span data-ttu-id="64ee6-339">Управление синхронизацией учетных данных</span><span class="sxs-lookup"><span data-stu-id="64ee6-339">Managing credentials synchronization</span></span>](#creds)

-   [<span data-ttu-id="64ee6-340">Синхронизация параметров приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-340">Windows app settings synchronization</span></span>](#appxsettings)

-   [<span data-ttu-id="64ee6-341">Пользовательские шаблоны расположения параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-341">Custom UE-V settings location templates</span></span>](#custom)

-   [<span data-ttu-id="64ee6-342">Непреднамеренное Настройка параметров пользователя</span><span class="sxs-lookup"><span data-stu-id="64ee6-342">Unintentional user settings configurations</span></span>](#prevent)

-   [<span data-ttu-id="64ee6-343">Производительность и емкость</span><span class="sxs-lookup"><span data-stu-id="64ee6-343">Performance and capacity</span></span>](#capacity)

-   [<span data-ttu-id="64ee6-344">Высокая доступность</span><span class="sxs-lookup"><span data-stu-id="64ee6-344">High availability</span></span>](#high)

-   [<span data-ttu-id="64ee6-345">Синхронизация часов компьютера</span><span class="sxs-lookup"><span data-stu-id="64ee6-345">Computer clock synchronization</span></span>](#clocksync)

### <a href="" id="creds"></a><span data-ttu-id="64ee6-346">Управление синхронизацией учетных данных в UE-V 2,1 и UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="64ee6-346">Managing credentials synchronization in UE-V 2.1 and UE-V 2.1 SP1</span></span>

<span data-ttu-id="64ee6-347">Многие корпоративные приложения, в том числе Microsoft Outlook и Lync, запрашивают у пользователей учетные данные домена при входе.</span><span class="sxs-lookup"><span data-stu-id="64ee6-347">Many enterprise applications, including Microsoft Outlook and Lync, prompt users for their domain credentials at login.</span></span> <span data-ttu-id="64ee6-348">Пользователи могут сохранить свои учетные данные на диске, чтобы не вводить их каждый раз при открытии этих приложений.</span><span class="sxs-lookup"><span data-stu-id="64ee6-348">Users have the option of saving their credentials to disk to prevent having to enter them every time they open these applications.</span></span> <span data-ttu-id="64ee6-349">Включение синхронизации перемещаемых учетных данных позволяет пользователям сохранять свои учетные данные на одном компьютере и избегать их повторного ввода на каждом компьютере, который они используют в своей среде.</span><span class="sxs-lookup"><span data-stu-id="64ee6-349">Enabling roaming credentials synchronization lets users save their credentials on one computer and avoid re-entering them on every computer they use in their environment.</span></span> <span data-ttu-id="64ee6-350">Пользователи могут синхронизировать некоторые учетные данные домена с UE-V 2,1 и 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="64ee6-350">Users can synchronize some domain credentials with UE-V 2.1 and 2.1 SP1.</span></span>

**<span data-ttu-id="64ee6-351">Важно.</span><span class="sxs-lookup"><span data-stu-id="64ee6-351">Important</span></span>**  
<span data-ttu-id="64ee6-352">Синхронизация учетных данных отключена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="64ee6-352">Credentials synchronization is disabled by default.</span></span> <span data-ttu-id="64ee6-353">Для реализации этой функции необходимо явным образом включить синхронизацию учетных данных во время развертывания.</span><span class="sxs-lookup"><span data-stu-id="64ee6-353">You must explicitly enable credentials synchronization during deployment to implement this feature.</span></span>



<span data-ttu-id="64ee6-354">UE-V 2,1 и 2,1 SP1 могут синхронизировать корпоративные учетные данные, но не перемещать учетные данные, предназначенные только для использования на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="64ee6-354">UE-V 2.1 and 2.1 SP1 can synchronize enterprise credentials, but do not roam credentials intended only for use on the local computer.</span></span>

<span data-ttu-id="64ee6-355">Учетные данные — это синхронные параметры, то есть они применяются к профилю при первом входе в систему после синхронизации UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-355">Credentials are synchronous settings, meaning they are applied to your profile the first time you log in to your computer after UE-V synchronizes.</span></span>

<span data-ttu-id="64ee6-356">Синхронизация учетных данных осуществляется с помощью собственного шаблона расположений параметров, который по умолчанию отключен.</span><span class="sxs-lookup"><span data-stu-id="64ee6-356">Credentials synchronization is managed by its own settings location template, which is disabled by default.</span></span> <span data-ttu-id="64ee6-357">Вы можете включить или отключить этот шаблон с помощью тех же методов, которые используются для других шаблонов.</span><span class="sxs-lookup"><span data-stu-id="64ee6-357">You can enable or disable this template through the same methods used for other templates.</span></span> <span data-ttu-id="64ee6-358">Идентификатор шаблона для этой функции — RoamingCredentialSettings.</span><span class="sxs-lookup"><span data-stu-id="64ee6-358">The template identifier for this feature is RoamingCredentialSettings.</span></span>

**<span data-ttu-id="64ee6-359">Важно.</span><span class="sxs-lookup"><span data-stu-id="64ee6-359">Important</span></span>**  
<span data-ttu-id="64ee6-360">Если в вашей среде используется перемещение учетных данных Active Directory, рекомендуем не включать шаблон перемещаемых учетных данных UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-360">If you are using Active Directory Credential Roaming in your environment, we recommend that you don’t enable the UE-V credential roaming template.</span></span>



<span data-ttu-id="64ee6-361">Чтобы включить синхронизацию учетных данных, используйте один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="64ee6-361">Use one of these methods to enable credentials synchronization:</span></span>

-   <span data-ttu-id="64ee6-362">Центр параметров компании</span><span class="sxs-lookup"><span data-stu-id="64ee6-362">Company Settings Center</span></span>

-   <span data-ttu-id="64ee6-363">PowerShell</span><span class="sxs-lookup"><span data-stu-id="64ee6-363">PowerShell</span></span>

-   <span data-ttu-id="64ee6-364">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="64ee6-364">Group Policy</span></span>

**<span data-ttu-id="64ee6-365">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-365">Note</span></span>**  
<span data-ttu-id="64ee6-366">Учетные данные шифруются во время синхронизации.</span><span class="sxs-lookup"><span data-stu-id="64ee6-366">Credentials are encrypted during synchronization.</span></span>



<span data-ttu-id="64ee6-367">[Центр настройки компании](https://technet.microsoft.com/library/dn458903.aspx)**:** установите флажок параметры перемещаемых учетных данных в разделе "Параметры Windows", чтобы включить синхронизацию учетных данных.</span><span class="sxs-lookup"><span data-stu-id="64ee6-367">[Company Settings Center](https://technet.microsoft.com/library/dn458903.aspx)**:** Check the Roaming Credential Settings check box under Windows Settings to enable credential synchronization.</span></span> <span data-ttu-id="64ee6-368">Снимите флажок, чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="64ee6-368">Uncheck the box to disable it.</span></span> <span data-ttu-id="64ee6-369">Этот флажок появляется только в центре настройки компании, если ваша учетная запись не настроена для синхронизации параметров с помощью учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="64ee6-369">This check box only appears in Company Settings Center if your account is not configured to synchronize settings using a Microsoft Account.</span></span>

<span data-ttu-id="64ee6-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** этот командлет PowerShell включает синхронизацию учетных данных:</span><span class="sxs-lookup"><span data-stu-id="64ee6-370">[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** This PowerShell cmdlet enables credential synchronization:</span></span>

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="64ee6-371">Этот командлет PowerShell отключает синхронизацию учетных данных:</span><span class="sxs-lookup"><span data-stu-id="64ee6-371">This PowerShell cmdlet disables credential synchronization:</span></span>

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

<span data-ttu-id="64ee6-372">[Групповая политика](https://technet.microsoft.com/library/dn458893.aspx)**:** чтобы включить синхронизацию учетных данных с помощью групповой политики, необходимо [развернуть последний шаблон MDOP ADMX](https://go.microsoft.com/fwlink/p/?LinkId=393944) .</span><span class="sxs-lookup"><span data-stu-id="64ee6-372">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You must [deploy the latest MDOP ADMX template](https://go.microsoft.com/fwlink/p/?LinkId=393944) to enable credential synchronization through group policy.</span></span> <span data-ttu-id="64ee6-373">Синхронизация учетных данных осуществляется с помощью параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-373">Credentials synchronization is managed with the Windows settings.</span></span> <span data-ttu-id="64ee6-374">Чтобы управлять этим компонентом с помощью групповой политики, включите политику синхронизации параметров Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-374">To manage this feature with Group Policy, enable the Synchronize Windows settings policy.</span></span>

1.  <span data-ttu-id="64ee6-375">Откройте редактор групповой политики и перейдите в раздел **Конфигурация пользователя — Административные шаблоны — компоненты Windows — виртуализация взаимодействия с пользователем Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="64ee6-375">Open Group Policy Editor and navigate to **User Configuration – Administrative Templates – Windows Components – Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="64ee6-376">Дважды щелкните элемент **Синхронизация параметров Windows**.</span><span class="sxs-lookup"><span data-stu-id="64ee6-376">Double-click on **Synchronize Windows settings**.</span></span>

3.  <span data-ttu-id="64ee6-377">Если эта политика включена, вы можете включить синхронизацию учетных данных, установив флажок для **перемещаемых учетных данных** , или отключить синхронизацию учетных данных, выполнив их проверку.</span><span class="sxs-lookup"><span data-stu-id="64ee6-377">If this policy is enabled, you can enable credentials synchronization by checking the **Roaming Credentials** check box, or disable credentials synchronization by unchecking it.</span></span>

4.  <span data-ttu-id="64ee6-378">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="64ee6-378">Click **OK**.</span></span>

### <span data-ttu-id="64ee6-379">Хранилища учетных данных, синхронизированные с UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-379">Credential locations synchronized by UE-V</span></span>

<span data-ttu-id="64ee6-380">Синхронизируются файлы учетных данных, сохраненные приложениями, в следующих папках:</span><span class="sxs-lookup"><span data-stu-id="64ee6-380">Credential files saved by applications into the following locations are synchronized:</span></span>

-   <span data-ttu-id="64ee6-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span><span class="sxs-lookup"><span data-stu-id="64ee6-381">%UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials</span></span>\\

-   <span data-ttu-id="64ee6-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span><span class="sxs-lookup"><span data-stu-id="64ee6-382">%UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto</span></span>\\

-   <span data-ttu-id="64ee6-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span><span class="sxs-lookup"><span data-stu-id="64ee6-383">%UserProfile%\\AppData\\Roaming\\Microsoft\\Protect</span></span>\\

-   <span data-ttu-id="64ee6-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span><span class="sxs-lookup"><span data-stu-id="64ee6-384">%UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates</span></span>\\

<span data-ttu-id="64ee6-385">Учетные данные, сохраненные в других папках, не синхронизируются UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-385">Credentials saved to other locations are not synchronized by UE-V.</span></span>

### <a href="" id="appxsettings"></a><span data-ttu-id="64ee6-386">Синхронизация параметров приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-386">Windows app settings synchronization</span></span>

<span data-ttu-id="64ee6-387">UE-V управляет синхронизацией параметров приложений для Windows тремя способами:</span><span class="sxs-lookup"><span data-stu-id="64ee6-387">UE-V manages Windows app settings synchronization in three ways:</span></span>

-   <span data-ttu-id="64ee6-388">**Синхронизация приложений для Windows.** Разрешение и запрет синхронизации приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-388">**Sync Windows Apps:** Allow or deny any Windows app synchronization</span></span>

-   <span data-ttu-id="64ee6-389">**Список приложений для Windows:** Синхронизация списка приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="64ee6-389">**Windows App List:** Synchronize a list of Windows apps</span></span>

-   <span data-ttu-id="64ee6-390">Неуказанные **настройки синхронизации по умолчанию:** Определите поведение синхронизации приложений для Windows, не указанных в списке приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-390">**Unlisted Default Sync Behavior:** Determine the synchronization behavior of Windows apps that are not in the Windows app list.</span></span>

<span data-ttu-id="64ee6-391">Дополнительные сведения можно найти в [списке приложений для Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="64ee6-391">For more information, see the [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

### <a href="" id="custom"></a><span data-ttu-id="64ee6-392">Пользовательские шаблоны расположения параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-392">Custom UE-V settings location templates</span></span>

<span data-ttu-id="64ee6-393">Если вы развертываете UE-V для синхронизации параметров для настраиваемых приложений, вы будете использовать генератор UE-V для создания настраиваемых шаблонов расположений параметров для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="64ee6-393">If you are deploying UE-V to synchronize settings for custom applications, you will use the UE-V Generator to create custom settings location templates for those desktop applications.</span></span> <span data-ttu-id="64ee6-394">После создания и проверки настраиваемого шаблона расположения параметров в тестовой среде вы можете развернуть шаблоны расположений параметров на компьютерах предприятия.</span><span class="sxs-lookup"><span data-stu-id="64ee6-394">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="64ee6-395">Пользовательские шаблоны расположений параметров должны развертываться с помощью существующей инфраструктуры развертывания, например, с помощью метода распространения программного обеспечения в среде System Center Configuration Manager, с настройками, или путем настройки каталога шаблонов параметров UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-395">Custom settings location templates must be deployed with an existing deployment infrastructure, like an enterprise software distribution (ESD) method such as System Center Configuration Manager, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="64ee6-396">Шаблоны, развернутые с помощью Configuration Manager или групповой политики, должны быть зарегистрированы с помощью UE-V WMI или Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64ee6-396">Templates that are deployed with Configuration Manager or Group Policy must be registered by using UE-V WMI or Windows PowerShell.</span></span>

<span data-ttu-id="64ee6-397">Дополнительные сведения о шаблонах расположений пользовательские параметры можно найти в разделе [развертывание UE-V 2. x для настраиваемых приложений](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="64ee6-397">For more information about custom settings location templates, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span> <span data-ttu-id="64ee6-398">Дополнительные сведения об использовании UE-V с Configuration Manager можно найти в разделе [Настройка UE-v 2. x с помощью System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="64ee6-398">For more information about using UE-V with Configuration Manager, see [Configuring UE-V 2.x with System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).</span></span>

### <a href="" id="prevent"></a><span data-ttu-id="64ee6-399">Предотвращение непреднамеренной конфигурации пользовательских параметров</span><span class="sxs-lookup"><span data-stu-id="64ee6-399">Prevent unintentional user settings configuration</span></span>

<span data-ttu-id="64ee6-400">UE-V загружает новые сведения о параметрах пользователей из места хранения параметров и применяет эти параметры к локальному компьютеру в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="64ee6-400">UE-V downloads new user settings information from a settings storage location and applies the settings to the local computer in these instances:</span></span>

-   <span data-ttu-id="64ee6-401">Каждый раз, когда запускается приложение с зарегистрированным шаблоном UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-401">Every time an application is started that has a registered UE-V template.</span></span>

-   <span data-ttu-id="64ee6-402">Когда пользователь входит в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="64ee6-402">When a user logs on to a computer.</span></span>

-   <span data-ttu-id="64ee6-403">Когда пользователь разблокирует компьютер.</span><span class="sxs-lookup"><span data-stu-id="64ee6-403">When a user unlocks a computer.</span></span>

-   <span data-ttu-id="64ee6-404">Подключение к удаленному рабочему столу, на котором установлен UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-404">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

-   <span data-ttu-id="64ee6-405">При выполнении запланированной задачи контроллера синхронизации.</span><span class="sxs-lookup"><span data-stu-id="64ee6-405">When the Sync Controller Application scheduled task is run.</span></span>

<span data-ttu-id="64ee6-406">Если пакет UE-V установлен на компьютере A и на компьютере B, а необходимые для него параметры находятся на компьютере A, необходимо сначала открыть и закрыть приложение на компьютере A.</span><span class="sxs-lookup"><span data-stu-id="64ee6-406">If UE-V is installed on computer A and computer B, and the settings that you want for the application are on computer A, then computer A should open and close the application first.</span></span> <span data-ttu-id="64ee6-407">Если приложение сначала открывается и закрывается на компьютере B, параметры приложения на компьютере A настраиваются на параметры приложения на компьютере B. Синхронизация параметров между компьютерами осуществляется отдельно для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-407">If the application is opened and closed on computer B first, then the application settings on computer A are configured to the application settings on computer B. Settings are synchronized between computers on per-application basis.</span></span> <span data-ttu-id="64ee6-408">С течением времени настройки будут согласовываться между компьютерами при открытии и закрытии с помощью предпочитаемых параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-408">Over time, settings become consistent between computers as they are opened and closed with preferred settings.</span></span>

<span data-ttu-id="64ee6-409">Этот сценарий также применим к параметрам Windows.</span><span class="sxs-lookup"><span data-stu-id="64ee6-409">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="64ee6-410">Если параметры Windows на компьютере B должны совпадать с параметрами Windows на компьютере A, пользователь должен сначала войти в систему и выйти из системы.</span><span class="sxs-lookup"><span data-stu-id="64ee6-410">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should log on and log off computer A first.</span></span>

<span data-ttu-id="64ee6-411">Если пользовательские параметры, необходимые пользователю, применяются в неправильном порядке, их можно восстановить, выполнив операцию восстановления для определенного приложения или конфигурации Windows на компьютере, на котором были переписаны параметры.</span><span class="sxs-lookup"><span data-stu-id="64ee6-411">If the user settings that the user wants are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="64ee6-412">Дополнительные сведения можно найти [в разделе Управление административным резервным копированием и восстановлением в UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span><span class="sxs-lookup"><span data-stu-id="64ee6-412">For more information, see [Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).</span></span>

### <a href="" id="capacity"></a><span data-ttu-id="64ee6-413">Планирование производительности и пропускной способности</span><span class="sxs-lookup"><span data-stu-id="64ee6-413">Performance and capacity planning</span></span>

<span data-ttu-id="64ee6-414">Укажите требования для UE-V со стандартной емкостью диска и наблюдением за работоспособностью сети.</span><span class="sxs-lookup"><span data-stu-id="64ee6-414">Specify your requirements for UE-V with standard disk capacity and network health monitoring.</span></span>

<span data-ttu-id="64ee6-415">UE-V использует общий доступ к блоку сообщений сервера (SMB) для хранения пакетов параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-415">UE-V uses a Server Message Block (SMB) share for the storage of settings packages.</span></span> <span data-ttu-id="64ee6-416">Размер пакетов параметров зависит от параметров, заданных для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-416">The size of settings packages varies depending on the settings information for each application.</span></span> <span data-ttu-id="64ee6-417">Несмотря на то, что большая часть пакетов параметров очень мала, синхронизация потенциально больших файлов, например изображений рабочего стола, может привести к снижению производительности, особенно в медленных сетях.</span><span class="sxs-lookup"><span data-stu-id="64ee6-417">While most settings packages are small, the synchronization of potentially large files, such as desktop images, can result in poor performance, particularly on slower networks.</span></span>

<span data-ttu-id="64ee6-418">Для снижения проблем с задержкой сети создайте места хранения параметров для тех же локальных сетей, где находятся компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="64ee6-418">To reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="64ee6-419">Рекомендуем использовать для хранения параметров 20 МБ свободного места на диске для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="64ee6-419">We recommend 20 MB of disk space per user for the settings storage location.</span></span>

<span data-ttu-id="64ee6-420">По умолчанию синхронизация UE-V истекает через 2 секунды, чтобы предотвратить чрезмерную задержку из-за большого пакета параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-420">By default, UE-V synchronization times out after 2 seconds to prevent excessive lag due to a large settings package.</span></span> <span data-ttu-id="64ee6-421">Вы можете настроить параметр PowerSchool = SyncProvider с помощью [объектов групповой политики](https://technet.microsoft.com/library/dn458893.aspx).</span><span class="sxs-lookup"><span data-stu-id="64ee6-421">You can configure the SyncMethod=SyncProvider setting by using [Group Policy Objects](https://technet.microsoft.com/library/dn458893.aspx).</span></span>

### <a href="" id="high"></a><span data-ttu-id="64ee6-422">Высокий уровень доступности для UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-422">High Availability for UE-V</span></span>

<span data-ttu-id="64ee6-423">Каталог и шаблон параметров для хранилища параметров UE-V поддерживает хранение данных пользователей на любом общем доступе для записи.</span><span class="sxs-lookup"><span data-stu-id="64ee6-423">The UE-V settings storage location and settings template catalog support storing user data on any writable share.</span></span> <span data-ttu-id="64ee6-424">Для обеспечения высокой доступности выполните указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="64ee6-424">To ensure high availability, follow these criteria:</span></span>

-   <span data-ttu-id="64ee6-425">Отформатируйте том хранилища в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="64ee6-425">Format the storage volume with an NTFS file system.</span></span>

-   <span data-ttu-id="64ee6-426">Общий доступ может использовать распределенную файловую систему (DFS), но есть и другие ограничения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-426">The share can use Distributed File System (DFS) but there are restrictions.</span></span>
<span data-ttu-id="64ee6-427">В частности, поддерживается одноцелевая Конфигурация репликации распределенной файловой системы (DFS-R) с пространством имен распределенной файловой системы (DFS-N) или без нее.</span><span class="sxs-lookup"><span data-stu-id="64ee6-427">Specifically, Distributed File System Replication (DFS-R) single target configuration with or without a Distributed File System Namespace (DFS-N) is supported.</span></span>
<span data-ttu-id="64ee6-428">Точно так же поддерживается только одна Целевая конфигурация с помощью DFS-N.</span><span class="sxs-lookup"><span data-stu-id="64ee6-428">Likewise, only single target configuration is supported with DFS-N.</span></span>
<span data-ttu-id="64ee6-429">Подробные сведения можно найти в разделе о [службе технической поддержки Microsoft для реплицированных данных профиля пользователя](https://go.microsoft.com/fwlink/p/?LinkId=313991) , а также о [параметрах поддержки Майкрософт для сценариев развертывания DFS-R и DFS-N](https://support.microsoft.com/kb/2533009).</span><span class="sxs-lookup"><span data-stu-id="64ee6-429">For detailed information, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://go.microsoft.com/fwlink/p/?LinkId=313991) and also [Information about Microsoft support policy for a DFS-R and DFS-N deployment scenario](https://support.microsoft.com/kb/2533009).</span></span>

    <span data-ttu-id="64ee6-430">Кроме того, так как SYSVOL использует DFS-R для репликации, SYSVOL нельзя использовать для репликации файлов данных UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-430">In addition, because SYSVOL uses DFS-R for replication, SYSVOL cannot be used for UE-V data file replication.</span></span>

-   <span data-ttu-id="64ee6-431">Настройка разрешений на доступ к общему ресурсу и списков управления доступом (ACL), указанных в разделе [развертывание места хранения параметров для UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span><span class="sxs-lookup"><span data-stu-id="64ee6-431">Configure the share permissions and NTFS access control lists (ACLs) as specified in [Deploying the Settings Storage Location for UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).</span></span>

-   <span data-ttu-id="64ee6-432">С помощью кластеризации файловых серверов и агента UE-V можно предоставить доступ к копиям данных о состоянии пользователя в случае сбоя связи.</span><span class="sxs-lookup"><span data-stu-id="64ee6-432">Use file server clustering along with the UE-V Agent to provide access to copies of user state data in the event of communications failures.</span></span>

-   <span data-ttu-id="64ee6-433">Вы можете хранить данные пути к хранилищу параметров (данные пользователей) и шаблоны каталогов шаблонов параметров в кластерных ресурсах, а также на ресурсах DFS-N и на обоих.</span><span class="sxs-lookup"><span data-stu-id="64ee6-433">You can store the settings storage path data (user data) and settings template catalog templates on clustered shares, on DFS-N shares, or on both.</span></span>

### <a href="" id="clocksync"></a><span data-ttu-id="64ee6-434">Синхронизация часов компьютера для синхронизации параметров UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-434">Synchronize computer clocks for UE-V settings synchronization</span></span>

<span data-ttu-id="64ee6-435">Компьютеры, на которых запущен агент UE-V Agent, должны использовать сервер времени для обеспечения единообразия параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-435">Computers that run the UE-V Agent must use a time server to maintain a consistent settings experience.</span></span> <span data-ttu-id="64ee6-436">UE-V использует отметки времени, чтобы определить, нужно ли синхронизировать параметры из места хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-436">UE-V uses time stamps to determine if settings must be synchronized from the settings storage location.</span></span> <span data-ttu-id="64ee6-437">Если часы компьютера неверны, более старые параметры могут переопределять более новые параметры, или новые параметры могут быть не сохранены в хранилище параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-437">If the computer clock is inaccurate, older settings can overwrite newer settings, or the new settings might not be saved to the settings storage location.</span></span>

## <a href="" id="prereqs"></a><span data-ttu-id="64ee6-438">Подтверждение предварительных требований и поддерживаемых конфигураций для UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-438">Confirm Prerequisites and Supported Configurations for UE-V</span></span>


<span data-ttu-id="64ee6-439">Прежде чем продолжить, убедитесь в том, что в вашей среде есть требования для выполнения UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-439">Before you proceed, make sure your environment includes these requirements for running UE-V.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="64ee6-440">Операционная система</span><span class="sxs-lookup"><span data-stu-id="64ee6-440">Operating system</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-441">Выпуск</span><span class="sxs-lookup"><span data-stu-id="64ee6-441">Edition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-442">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="64ee6-442">Service pack</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-443">Системная архитектура</span><span class="sxs-lookup"><span data-stu-id="64ee6-443">System architecture</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-444">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="64ee6-444">Windows PowerShell</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="64ee6-445">Microsoft .NET Framework</span><span class="sxs-lookup"><span data-stu-id="64ee6-445">Microsoft .NET Framework</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-446">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="64ee6-446">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-447">Лучшая, Корпоративная или профессиональная версия</span><span class="sxs-lookup"><span data-stu-id="64ee6-447">Ultimate, Enterprise, or Professional Edition</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-448">SP1</span><span class="sxs-lookup"><span data-stu-id="64ee6-448">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-449">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="64ee6-449">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-450">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-450">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-451">Платформа .NET Framework 4,5 или более новой версии для UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="64ee6-451">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="64ee6-452">Платформа .NET Framework 4 или более новой версии для UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="64ee6-452">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-453">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="64ee6-453">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-454">Стандартная, Корпоративная, для центра обработки данных или веб-сервера</span><span class="sxs-lookup"><span data-stu-id="64ee6-454">Standard, Enterprise, Datacenter, or Web Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-455">SP1</span><span class="sxs-lookup"><span data-stu-id="64ee6-455">SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-456">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="64ee6-456">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-457">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-457">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-458">Платформа .NET Framework 4,5 или более новой версии для UE-V 2,1.</span><span class="sxs-lookup"><span data-stu-id="64ee6-458">.NET Framework 4.5 or higher for UE-V 2.1.</span></span></p>
<p><span data-ttu-id="64ee6-459">Платформа .NET Framework 4 или более новой версии для UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="64ee6-459">.NET Framework 4 or higher for UE-V 2.0.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-460">Windows 8 и Windows 8,1</span><span class="sxs-lookup"><span data-stu-id="64ee6-460">Windows 8 and Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-461">Enterprise или Pro</span><span class="sxs-lookup"><span data-stu-id="64ee6-461">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-462">Нет</span><span class="sxs-lookup"><span data-stu-id="64ee6-462">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-463">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="64ee6-463">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-464">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-464">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-465">.NET Framework 4,5 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-465">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-466">Версия Windows 10 до 1607</span><span class="sxs-lookup"><span data-stu-id="64ee6-466">Windows 10, pre-1607 version</span></span></p>
<div class="alert">
<strong><span data-ttu-id="64ee6-467">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-467">Note</span></span></strong><br/><p><span data-ttu-id="64ee6-468">Только UE-V 2,1 SP1 поддерживает Windows 10, версию до 1607</span><span class="sxs-lookup"><span data-stu-id="64ee6-468">Only UE-V 2.1 SP1 supports Windows 10, pre-1607 version</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="64ee6-469">Enterprise или Pro</span><span class="sxs-lookup"><span data-stu-id="64ee6-469">Enterprise or Pro</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-470">Нет</span><span class="sxs-lookup"><span data-stu-id="64ee6-470">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-471">32- или 64-разрядная</span><span class="sxs-lookup"><span data-stu-id="64ee6-471">32-bit or 64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-472">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-472">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-473">.NET Framework 4.6</span><span class="sxs-lookup"><span data-stu-id="64ee6-473">.NET Framework 4.6</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="64ee6-474">Windows Server 2012 и Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="64ee6-474">Windows Server 2012 and Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-475">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="64ee6-475">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-476">Нет</span><span class="sxs-lookup"><span data-stu-id="64ee6-476">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-477">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="64ee6-477">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-478">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-478">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-479">.NET Framework 4,5 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-479">.NET Framework 4.5 or higher</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="64ee6-480">Windows Server2016</span><span class="sxs-lookup"><span data-stu-id="64ee6-480">Windows Server 2016</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-481">Стандартный или центр обработки данных</span><span class="sxs-lookup"><span data-stu-id="64ee6-481">Standard or Datacenter</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-482">Нет</span><span class="sxs-lookup"><span data-stu-id="64ee6-482">None</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-483">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="64ee6-483">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-484">Windows PowerShell 3,0 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-484">Windows PowerShell 3.0 or higher</span></span></p></td>
<td align="left"><p><span data-ttu-id="64ee6-485">.NET Framework 4,6 или более позднюю версию</span><span class="sxs-lookup"><span data-stu-id="64ee6-485">.NET Framework 4.6 or higher</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="64ee6-486">Также...</span><span class="sxs-lookup"><span data-stu-id="64ee6-486">Also…</span></span>

-   <span data-ttu-id="64ee6-487">**Лицензия для MDOP:** Эта технология является частью пакета оптимизации рабочего стола Майкрософт (MDOP).</span><span class="sxs-lookup"><span data-stu-id="64ee6-487">**MDOP License:** This technology is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="64ee6-488">Корпоративные пользователи могут получить MDOP с помощью программы Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="64ee6-488">Enterprise customers can get MDOP with Microsoft Software Assurance.</span></span> <span data-ttu-id="64ee6-489">Дополнительные сведения о программе Software Assurance и приобретении MDOP можно найти в статьях получение MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="64ee6-489">For more information about Microsoft Software Assurance and acquiring MDOP, see How Do I Get MDOP (https://go.microsoft.com/fwlink/p/?LinkId=322049).</span></span>

-   <span data-ttu-id="64ee6-490">**Учетные данные администратора** для компьютера, на котором вы хотите установить</span><span class="sxs-lookup"><span data-stu-id="64ee6-490">**Administrative Credentials** for any computer on which you’ll be installing</span></span>

**<span data-ttu-id="64ee6-491">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-491">Note</span></span>**  

-   <span data-ttu-id="64ee6-492">Начиная с WIndows 10 версии 1607, UE-V входит в состав [Windows 10 для предприятий](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) и больше не входит в состав пакета оптимизации рабочей среды Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="64ee6-492">Starting with WIndows 10, version 1607, UE-V is included with [Windows 10 for Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) and is no longer part of the Microsoft Desktop Optimization Pack.</span></span>

-   <span data-ttu-id="64ee6-493">Для использования Windows PowerShell UE-V Agent агента UE-V требуется, чтобы была включена платформа .NET Framework 4 или выше и Windows PowerShell 3,0 или более новой версии.</span><span class="sxs-lookup"><span data-stu-id="64ee6-493">The UE-V Windows PowerShell feature of the UE-V Agent requires .NET Framework 4 or higher and Windows PowerShell 3.0 or higher to be enabled.</span></span> <span data-ttu-id="64ee6-494">Скачайте Windows PowerShell 3,0 [здесь](https://go.microsoft.com/fwlink/?LinkId=309609).</span><span class="sxs-lookup"><span data-stu-id="64ee6-494">Download Windows PowerShell 3.0 [here](https://go.microsoft.com/fwlink/?LinkId=309609).</span></span>

-   <span data-ttu-id="64ee6-495">Установите платформу .NET Framework 4 или .NET Framework 4,5 на компьютеры под управлением операционной системы Windows 7 или Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="64ee6-495">Install .NET Framework 4 or .NET Framework 4.5 on computers that run the Windows 7 or the Windows Server 2008 R2 operating system.</span></span> <span data-ttu-id="64ee6-496">Операционные системы Windows 8, Windows 8,1 и Windows Server 2012 поставляются с установленной платформой .NET Framework 4,5.</span><span class="sxs-lookup"><span data-stu-id="64ee6-496">The Windows 8, Windows 8.1, and Windows Server 2012 operating systems come with .NET Framework 4.5 installed.</span></span> <span data-ttu-id="64ee6-497">Операционная система Windows 10 поставляется с установленной платформой .NET Framework 4,6.</span><span class="sxs-lookup"><span data-stu-id="64ee6-497">The Windows 10 operating system comes with .NET Framework 4.6 installed.</span></span>
-   <span data-ttu-id="64ee6-498">Политика "удалить перемещаемый кэш" для обязательных профилей не поддерживается UE-V и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="64ee6-498">The “Delete Roaming Cache” policy for Mandatory profiles is not supported with UE-V and should not be used.</span></span>



<span data-ttu-id="64ee6-499">Специальные требования к оперативной памяти (RAM) не относятся к UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-499">There are no special random access memory (RAM) requirements specific to UE-V.</span></span>

### <span data-ttu-id="64ee6-500">Синхронизация параметров с помощью поставщика синхронизации</span><span class="sxs-lookup"><span data-stu-id="64ee6-500">Synchronization of Settings through the Sync Provider</span></span>

<span data-ttu-id="64ee6-501">Поставщик синхронизации — это параметр по умолчанию для пользователей, который синхронизирует локальный кэш с местом хранения параметров в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="64ee6-501">Sync Provider is the default setting for users, which synchronizes a local cache with the settings storage location in these instances:</span></span>

-   <span data-ttu-id="64ee6-502">Вход в систему и выход из нее</span><span class="sxs-lookup"><span data-stu-id="64ee6-502">Logon/logoff</span></span>

-   <span data-ttu-id="64ee6-503">Блокировка и разблокировка</span><span class="sxs-lookup"><span data-stu-id="64ee6-503">Lock/unlock</span></span>

-   <span data-ttu-id="64ee6-504">Подключение к удаленному рабочему столу или отключение</span><span class="sxs-lookup"><span data-stu-id="64ee6-504">Remote desktop connect/disconnect</span></span>

-   <span data-ttu-id="64ee6-505">Открытие или закрытие приложения</span><span class="sxs-lookup"><span data-stu-id="64ee6-505">Application open/close</span></span>

<span data-ttu-id="64ee6-506">Запланированная задача управляет синхронизацией параметров каждые 30 минут или с определенными событиями триггеров для некоторых приложений.</span><span class="sxs-lookup"><span data-stu-id="64ee6-506">A scheduled task manages this synchronization of settings every 30 minutes or through certain trigger events for certain applications.</span></span> <span data-ttu-id="64ee6-507">Дополнительные сведения можно найти [в разделе Изменение частоты запланированных задач UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="64ee6-507">For more information, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="64ee6-508">Агент UE-V Agent синхронизирует параметры пользователей для компьютеров, которые не всегда подключены к корпоративной сети (удаленные компьютеры и переносные компьютеры), и компьютеры, которые всегда подключены к сети (компьютеры, на которых выполняются сеансы связи с Windows Server и хост-интерфейсов виртуальных рабочих столов (VDI)).</span><span class="sxs-lookup"><span data-stu-id="64ee6-508">The UE-V Agent synchronizes user settings for computers that are not always connected to the enterprise network (remote computers and laptops) and computers that are always connected to the network (computers that run Windows Server and host virtual desktop interface (VDI) sessions).</span></span>

<span data-ttu-id="64ee6-509">**Синхронизация для компьютеров с постоянно доступными подключениями:** При использовании UE-V на компьютерах, которые всегда подключены к сети, необходимо настроить агент UE-V для синхронизации параметров с помощью параметра *PowerSchool = None* , который рассчитает сервер хранилища параметров стандартным сетевым общим доступом.</span><span class="sxs-lookup"><span data-stu-id="64ee6-509">**Synchronization for computers with always-available connections:** When you use UE-V on computers that are always connected to the network, you must configure the UE-V Agent to synchronize settings by using the *SyncMethod=None* parameter, which treats the settings storage server as a standard network share.</span></span> <span data-ttu-id="64ee6-510">В этой конфигурации агент UE-V можно настроить таким образом, чтобы уведомить о задержке импорта параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-510">In this configuration, the UE-V Agent can be configured to notify if the import of the application settings is delayed.</span></span>

<span data-ttu-id="64ee6-511">Включите такую конфигурацию одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="64ee6-511">Enable this configuration through one of these methods:</span></span>

-   <span data-ttu-id="64ee6-512">Во время установки UE-V в командной строке или пакетном файле задайте параметр AgentSetup.exe *PowerSchool = None*.</span><span class="sxs-lookup"><span data-stu-id="64ee6-512">During UE-V installation, at the command prompt or in a batch file, set the AgentSetup.exe parameter *SyncMethod = None*.</span></span> <span data-ttu-id="64ee6-513">[Развертывание агента UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) предоставляет дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="64ee6-513">[Deploying the UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) provides more information.</span></span>

-   <span data-ttu-id="64ee6-514">После установки UE-V используйте функцию управления параметрами в System Center 2012 Configuration Manager или в шаблонах MDOP ADMX для принудительной отправки конфигурации *PowerSchool = None* .</span><span class="sxs-lookup"><span data-stu-id="64ee6-514">After the UE-V installation, use the Settings Management feature in System Center 2012 Configuration Manager or the MDOP ADMX templates to push the *SyncMethod = None* configuration.</span></span>

-   <span data-ttu-id="64ee6-515">Используйте Windows PowerShell или инструментарий управления Windows (WMI) для установки конфигурации *PowerSchool = None* .</span><span class="sxs-lookup"><span data-stu-id="64ee6-515">Use Windows PowerShell or Windows Management Instrumentation (WMI) to set the *SyncMethod = None* configuration.</span></span>

    **<span data-ttu-id="64ee6-516">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-516">Note</span></span>**  
    <span data-ttu-id="64ee6-517">Эти два последних способа не работают для сред инфраструктуры виртуальных рабочих столов (VDI) в составе пула.</span><span class="sxs-lookup"><span data-stu-id="64ee6-517">These last two methods do not work for pooled virtual desktop infrastructure (VDI) environments.</span></span>



<span data-ttu-id="64ee6-518">Прежде чем начать синхронизацию, необходимо перезагрузить компьютер.</span><span class="sxs-lookup"><span data-stu-id="64ee6-518">You must restart the computer before the settings start to synchronize.</span></span>

**<span data-ttu-id="64ee6-519">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-519">Note</span></span>**  
<span data-ttu-id="64ee6-520">Если задано значение *PowerSchool = None*, любые изменения параметров сохраняются непосредственно на сервере.</span><span class="sxs-lookup"><span data-stu-id="64ee6-520">If you set *SyncMethod = None*, any settings changes are saved directly to the server.</span></span> <span data-ttu-id="64ee6-521">Если не удается найти сетевое подключение к хранилищу параметров, изменения параметров кэшируются на устройстве и синхронизируются при следующем запуске поставщика синхронизации.</span><span class="sxs-lookup"><span data-stu-id="64ee6-521">If the network connection to the settings storage path is not found, then the settings changes are cached on the device and are synchronized the next time that the sync provider runs.</span></span> <span data-ttu-id="64ee6-522">Если путь к хранилищу параметров не найден, а профиль пользователя удален из среды VDI из пула при выходе из системы, изменения параметров теряются, и пользователь должен повторно применить изменения при повторном подключении компьютера к пути к хранилищу параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-522">If the settings storage path is not found and the user profile is removed from a pooled VDI environment on logoff, settings changes are lost and the user must reapply the change when the computer is reconnected to the settings storage path.</span></span>



<span data-ttu-id="64ee6-523">**Синхронизация для внешних обработчиков синхронизации:** Параметр *PowerSchool = External* указывает на то, что если параметры UE-V записываются в локальную папку на компьютере пользователя, можно использовать любые внешние подсистемы синхронизации (например, OneDrive для бизнеса, рабочие папки, SharePoint или Dropbox) для применения этих параметров к разным компьютерам, к которым пользователи обращаются.</span><span class="sxs-lookup"><span data-stu-id="64ee6-523">**Synchronization for external sync engines:** The *SyncMethod=External* parameter specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

<span data-ttu-id="64ee6-524">**Поддержка общих сеансов VDI.** UE-V 2,1 и 2,1 SP1 предоставляют поддержку для сеансов VDI, которые являются общими для конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="64ee6-524">**Support for shared VDI sessions:** UE-V 2.1 and 2.1 SP1 provide support for VDI sessions that are shared among end users.</span></span> <span data-ttu-id="64ee6-525">Вы можете зарегистрировать и настроить специальный шаблон VDI, который гарантирует, что в UE-V все возможности остаются неизменными для неустойчивых сеансов VDI.</span><span class="sxs-lookup"><span data-stu-id="64ee6-525">You can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

**<span data-ttu-id="64ee6-526">Примечание.</span><span class="sxs-lookup"><span data-stu-id="64ee6-526">Note</span></span>**  
<span data-ttu-id="64ee6-527">Если не включить режим VDI для непостоянных сеансов VDI, некоторые функции не работают, такие как [резервное копирование, восстановление и Загрузка последней удачной (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span><span class="sxs-lookup"><span data-stu-id="64ee6-527">If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as [back-up/restore and last known good (LKG)](https://technet.microsoft.com/library/dn878331.aspx).</span></span>



<span data-ttu-id="64ee6-528">Шаблон VDI предоставляется вместе с UE-V 2,1 и 2,1 SP1 и обычно доступен здесь после установки: C:\\program Files Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span><span class="sxs-lookup"><span data-stu-id="64ee6-528">The VDI template is provided with UE-V 2.1 and 2.1 SP1 and is typically available here after installation: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml</span></span>

### <span data-ttu-id="64ee6-529">Необходимые условия для поддержки генераторов UE-V</span><span class="sxs-lookup"><span data-stu-id="64ee6-529">Prerequisites for UE-V Generator support</span></span>

<span data-ttu-id="64ee6-530">Установите генератор UE-V на компьютере, который используется для создания настраиваемых шаблонов расположений параметров.</span><span class="sxs-lookup"><span data-stu-id="64ee6-530">Install the UE-V Generator on the computer that is used to create custom settings location templates.</span></span> <span data-ttu-id="64ee6-531">Этот компьютер должен иметь возможность запускать приложения, параметры которых синхронизированы.</span><span class="sxs-lookup"><span data-stu-id="64ee6-531">This computer should be able to run the applications whose settings are synchronized.</span></span> <span data-ttu-id="64ee6-532">Вы должны быть участником группы "Администраторы" на компьютере, на котором запущено программное обеспечение для создания генератора UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-532">You must be a member of the Administrators group on the computer that runs the UE-V Generator software.</span></span>

<span data-ttu-id="64ee6-533">На компьютере, на котором используется файловая система NTFS, должен быть установлен генератор UE-V.</span><span class="sxs-lookup"><span data-stu-id="64ee6-533">The UE-V Generator must be installed on a computer that uses an NTFS file system.</span></span> <span data-ttu-id="64ee6-534">Для использования программного обеспечения генератора UE-V требуется платформа .NET Framework 4.</span><span class="sxs-lookup"><span data-stu-id="64ee6-534">The UE-V Generator software requires .NET Framework 4.</span></span> <span data-ttu-id="64ee6-535">Дополнительные сведения можно найти в разделе [развертывание UE-V 2. x для настраиваемых приложений](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="64ee6-535">For more information, see [Deploy UE-V 2.x for Custom Applications](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).</span></span>

## <span data-ttu-id="64ee6-536">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="64ee6-536">Other resources for this product</span></span>


-   [<span data-ttu-id="64ee6-537">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="64ee6-537">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="64ee6-538">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="64ee6-538">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="64ee6-539">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="64ee6-539">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="64ee6-540">Устранение неполадок UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="64ee6-540">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="64ee6-541">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="64ee6-541">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)














