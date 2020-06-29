---
title: Развертывание Microsoft Office 2013 с помощью App-V
description: Развертывание Microsoft Office 2013 с помощью App-V
author: dansimp
ms.assetid: 02df5dc8-79e2-4c5c-8398-dbfb23344ab3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: c57227d531c61949f9160c27fc249db72dbc6523
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814632"
---
# <span data-ttu-id="ee6d9-103">Развертывание Microsoft Office 2013 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="ee6d9-104">В этой статье описано, как использовать Microsoft Application Virtualization 5,0 или более поздних версий для поставки Microsoft Office 2013 как виртуализованных приложений на компьютерах вашей организации.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-104">Use the information in this article to use Microsoft Application Virtualization 5.0, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="ee6d9-105">Сведения о том, как использовать App-V для отправки Office 2010, можно найти в разделе [развертывание Microsoft office 2010 с помощью App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="ee6d9-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v.md).</span></span> <span data-ttu-id="ee6d9-106">Чтобы успешно развернуть Office 2013 с помощью App-V, вам необходимо ознакомиться с Office 2013 и PP-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and pp-V.</span></span>

<span data-ttu-id="ee6d9-107">Этот раздел включает в себя следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="ee6d9-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="ee6d9-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="ee6d9-109">Создание пакета Office 2013 для App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="ee6d9-110">Публикация пакета Office для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-110">Publishing the Office package for App-V 5.0</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="ee6d9-111">Настройка пакетов приложений Office App-V и управление ими</span><span class="sxs-lookup"><span data-stu-id="ee6d9-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="ee6d9-112">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="ee6d9-112">What to know before you start</span></span>


<span data-ttu-id="ee6d9-113">Перед развертыванием Office 2013 с помощью App-V ознакомьтесь со следующими сведениями о планировании.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="ee6d9-114">Поддерживаемые версии Office и сосуществование Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="ee6d9-115">В следующей таблице приведены сведения о поддерживаемых версиях Office и о том, как работать с имеющимися версиями Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-116">Сведения для проверки</span><span class="sxs-lookup"><span data-stu-id="ee6d9-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ee6d9-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="ee6d9-118">Планирование использования App-V с Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ee6d9-119">Поддерживаемые версии Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-120">Поддерживаемые типы развертывания (например, классическое приложение, инфраструктура личных виртуальных рабочих столов (VDI), в составе пула VDI)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-121">Варианты лицензирования Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="ee6d9-122">Планирование использования App-V с Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-123">Рекомендации по установке разных версий Office на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="ee6d9-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="ee6d9-124">Требования к пакетированию, публикации и развертыванию</span><span class="sxs-lookup"><span data-stu-id="ee6d9-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="ee6d9-125">Перед развертыванием Office с помощью App-V ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-126">Задача</span><span class="sxs-lookup"><span data-stu-id="ee6d9-126">Task</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ee6d9-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-128">Создание пакетов</span><span class="sxs-lookup"><span data-stu-id="ee6d9-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ee6d9-129">Все приложения Office, которые вы хотите развернуть для пользователей, должны находиться в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-130">В App-V 5,0 и более поздних версиях для создания пакетов необходимо использовать средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-130">In App-V 5.0 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="ee6d9-131">Нельзя использовать секвенсор.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-132">Если вы развертываете Microsoft Visio 2013 и Microsoft Project 2013 вместе с Office, необходимо включить их в один пакет с Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="ee6d9-133">Дополнительные сведения можно найти в разделе <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> развертывание Visio 2013 и Project 2013 с Office </a> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee6d9-134">Публикация</span><span class="sxs-lookup"><span data-stu-id="ee6d9-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ee6d9-135">Вы можете опубликовать только один пакет Office на каждом клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-136">Необходимо опубликовать пакет Office глобально.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-136">You must publish the Office package globally.</span></span> <span data-ttu-id="ee6d9-137">Вы не можете опубликовать пользователя.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-138">Развертывание любого из перечисленных ниже продуктов на общем компьютере, например с помощью служб удаленных рабочих столов:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee6d9-139">Приложения Microsoft 365 для предприятий</span><span class="sxs-lookup"><span data-stu-id="ee6d9-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-140">Visio Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="ee6d9-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-141">Project Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="ee6d9-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="ee6d9-142">Необходимо включить <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> активацию на общем компьютере </a> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="ee6d9-143">Активация на общем компьютере не используется, если вы разрабатываете продукт корпоративного лицензирования, например:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee6d9-144">Office профессиональный плюс 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-145">Visio профессиональный 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-146">Project профессиональный 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="ee6d9-147">Исключение приложений Office из пакета</span><span class="sxs-lookup"><span data-stu-id="ee6d9-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="ee6d9-148">В приведенной ниже таблице описаны рекомендуемые методы для исключения конкретных приложений Office из пакета.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-149">Задача</span><span class="sxs-lookup"><span data-stu-id="ee6d9-149">Task</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-150">Сведения</span><span class="sxs-lookup"><span data-stu-id="ee6d9-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-151">Используйте <strong> параметр ExcludeApp </strong> при создании пакета с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ee6d9-152">Позволяет исключить из пакета определенные приложения Office, когда средство развертывания Office создаст пакет.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="ee6d9-153">Например, вы можете использовать этот параметр, чтобы создать пакет, содержащий только Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-154">Дополнительные сведения можно найти в разделе <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp element </a> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee6d9-155">Изменение файла DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="ee6d9-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ee6d9-156">Измените файл DeploymentConfig.xml после создания пакета.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="ee6d9-157">Этот файл содержит параметры пакета по умолчанию для всех пользователей на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-158">Дополнительные сведения можно найти в разделе <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> Отключение приложений Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="ee6d9-159">Создание пакета Office 2013 для App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="ee6d9-160">Выполните описанные ниже действия, чтобы создать пакет Office 2013 для App-V 5,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-160">Complete the following steps to create an Office 2013 package for App-V 5.0 or later.</span></span>

