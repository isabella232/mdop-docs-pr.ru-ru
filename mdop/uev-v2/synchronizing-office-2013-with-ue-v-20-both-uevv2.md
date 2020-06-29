---
title: Синхронизация Office 2013 с UE-V 2,0
description: Синхронизация Office 2013 с UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826889"
---
# <span data-ttu-id="040f7-103">Синхронизация Office 2013 с UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="040f7-103">Synchronizing Office 2013 with UE-V 2.0</span></span>


<span data-ttu-id="040f7-104">Microsoft User Experience Virtualization (UE-V) 2,0 поддерживает синхронизацию параметров приложений Microsoft Office 2013 с помощью шаблона, доступного из коллекции шаблонов UE-V.</span><span class="sxs-lookup"><span data-stu-id="040f7-104">Microsoft User Experience Virtualization (UE-V) 2.0 supports the synchronization of Microsoft Office 2013 application setting using a template available from the UE-V template gallery.</span></span> <span data-ttu-id="040f7-105">Сочетание поддержки UE-V 2 и App-V 5,0 с пакетом обновления 2 (SP2) для Office 2013 профессиональный плюс обеспечивает одинаковый интерфейс для виртуализированного экземпляра Office 2013 с любого устройства или виртуального рабочего стола с поддержкой UE-V.</span><span class="sxs-lookup"><span data-stu-id="040f7-105">The combination of UE-V 2 and App-V 5.0 SP2 support of Office 2013 Professional Plus enables the same experience on virtualized instance of Office 2013 from any UE-V-enabled device or virtualized desktop.</span></span>