**<span data-ttu-id="ee6d9-161">Важно.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-161">Important</span></span>**  
<span data-ttu-id="ee6d9-162">В App-V 5,0 и более поздних версиях необходимо создать пакет с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-162">In App-V 5.0 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="ee6d9-163">Нельзя использовать секвенсор для создания пакетов.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-163">You cannot use the Sequencer to create packages.</span></span>


### <span data-ttu-id="ee6d9-164">Проверка готовности к использованию средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="ee6d9-165">На компьютере, на котором устанавливается средство развертывания Office, должны быть:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-166">Предварительные</span><span class="sxs-lookup"><span data-stu-id="ee6d9-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-167">Описание</span><span class="sxs-lookup"><span data-stu-id="ee6d9-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-168">Необходимое программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="ee6d9-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="ee6d9-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee6d9-170">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="ee6d9-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="ee6d9-171">64-разрядная версия Windows 8</span><span class="sxs-lookup"><span data-stu-id="ee6d9-171">64-bit version of Windows 8</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-172">64-разрядная версия Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee6d9-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


**<span data-ttu-id="ee6d9-173">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-173">Note</span></span>**  
<span data-ttu-id="ee6d9-174">В этой статье термин "пакет приложения Office 2013 App-V" относится к лицензированию подписок и корпоративному лицензированию.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>


### <span data-ttu-id="ee6d9-175">Создание пакетов Office 2013 App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="ee6d9-176">Пакеты App-V для Office 2013 создаются с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="ee6d9-177">Ниже описано, как создать пакет Office 2013 App-V с корпоративным лицензированием или лицензией на подписку.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="ee6d9-178">Создавайте пакеты App-V для Office 2013 на компьютерах с 64-разрядной версией Windows.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="ee6d9-179">После создания пакет App-V для Office 2013 будет работать на компьютерах с Windows 7 и Windows 8, поддерживающих версию 32 и 64.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7 and Windows 8 computers.</span></span>

### <span data-ttu-id="ee6d9-180">Скачать средство развертывания Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="ee6d9-181">Пакеты App-V для Office 2013 создаются с помощью средства развертывания Office, которое создает пакет App-V для Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="ee6d9-182">Пакет нельзя создать или изменить с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="ee6d9-183">Чтобы начать создание пакета, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-183">To begin package creation:</span></span>