<span data-ttu-id="040f7-106">Чтобы активировать поддержку параметров приложений UE-V в Office 2013, вы можете скачать официальные шаблоны UE-V Office 2013 из [коллекции шаблонов Microsoft User Experience Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589).</span><span class="sxs-lookup"><span data-stu-id="040f7-106">To activate UE-V application settings support of Office 2013, you can download official UE-V Office 2013 templates from the [Microsoft User Experience Virtualization (UE-V) 2 Template Gallery](https://go.microsoft.com/fwlink/p/?LinkId=246589).</span></span> <span data-ttu-id="040f7-107">Этот ресурс предоставляет шаблоны расположений параметров Microsoft, разработанные корпорацией Майкрософт, а также шаблоны расположений параметров в сообществе.</span><span class="sxs-lookup"><span data-stu-id="040f7-107">This resource provides Microsoft-authored UE-V settings location templates as well as community-developed settings location templates.</span></span>

## <span data-ttu-id="040f7-108">Поддержка Microsoft Office в UE-V</span><span class="sxs-lookup"><span data-stu-id="040f7-108">Microsoft Office support in UE-V</span></span>


<span data-ttu-id="040f7-109">UE-V 1,0 и UE-V 2 содержат шаблоны расположений параметров для Microsoft Office 2010.</span><span class="sxs-lookup"><span data-stu-id="040f7-109">UE-V 1.0 and UE-V 2 include settings location templates for Microsoft Office 2010.</span></span> <span data-ttu-id="040f7-110">Эти шаблоны распространяются и регистрируются в рамках процесса установки UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="040f7-110">These templates are distributed and registered as part of the UE-V Agent installation process.</span></span> <span data-ttu-id="040f7-111">Эти шаблоны помогают синхронизировать взаимодействие пользователей между устройствами.</span><span class="sxs-lookup"><span data-stu-id="040f7-111">These templates help synchronize users’ Office experience between devices.</span></span> <span data-ttu-id="040f7-112">Шаблоны UE-V для Office 2013 предоставляют очень похожие параметры для шаблонов Office 2010.</span><span class="sxs-lookup"><span data-stu-id="040f7-112">The UE-V templates for Office 2013 provide a very similar settings experience to the templates for Office 2010.</span></span> <span data-ttu-id="040f7-113">Параметры Microsoft Office 2013, перемещенные с помощью Office 365, не включаются в эти параметры.</span><span class="sxs-lookup"><span data-stu-id="040f7-113">Microsoft Office 2013 settings roamed by Office 365 experience are not included in these settings.</span></span> <span data-ttu-id="040f7-114">Список параметров, относящихся к Office 365, можно найти в статье [Обзор параметров пользователей и роуминга для Office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).</span><span class="sxs-lookup"><span data-stu-id="040f7-114">For a list of Office 365-specific settings, see [Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).</span></span>

## <span data-ttu-id="040f7-115">Синхронизированные параметры Office 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-115">Synchronized Office 2013 Settings</span></span>


<span data-ttu-id="040f7-116">В следующих таблицах содержатся сведения о поддержке Office 2013 в UE-V:</span><span class="sxs-lookup"><span data-stu-id="040f7-116">The following tables contain the details for Office 2013 support in UE-V:</span></span>

### <span data-ttu-id="040f7-117">Поддерживаемые шаблоны UE-V для Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="040f7-117">Supported UE-V templates for Microsoft Office</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="040f7-118">Шаблоны Office 2013 (UE-V 2,0, доступные в коллекции UE-V):</span><span class="sxs-lookup"><span data-stu-id="040f7-118">Office 2013 templates (UE-V 2.0, available on UE-V gallery):</span></span></th>
<th align="left"><span data-ttu-id="040f7-119">Шаблоны Office 2010 (UE-V 1,0 &amp; 1,0 SP1):</span><span class="sxs-lookup"><span data-stu-id="040f7-119">Office 2010 templates (UE-V 1.0 &amp; 1.0 SP1):</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="040f7-120">MicrosoftOffice2013Win32.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-120">MicrosoftOffice2013Win32.xml</span></span></p>
<p><span data-ttu-id="040f7-121">MicrosoftOffice2013Win64.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-121">MicrosoftOffice2013Win64.xml</span></span></p>
<p><span data-ttu-id="040f7-122">MicrosoftLync2013Win32.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-122">MicrosoftLync2013Win32.xml</span></span></p>
<p><span data-ttu-id="040f7-123">MicrosoftLync2013Win64.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-123">MicrosoftLync2013Win64.xml</span></span></p></td>
<td align="left"><p><span data-ttu-id="040f7-124">MicrosoftOffice2010Win32.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-124">MicrosoftOffice2010Win32.xml</span></span></p>
<p><span data-ttu-id="040f7-125">MicrosoftOffice2010Win64.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-125">MicrosoftOffice2010Win64.xml</span></span></p>
<p><span data-ttu-id="040f7-126">MicrosoftLync2010.xml</span><span class="sxs-lookup"><span data-stu-id="040f7-126">MicrosoftLync2010.xml</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="040f7-127">Приложения Microsoft Office, поддерживаемые шаблонами UE-V</span><span class="sxs-lookup"><span data-stu-id="040f7-127">Microsoft Office Applications supported by the UE-V templates</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="040f7-128">Microsoft Access 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-128">Microsoft Access 2013</span></span></p>
<p><span data-ttu-id="040f7-129">Microsoft Lync 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-129">Microsoft Lync 2013</span></span></p>
<p><span data-ttu-id="040f7-130">Microsoft Excel 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-130">Microsoft Excel 2013</span></span></p>
<p><span data-ttu-id="040f7-131">Microsoft InfoPath 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-131">Microsoft InfoPath 2013</span></span></p>
<p><span data-ttu-id="040f7-132">Microsoft OneNote 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-132">Microsoft OneNote 2013</span></span></p>
<p><span data-ttu-id="040f7-133">Microsoft Outlook 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-133">Microsoft Outlook 2013</span></span></p>
<p><span data-ttu-id="040f7-134">Microsoft PowerPoint 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-134">Microsoft PowerPoint 2013</span></span></p>
<p><span data-ttu-id="040f7-135">Microsoft Project 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-135">Microsoft Project 2013</span></span></p>
<p><span data-ttu-id="040f7-136">Microsoft Publisher 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-136">Microsoft Publisher 2013</span></span></p>
<p><span data-ttu-id="040f7-137">Microsoft SharePoint Designer 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-137">Microsoft SharePoint Designer 2013</span></span></p>
<p><span data-ttu-id="040f7-138">Microsoft Visio 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-138">Microsoft Visio 2013</span></span></p>
<p><span data-ttu-id="040f7-139">Microsoft Word 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-139">Microsoft Word 2013</span></span></p>
<p><span data-ttu-id="040f7-140">Диспетчер отправки Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="040f7-140">Microsoft Office Upload Manager</span></span></p></td>
<td align="left"><p><span data-ttu-id="040f7-141">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-141">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="040f7-142">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-142">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="040f7-143">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-143">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="040f7-144">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-144">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="040f7-145">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-145">Microsoft OneNote 2010</span></span></p>
<p><span data-ttu-id="040f7-146">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-146">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="040f7-147">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-147">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="040f7-148">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-148">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="040f7-149">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-149">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="040f7-150">Microsoft SharePoint Designer 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-150">Microsoft SharePoint Designer 2010</span></span></p>
<p><span data-ttu-id="040f7-151">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-151">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="040f7-152">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="040f7-152">Microsoft Word 2010</span></span></p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="040f7-153">Развертывание шаблонов Office 2013</span><span class="sxs-lookup"><span data-stu-id="040f7-153">Deploying the Office 2013 templates</span></span>


<span data-ttu-id="040f7-154">Вы можете развернуть шаблон расположения параметров UE-V следующими способами:</span><span class="sxs-lookup"><span data-stu-id="040f7-154">You can deploy UE-V settings location template with the following methods:</span></span>

-   <span data-ttu-id="040f7-155">**Регистрация шаблона с помощью PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="040f7-155">**Registering template via PowerShell**.</span></span> <span data-ttu-id="040f7-156">Если вы используете Windows PowerShell для управления компьютерами, выполните следующую команду Windows PowerShell открыть в качестве администратора, чтобы зарегистрировать этот шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="040f7-156">If you use Windows PowerShell to manage computers, run the following Windows PowerShell command open as an administrator to register this settings location template:</span></span>

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    <span data-ttu-id="040f7-157">Дополнительные сведения об использовании UE-V и Windows PowerShell см. [в разделе Управление шаблонами расположений параметров ue-v 2. x с помощью Windows PowerShell и WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="040f7-157">For more information using UE-V and Windows PowerShell, see [Managing UE-V 2.x Settings Location Templates Using Windows PowerShell and WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).</span></span>

-   <span data-ttu-id="040f7-158">**Зарегистрируйте шаблон с помощью пути к каталогу шаблонов**.</span><span class="sxs-lookup"><span data-stu-id="040f7-158">**Registering template via Template Catalog Path**.</span></span> <span data-ttu-id="040f7-159">Если вы используете путь к каталогу шаблонов параметров для управления шаблонами на компьютерах пользователей, скопируйте шаблон Office 2013 в папку, определенную в агенте UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="040f7-159">If you use the Settings Template Catalog Path to manage templates on users’ computers, copy the Office 2013 template into the folder defined in the UE-V Agent.</span></span> <span data-ttu-id="040f7-160">В следующий раз при выполнении запланированной задачи шаблона "автоматическое обновление" (ApplySettingsCatalog.exe) на устройстве будет зарегистрирован шаблон расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="040f7-160">The next time the Template Auto Update (ApplySettingsCatalog.exe) scheduled task runs, the settings location template will be registered on the device.</span></span> <span data-ttu-id="040f7-161">Дополнительные сведения можно найти [в разделе развертывание каталога шаблонов параметров для UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).</span><span class="sxs-lookup"><span data-stu-id="040f7-161">For more information, see [Deploying the Settings Template Catalog for UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).</span></span>

-   <span data-ttu-id="040f7-162">**Регистрация шаблона с помощью Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="040f7-162">**Registering template via Configuration Manager**.</span></span> <span data-ttu-id="040f7-163">Если вы используете Configuration Manager для управления шаблонами хранилища параметров UE-V, создайте CAB шаблона, импортируйте его в Configuration Manager, а затем выполните развертывание базового плана для клиентов.</span><span class="sxs-lookup"><span data-stu-id="040f7-163">If you use Configuration Manager to manage your UE-V settings storage templates, then recreate the Template Baseline CAB, import it into Configuration Manager, and then deploy the baseline to your clients.</span></span> <span data-ttu-id="040f7-164">Дополнительные сведения можно найти в руководстве, приведенном в документации по [пакету конфигурации System Center 2012 для Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="040f7-164">For more information, see the guidance provided in the documentation for the [System Center 2012 Configuration Pack for Microsoft User Experience Virtualization 2](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






 

 