1.  <span data-ttu-id="ee6d9-184">Скачайте [средство развертывания Office для приложения "нажми и работай](https://www.microsoft.com/download/details.aspx?id=36778)".</span><span class="sxs-lookup"><span data-stu-id="ee6d9-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="ee6d9-185">Запустите exe исполняемый файл и извлеките его компоненты в нужное место.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="ee6d9-186">Чтобы упростить этот процесс, вы можете создать общую сетевую папку, в которой будут сохраняться функции.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="ee6d9-187">Пример: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="ee6d9-188">Убедитесь в том, что в указанном расположении есть setup.exe и configuration.xml файл.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="ee6d9-189">Загрузка приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-189">Download Office 2013 applications</span></span>

<span data-ttu-id="ee6d9-190">После того как вы загрузили средство развертывания Office, вы можете использовать его для получения последних приложений Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="ee6d9-191">После того как вы получите приложения Office, вы создадите пакет Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="ee6d9-192">XML-файл, который входит в состав средства развертывания Office, определяет сведения о продукте, например языки и приложения Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="ee6d9-193">**Настройте образец XML-файла конфигурации.** Чтобы настроить приложения Office, используйте образец XML-файла конфигурации, который вы загрузили с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="ee6d9-194">Откройте образец XML-файла в блокноте или в любом любимом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="ee6d9-195">После открытия файла примера configuration.xml и его подготовки к редактированию вы можете указать продукты, языки и путь, по которому нужно сохранить приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="ee6d9-196">Ниже приведен простой пример файла configuration.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-196">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      **<span data-ttu-id="ee6d9-197">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-197">Note</span></span>**  
      <span data-ttu-id="ee6d9-198">XML-файл конфигурации — это пример XML-файла.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="ee6d9-199">Файл содержит строки, которые снабжены комментариями. Вы можете "снять комментарий", чтобы настроить дополнительные параметры файла.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>

      <span data-ttu-id="ee6d9-200">Вышеприведенный XML-файл конфигурации указывает на то, что версия Office 2013 ProPlus 32-bit Edition, включая Visio профессиональный плюс, будет загружена на английском языке в \\\\server\\Office 2013 (это расположение, в которое будут сохранены приложения Office).</span><span class="sxs-lookup"><span data-stu-id="ee6d9-200">The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="ee6d9-201">Обратите внимание, что код продукта приложения не влияет на финальное лицензирование Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-201">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="ee6d9-202">Пакеты App-V для Office 2013 с различными лицензированиями можно создавать из одних и тех же приложений, выдавая лицензирование на более поздней стадии.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-202">Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="ee6d9-203">В таблице ниже перечислены настраиваемые атрибуты и элементы XML-файла.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-203">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="ee6d9-204">Ввод</span><span class="sxs-lookup"><span data-stu-id="ee6d9-204">Input</span></span></th>
      <th align="left"><span data-ttu-id="ee6d9-205">Описание</span><span class="sxs-lookup"><span data-stu-id="ee6d9-205">Description</span></span></th>
      <th align="left"><span data-ttu-id="ee6d9-206">Пример.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-206">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="ee6d9-207">Добавить элемент</span><span class="sxs-lookup"><span data-stu-id="ee6d9-207">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-208">Указывает продукты и языки, которые нужно включить в пакет.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-208">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-209">Н/Д</span><span class="sxs-lookup"><span data-stu-id="ee6d9-209">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="ee6d9-210">OfficeClientEdition (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-210">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-211">Указывает выпуск Office 2013, который будет использоваться: с 32 или 64-bit.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-211">Specifies the edition of Office 2013 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="ee6d9-212">Операция завершается сбоем, если <strong> </strong> для OfficeClientEdition не задано допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-212">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="ee6d9-213">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="ee6d9-213">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="ee6d9-214">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="ee6d9-214">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="ee6d9-215">Элемент Product</span><span class="sxs-lookup"><span data-stu-id="ee6d9-215">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-216">Указывает приложение.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-216">Specifies the application.</span></span> <span data-ttu-id="ee6d9-217">Проект 2013 и Visio 2013 должны быть указаны в качестве добавленного продукта для включения в приложения.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-217">Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</span></span></p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
      <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
      <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="ee6d9-218">Элемент Language</span><span class="sxs-lookup"><span data-stu-id="ee6d9-218">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-219">Указывает язык, поддерживаемый в приложениях.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-219">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="ee6d9-220">Версия (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-220">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-221">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-221">Optional.</span></span> <span data-ttu-id="ee6d9-222">Задает сборку, используемую для пакета.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-222">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="ee6d9-223">По умолчанию — это новейшая объявленная сборка (определенная в v32.CAB на источнике Office).</span><span class="sxs-lookup"><span data-stu-id="ee6d9-223">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>15.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="ee6d9-224">Источник (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-224">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="ee6d9-225">Указывает расположение, в которое будут сохраняться приложения.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-225">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2013”</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="ee6d9-226">После редактирования файла configuration.xml, чтобы указать необходимый продукт, язык и расположение, в котором будут сохраняться приложения Office 2013, вы можете сохранить файл конфигурации, например Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-226">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="ee6d9-227">**Скачайте приложения в указанное расположение:** Используйте командную команду с повышенными привилегиями и 64-разрядную операционную систему, чтобы скачать приложения Office 2013, которые позже будут преобразованы в пакет App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-227">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="ee6d9-228">Ниже приведен пример команды с описанием сведений.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-228">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="ee6d9-229">В примере:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-229">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-230">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-230">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-231">— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-231">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-232">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="ee6d9-232">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-233">— Это средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-233">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-234">/Download</span><span class="sxs-lookup"><span data-stu-id="ee6d9-234">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-235">загружает приложения Office 2013, указанные в customConfig.xml файле.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-235">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="ee6d9-236">Эти биты можно позже преобразовать в пакет App-V для Office 2013 с корпоративным лицензированием.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-236">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-237">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ee6d9-237">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-238">передает XML-файл конфигурации, необходимый для завершения процесса загрузки, в этом примере customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-238">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="ee6d9-239">После использования команды скачать приложения Office нужно найти в расположении, указанном в XML-файле конфигурации, в этом примере \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-239">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="ee6d9-240">Преобразование приложений Office в пакет App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-240">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="ee6d9-241">После загрузки приложений Office 2013 с помощью средства развертывания Office с помощью средства развертывания Office можно преобразовать их в пакет приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-241">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="ee6d9-242">Выполните действия, соответствующие вашей модели лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-242">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="ee6d9-243">Общие сведения о том, что вам нужно сделать:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-243">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="ee6d9-244">Создавайте пакеты App-V для Office 2013 на компьютерах с 64-разрядной версией Windows.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-244">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="ee6d9-245">Однако пакет будет работать на компьютерах с операционной системой Windows 7 и Windows 8 (32-64 разрядная версия).</span><span class="sxs-lookup"><span data-stu-id="ee6d9-245">However, the package will run on 32-bit and 64-bit Windows 7 and Windows 8 computers.</span></span>

-   <span data-ttu-id="ee6d9-246">Создайте пакет Office App-V для лицензирования подписки или корпоративного лицензирования с помощью средства развертывания Office, а затем измените файл конфигурации CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-246">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="ee6d9-247">В следующей таблице приведены значения, которые необходимо ввести в файл CustomConfig.xml для модели лицензирования, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-247">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="ee6d9-248">В разделах, которые следуют за таблицей, указаны точные записи, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-248">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-249">Код продукта</span><span class="sxs-lookup"><span data-stu-id="ee6d9-249">Product ID</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-250">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="ee6d9-250">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-251">Лицензирование подписки</span><span class="sxs-lookup"><span data-stu-id="ee6d9-251">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ee6d9-252">Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-252">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-253">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="ee6d9-253">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-254">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="ee6d9-254">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ee6d9-255">Office 2013 с Visio 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-255">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-256">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="ee6d9-256">ProPlusVolume</span></span></p>
<p><span data-ttu-id="ee6d9-257">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="ee6d9-257">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-258">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="ee6d9-258">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="ee6d9-259">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="ee6d9-259">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ee6d9-260">Office 2013 с Visio 2013 и Project 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-260">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-261">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="ee6d9-261">ProPlusVolume</span></span></p>
<p><span data-ttu-id="ee6d9-262">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="ee6d9-262">VisioProVolume</span></span></p>
<p><span data-ttu-id="ee6d9-263">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="ee6d9-263">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-264">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="ee6d9-264">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="ee6d9-265">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="ee6d9-265">VisioProRetail</span></span></p>
<p><span data-ttu-id="ee6d9-266">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="ee6d9-266">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="ee6d9-267">Преобразование приложений Office в пакет App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-267">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="ee6d9-268">В блокноте снова откройте файл CustomConfig.xml и внесите в него указанные ниже изменения.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-268">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="ee6d9-269">Параметр</span><span class="sxs-lookup"><span data-stu-id="ee6d9-269">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="ee6d9-270">Что нужно сделать, чтобы изменить значение на</span><span class="sxs-lookup"><span data-stu-id="ee6d9-270">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="ee6d9-271">Источник</span><span class="sxs-lookup"><span data-stu-id="ee6d9-271">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-272">Наведите указатель мыши на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-272">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="ee6d9-273">ProductID</span><span class="sxs-lookup"><span data-stu-id="ee6d9-273">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-274">Укажите тип лицензирования, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-274">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="ee6d9-275">Лицензирование подписки</span><span class="sxs-lookup"><span data-stu-id="ee6d9-275">Subscription Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="ee6d9-276">В этом примере были сделаны следующие изменения для создания пакета с лицензией на подписку.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-276">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-277">Источник</span><span class="sxs-lookup"><span data-stu-id="ee6d9-277">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-278">— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-278">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-279">Код продукта</span><span class="sxs-lookup"><span data-stu-id="ee6d9-279">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-280">для Office изменено на <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-280">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-281">Код продукта</span><span class="sxs-lookup"><span data-stu-id="ee6d9-281">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-282">для Visio изменено на <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-282">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="ee6d9-283">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="ee6d9-283">Volume Licensing</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p><span data-ttu-id="ee6d9-284">В этом примере были сделаны следующие изменения для создания пакета с помощью программы корпоративного лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-284">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-285">Источник</span><span class="sxs-lookup"><span data-stu-id="ee6d9-285">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-286">— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-286">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-287">Код продукта</span><span class="sxs-lookup"><span data-stu-id="ee6d9-287">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-288">для Office изменено на <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-288">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-289">Код продукта</span><span class="sxs-lookup"><span data-stu-id="ee6d9-289">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-290">для Visio изменено на <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-290">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="ee6d9-291">ExcludeApp (необязательно)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-291">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-292">Позволяет указать программы Office, которые не нужно включать в пакет App-V, создаваемый средством развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-292">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="ee6d9-293">Например, вы можете исключить Access и InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-293">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="ee6d9-294">PACKAGEGUID (необязательно)</span><span class="sxs-lookup"><span data-stu-id="ee6d9-294">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-295">По умолчанию все пакеты App-V, созданные с помощью средства развертывания Office, имеют один и тот же идентификатор пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-295">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="ee6d9-296">Вы можете использовать PACKAGEGUID, чтобы указать другой идентификатор пакета для каждого пакета, который позволяет публиковать несколько пакетов App-V, созданных средством развертывания Office, и управлять ими с помощью сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-296">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="ee6d9-297">Например, если вы хотите использовать этот параметр, если вы создаете разные пакеты для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-297">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="ee6d9-298">Например, вы можете создать пакет с помощью Office 2013 для некоторых пользователей и создать еще один пакет с Office 2013 и Visio 2013 для другого набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-298">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="ee6d9-299">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-299">Note</span></span></strong><br/><p><span data-ttu-id="ee6d9-300">Даже если вы используете уникальные идентификаторы пакетов, вы по-прежнему можете развернуть только один пакет App-V на одном устройстве.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-300">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="ee6d9-301">С помощью команды/packager можно преобразовать приложения Office в пакет Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-301">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="ee6d9-302">Пример</span><span class="sxs-lookup"><span data-stu-id="ee6d9-302">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="ee6d9-303">В примере:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-303">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-304">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-304">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-305">— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-305">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-306">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="ee6d9-306">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-307">— Это средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-307">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-308">/packager</span><span class="sxs-lookup"><span data-stu-id="ee6d9-308">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-309">создает пакет App-V Office 2013 с корпоративным лицензированием, как указано в файле customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-309">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-310">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="ee6d9-310">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-311">передает XML-файл конфигурации (в данном случае customConfig), подготовленный для этапа упаковки.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-311">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="ee6d9-312">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="ee6d9-312">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="ee6d9-313">Указывает расположение только что созданного пакета Office App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-313">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="ee6d9-314">Убедитесь в том, что пакет App-V для Office 2013 правильно работает:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-314">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="ee6d9-315">Опубликуйте пакет App-V Office 2013, созданный глобально, на тестовом компьютере, и убедитесь, что появились ярлыки Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-315">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="ee6d9-316">Запустите несколько приложений Office 2013, например Excel или Word, чтобы убедиться, что пакет работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-316">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="ee6d9-317">Публикация пакета Office для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-317">Publishing the Office package for App-V 5.0</span></span>


<span data-ttu-id="ee6d9-318">Используйте указанные ниже сведения, чтобы опубликовать пакет Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-318">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="ee6d9-319">Методы публикации пакетов приложения Office App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-319">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="ee6d9-320">Развертывание пакета App-V для Office 2013 с помощью тех же способов, которые вы используете для любого другого пакета:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-320">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="ee6d9-321">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ee6d9-321">System Center Configuration Manager</span></span>

-   <span data-ttu-id="ee6d9-322">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-322">App-V Server</span></span>

-   <span data-ttu-id="ee6d9-323">Самостоятельная работа с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee6d9-323">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="ee6d9-324">Необходимые условия и требования к публикации</span><span class="sxs-lookup"><span data-stu-id="ee6d9-324">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-325">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="ee6d9-325">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-326">Сведения</span><span class="sxs-lookup"><span data-stu-id="ee6d9-326">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-327">Включение сценариев PowerShell для клиентов App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-327">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-328">Чтобы опубликовать пакеты Office 2013, необходимо выполнить сценарий.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-328">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="ee6d9-329">Сценарии пакетов по умолчанию отключены для клиентов App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-329">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="ee6d9-330">Чтобы включить сценарии, выполните следующую команду PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-330">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee6d9-331">Публикация пакета Office 2013 в глобальном масштабе</span><span class="sxs-lookup"><span data-stu-id="ee6d9-331">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-332">Точки расширения в пакете Office App-V требуют установки на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-332">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="ee6d9-333">При публикации на уровне компьютера не требуется выполнять необходимые действия или распространяемые компоненты, а пакет Office 2013 глобально позволяет приложениям работать как в исходном установленном Office, устраняя необходимость настраивать пакеты для администраторов.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-333">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="ee6d9-334">Публикация пакета Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-334">How to publish an Office package</span></span>

<span data-ttu-id="ee6d9-335">Выполните следующую команду, чтобы опубликовать пакет Office глобально.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-335">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="ee6d9-336">С консоли управления Веба на сервере App-V можно добавлять разрешения для группы компьютеров, а не для группы пользователей, чтобы пакеты могли публиковаться на компьютерах в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-336">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="ee6d9-337">Настройка пакетов приложений Office App-V и управление ими</span><span class="sxs-lookup"><span data-stu-id="ee6d9-337">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="ee6d9-338">Для управления пакетами Office App-V используйте те же действия, что и для любого другого пакета, но есть несколько исключений, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-338">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="ee6d9-339">Включение подключаемых модулей Office с помощью групп подключений</span><span class="sxs-lookup"><span data-stu-id="ee6d9-339">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="ee6d9-340">Отключение приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-340">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="ee6d9-341">Отключение сочетаний клавиш в Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-341">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="ee6d9-342">Управление обновлениями пакетов Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-342">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="ee6d9-343">Управление обновлениями лицензирования Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-343">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="ee6d9-344">Развертывание Visio 2013 и Project 2013 с Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-344">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="ee6d9-345">Включение подключаемых модулей Office с помощью групп подключений</span><span class="sxs-lookup"><span data-stu-id="ee6d9-345">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="ee6d9-346">Выполните действия, описанные в этом разделе, чтобы включить подключаемые модули Office для пакета Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-346">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="ee6d9-347">Чтобы использовать подключаемые модули Office, необходимо использовать секвенсор App-V для создания отдельного пакета, содержащего только подключаемые модули. Вы не можете использовать средство развертывания Office для создания пакета подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-347">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="ee6d9-348">Затем создайте группу подключения, которая включает пакет Office и пакет подключаемых модулей, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-348">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="ee6d9-349">Чтобы включить подключаемые модули для пакетов Office App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-349">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="ee6d9-350">Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-350">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="ee6d9-351">Поочередные подключаемые модули с помощью секвенсора App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-351">Sequence your plug-ins using the App-V 5.0 Sequencer.</span></span> <span data-ttu-id="ee6d9-352">Убедитесь, что на компьютере, используемом для последовательного подключения к сети, установлен Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-352">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="ee6d9-353">При последовательности подключаемых модулей Office 2013 рекомендуется использовать приложения Microsoft 365 для предприятий (невиртуальные) на компьютере с виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-353">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="ee6d9-354">Создайте пакет App-V 5,0, который содержит нужные подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-354">Create an App-V 5.0 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="ee6d9-355">Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-355">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="ee6d9-356">Добавьте пакет приложений Office 2013 App-V и подключаемый комплект, который вы последовательно расдобавили в группу подключений, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-356">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="ee6d9-357">Важно.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-357">Important</span></span>**  
    <span data-ttu-id="ee6d9-358">Порядок пакетов в группе подключения определяет порядок, в котором будет объединено содержимое пакета.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-358">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="ee6d9-359">В файле-дескрипторе группы подключения сначала добавьте пакет Office 2013 App-V, а затем добавьте пакет App-V для плагина.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-359">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="ee6d9-360">Убедитесь, что оба пакета опубликованы на целевом компьютере, и что пакет Plug-in опубликован глобально, чтобы они соответствовали глобальным параметрам опубликованного пакета Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-360">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="ee6d9-361">Убедитесь в том, что в файле конфигурации развертывания для пакета Plug-in установлены те же параметры, что и в пакете приложения Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-361">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="ee6d9-362">Так как пакет Office 2013 App-V интегрируется с операционной системой, параметры комплекта для подключения должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-362">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="ee6d9-363">Вы можете выполнить поиск по файлу конфигурации развертывания в режиме COM и убедиться, что для пакета подключаемых модулей установлено значение "Интеграция", и что "InProcessEnabled" и "OutOfProcessEnabled" соответствуют параметрам пакета Office 2013 App-V, который вы опубликовали.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-363">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="ee6d9-364">Откройте файл конфигурации развертывания и задайте для параметра значения для **объектов** значение **false**.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-364">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="ee6d9-365">Если вы внесли изменения в файл конфигурации развертывания после выполнения последовательности, убедитесь в том, что пакет Plug-in опубликован с файлом.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-365">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="ee6d9-366">Убедитесь, что созданная группа подключения включена на нужном компьютере.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-366">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="ee6d9-367">Если пакет Office 2013 App-V используется, если группа подключений включена, возможно, созданная группа подключения будет "отложить".</span><span class="sxs-lookup"><span data-stu-id="ee6d9-367">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="ee6d9-368">В этом случае вам потребуется перезагрузить компьютер, чтобы успешно включить группу соединений.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-368">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="ee6d9-369">После успешной публикации обоих пакетов и включения группы подключения запустите целевое приложение Office 2013 и убедитесь, что подключенный и добавленный в группу подключения внешний сервер работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-369">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="ee6d9-370">Отключение приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-370">Disabling Office 2013 applications</span></span>

<span data-ttu-id="ee6d9-371">Вам может потребоваться отключить определенные приложения в пакете Office App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-371">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="ee6d9-372">Например, вы можете отключить Access, но оставить все остальные доступные приложения Office в главном приложении.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-372">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="ee6d9-373">При отключении приложения конечный пользователь больше не увидит ярлык для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-373">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="ee6d9-374">Переупорядочение приложения не требуется.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-374">You do not have to re-sequence the application.</span></span> <span data-ttu-id="ee6d9-375">При изменении файла конфигурации развертывания после публикации пакета Office 2013 App-V необходимо сохранить изменения, добавить пакет приложения Office 2013 и затем повторно опубликовать его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-375">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="ee6d9-376">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-376">Note</span></span>**  
<span data-ttu-id="ee6d9-377">Чтобы исключить определенные приложения Office (например, Access и InfoPath) при создании пакета App-V с помощью средства развертывания Office, используйте параметр **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-377">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="ee6d9-378">Дополнительные сведения можно найти в разделе [ссылки на файл "нажми и работай configuration.xml"](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee6d9-378">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="ee6d9-379">Отключение приложения Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-379">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="ee6d9-380">Откройте файл конфигурации развертывания в текстовом редакторе, например в **блокноте** , и выполните поиск по слову "приложения".</span><span class="sxs-lookup"><span data-stu-id="ee6d9-380">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="ee6d9-381">Найдите приложение Office, которое вы хотите отключить, например Access 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-381">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="ee6d9-382">Измените значение "включено" с "истина" на "ложь".</span><span class="sxs-lookup"><span data-stu-id="ee6d9-382">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="ee6d9-383">Сохраните файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-383">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="ee6d9-384">Добавьте пакет App-V Office 2013 с новым файлом конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-384">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="ee6d9-385">Повторно добавьте пакет Office 2013 App-V, а затем снова опубликуйте его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-385">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="ee6d9-386">Отключение сочетаний клавиш в Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-386">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="ee6d9-387">Вместо отмены публикации или удаления пакета вы можете отключить сочетания клавиш для некоторых приложений Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-387">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="ee6d9-388">В следующем примере показано, как отключить сочетания клавиш для Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-388">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="ee6d9-389">Отключение сочетаний клавиш для приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-389">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="ee6d9-390">Откройте файл конфигурации развертывания в блокноте и выполните поиск по запросу "ярлыки".</span><span class="sxs-lookup"><span data-stu-id="ee6d9-390">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="ee6d9-391">Чтобы отключить определенные сочетания клавиш, удалите или закомментируйте конкретные сочетания клавиш, которые вам не нужны.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-391">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="ee6d9-392">Подсистема должна быть доступна и включена.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-392">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="ee6d9-393">Например, в приведенном ниже примере удалите сочетания клавиш Microsoft Access, сохранив при этом ярлыки/shortcut не &lt; &gt; &lt; &gt; смогут отключить ярлык Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-393">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="ee6d9-394">Сохраните файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-394">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="ee6d9-395">Повторно опубликуйте пакет Office 2013 App-V с новым файлом конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-395">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="ee6d9-396">Многие дополнительные параметры можно изменить, изменив конфигурацию развертывания для пакетов App-V, например сопоставления типов файлов, виртуальной файловой системы и т. д.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-396">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="ee6d9-397">Дополнительные сведения об использовании файлов конфигурации развертывания для изменения параметров пакета App-V можно найти в разделе Дополнительные ресурсы в конце документа.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-397">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="ee6d9-398">Управление обновлениями пакетов Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-398">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="ee6d9-399">Чтобы обновить пакет Office 2013, используйте средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-399">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="ee6d9-400">Чтобы обновить ранее развернутый пакет Office 2013, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-400">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="ee6d9-401">Как обновить ранее развернутый пакет Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-401">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="ee6d9-402">Создайте новый пакет Office 2013 с помощью средства развертывания Office, которое использует самую последнюю версию приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-402">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="ee6d9-403">Последние биты Office 2013 всегда можно получить на этапе загрузки пакета App-V приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-403">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="ee6d9-404">Недавно созданный пакет Office 2013 содержит самые последние обновления и новый идентификатор версии.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-404">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="ee6d9-405">Все пакеты, созданные с помощью средства развертывания Office, имеют одинаковый журнал обращений.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-405">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="ee6d9-406">Примечание.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-406">Note</span></span>**  
    <span data-ttu-id="ee6d9-407">У пакетов Office App-V есть два идентификатора версии:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-407">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="ee6d9-408">Идентификатор версии пакета App-V для Office 2013, уникальный для всех пакетов, созданных с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-408">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="ee6d9-409">Второй идентификатор версии пакета App-V, x. x. x. x, например, в манифесте AppX, который будет изменен только в том случае, если у вас есть новая версия Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-409">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="ee6d9-410">Например, если выпущена новая версия Office 2013 с обновлениями, а пакет создан с помощью средства развертывания Office для включения этих обновлений, номер версии X. X. x. X изменится, чтобы показать, что сама версия Office изменилась.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-410">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="ee6d9-411">Сервер App-V использует номер версии X. X. X. X, чтобы отличать этот пакет и распознать, что он будет содержать новые обновления для ранее опубликованного пакета, и в результате его можно опубликовать как обновление для существующего пакета Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-411">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="ee6d9-412">Глобально опубликуйте созданные пакеты Office 2013 App-V на компьютерах, на которых вы хотите применить новые обновления.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-412">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="ee6d9-413">Так как новый пакет имеет тот же журнал обращений к устаревшему пакету Office 2013 App-V, при публикации нового пакета с обновлениями будут применены только новые изменения старого пакета, поэтому они будут быстрее.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-413">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="ee6d9-414">Обновления будут применены таким же образом для глобальных опубликованных пакетов App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-414">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="ee6d9-415">Так как приложения, скорее всего, будут использоваться, обновления могут быть отложены до тех пор, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-415">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="ee6d9-416">Управление обновлениями лицензирования Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-416">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="ee6d9-417">Если у нового пакета Office 2013 App-V есть лицензия, отличная от уже развернутого пакета App-V для Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-417">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="ee6d9-418">Например, развернутый пакет Office 2013 является подпиской на основе подписки на Office 2013, а новый пакет Office 2013 — на основе корпоративного лицензирования, поэтому для обеспечения беспрепятственного лицензирования необходимо следовать приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-418">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="ee6d9-419">Как обновить лицензию на Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee6d9-419">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="ee6d9-420">Отменить публикацию уже развернутого пакета приложения лицензированных подписок на Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-420">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="ee6d9-421">Удалите неопубликованный пакет приложения для лицензирования подписки на Office 2013.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-421">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="ee6d9-422">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-422">Restart the computer.</span></span>

4.  <span data-ttu-id="ee6d9-423">Добавьте новый пакет корпоративного лицензирования Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-423">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="ee6d9-424">Опубликуйте добавленный пакет App-V Office 2013 с помощью программы корпоративного лицензирования.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-424">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="ee6d9-425">Пакет Office 2013 App-V с выбранным лицензированием будет успешно развернут.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-425">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="ee6d9-426">Развертывание Visio 2013 и Project 2013 с Office</span><span class="sxs-lookup"><span data-stu-id="ee6d9-426">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="ee6d9-427">В таблице ниже описаны требования и параметры для развертывания Visio 2013 и Project 2013 с Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-427">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-428">Задача</span><span class="sxs-lookup"><span data-stu-id="ee6d9-428">Task</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-429">Сведения</span><span class="sxs-lookup"><span data-stu-id="ee6d9-429">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-430">Как упаковать и опубликовать Visio 2013 и Project 2013 с Office?</span><span class="sxs-lookup"><span data-stu-id="ee6d9-430">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-431">Вы должны включить Visio 2013 и Project 2013 в один и тот же пакет для Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-431">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="ee6d9-432">Если вы не развертываете Office, вы можете создать пакет, содержащий Visio и/или Project, при условии, что вы подпишитесь на <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> развертывание Microsoft Office 2010 с помощью App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="ee6d9-432">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee6d9-433">Как развернуть Visio 2013 и Project 2013 для определенных пользователей?</span><span class="sxs-lookup"><span data-stu-id="ee6d9-433">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-434">Воспользуйтесь одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-434">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ee6d9-435">Если вы хотите...</span><span class="sxs-lookup"><span data-stu-id="ee6d9-435">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="ee6d9-436">... затем используйте этот метод</span><span class="sxs-lookup"><span data-stu-id="ee6d9-436">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="ee6d9-437">Создание двух разных пакетов и развертывание каждого из них в другой группе пользователей</span><span class="sxs-lookup"><span data-stu-id="ee6d9-437">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-438">Создание и развертывание следующих пакетов:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-438">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="ee6d9-439">Пакет, содержащий только Office — развертывание на компьютерах, пользователям которых требуется только Office.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-439">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-440">Пакет, содержащий Office, Visio и Project-deploy, на компьютеры, для пользователей которых нужны все три приложения.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-440">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="ee6d9-441">Если вам нужен только один пакет для всей организации или если у вас есть пользователи, которым предоставлен доступ к компьютерам:</span><span class="sxs-lookup"><span data-stu-id="ee6d9-441">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="ee6d9-442">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-442">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="ee6d9-443">Создание пакета, содержащего Office, Visio и Project.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-443">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-444">Развертывание пакета для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-444">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="ee6d9-445">Используйте <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , чтобы запретить определенным пользователям использовать Visio и Project.</span><span class="sxs-lookup"><span data-stu-id="ee6d9-445">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="ee6d9-446">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ee6d9-446">Additional resources</span></span>


**<span data-ttu-id="ee6d9-447">Пакеты Office 2013 App-V 5,0 5,0 дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ee6d9-447">Office 2013 App-V 5.0 Packages 5.0 Additional Resources</span></span>**

[<span data-ttu-id="ee6d9-448">Средство развертывания Office для "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="ee6d9-448">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="ee6d9-449">Поддерживаемые сценарии для развертывания Microsoft Office в последовательном пакете App-V</span><span class="sxs-lookup"><span data-stu-id="ee6d9-449">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="ee6d9-450">Пакеты Office 2010 App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-450">Office 2010 App-V 5.0 Packages</span></span>**

[<span data-ttu-id="ee6d9-451">Комплект виртуализации Microsoft Office 2010 для Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-451">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="ee6d9-452">Известные проблемы, возникающие при создании или использовании пакета Office 2010 для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-452">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="ee6d9-453">Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-453">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="ee6d9-454">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="ee6d9-454">Connection Groups</span></span>**

[<span data-ttu-id="ee6d9-455">Развертывание групп подключений в Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="ee6d9-455">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="ee6d9-456">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="ee6d9-456">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="ee6d9-457">Динамическая настройка</span><span class="sxs-lookup"><span data-stu-id="ee6d9-457">Dynamic Configuration</span></span>**

[<span data-ttu-id="ee6d9-458">Сведения о динамической конфигурации App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ee6d9-458">About App-V 5.0 Dynamic Configuration</span></span>](about-app-v-50-dynamic-configuration.md)














