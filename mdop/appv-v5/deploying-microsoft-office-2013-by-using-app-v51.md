---
title: Развертывание Microsoft Office 2013 с помощью App-V
description: Развертывание Microsoft Office 2013 с помощью App-V
author: dansimp
ms.assetid: 9a7be05e-2a7a-4874-af25-09c0f5037876
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: f6a54cadce79ff3680fd69206eba8ac3fbe83a68
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814629"
---
# <span data-ttu-id="b233b-103">Развертывание Microsoft Office 2013 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-103">Deploying Microsoft Office 2013 by Using App-V</span></span>


<span data-ttu-id="b233b-104">В этой статье описано, как использовать Microsoft Application Virtualization (App-V) 5,1 или более поздних версий для поставки Microsoft Office 2013 как виртуализированного приложения на компьютерах организации.</span><span class="sxs-lookup"><span data-stu-id="b233b-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2013 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="b233b-105">Сведения о том, как использовать App-V для отправки Office 2010, можно найти в разделе [развертывание Microsoft office 2010 с помощью App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="b233b-105">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span> <span data-ttu-id="b233b-106">Чтобы успешно развернуть Office 2013 с помощью App-V, вам необходимо ознакомиться с Office 2013 и приложением-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-106">To successfully deploy Office 2013 with App-V, you need to be familiar with Office 2013 and App-V.</span></span>

<span data-ttu-id="b233b-107">Этот раздел включает в себя следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="b233b-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b233b-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="b233b-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="b233b-109">Создание пакета Office 2013 для App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="b233b-109">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="b233b-110">Публикация пакета Office для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b233b-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="b233b-111">Настройка пакетов приложений Office App-V и управление ими</span><span class="sxs-lookup"><span data-stu-id="b233b-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="b233b-112">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="b233b-112">What to know before you start</span></span>


<span data-ttu-id="b233b-113">Перед развертыванием Office 2013 с помощью App-V ознакомьтесь со следующими сведениями о планировании.</span><span class="sxs-lookup"><span data-stu-id="b233b-113">Before you deploy Office 2013 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="b233b-114">Поддерживаемые версии Office и сосуществование Office</span><span class="sxs-lookup"><span data-stu-id="b233b-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="b233b-115">В следующей таблице приведены сведения о поддерживаемых версиях Office и о том, как работать с имеющимися версиями Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-116">Сведения для проверки</span><span class="sxs-lookup"><span data-stu-id="b233b-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="b233b-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b233b-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="b233b-118">Планирование использования App-V с Office</span><span class="sxs-lookup"><span data-stu-id="b233b-118">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b233b-119">Поддерживаемые версии Office</span><span class="sxs-lookup"><span data-stu-id="b233b-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="b233b-120">Поддерживаемые типы развертывания (например, классическое приложение, инфраструктура личных виртуальных рабочих столов (VDI), в составе пула VDI)</span><span class="sxs-lookup"><span data-stu-id="b233b-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="b233b-121">Варианты лицензирования Office</span><span class="sxs-lookup"><span data-stu-id="b233b-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office51.md#bkmk-plan-coexisting)"><span data-ttu-id="b233b-122">Планирование использования App-V с Office</span><span class="sxs-lookup"><span data-stu-id="b233b-122">Planning for Using App-V with Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="b233b-123">Рекомендации по установке разных версий Office на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="b233b-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>


### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="b233b-124">Требования к пакетированию, публикации и развертыванию</span><span class="sxs-lookup"><span data-stu-id="b233b-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="b233b-125">Перед развертыванием Office с помощью App-V ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="b233b-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-126">Задача</span><span class="sxs-lookup"><span data-stu-id="b233b-126">Task</span></span></th>
<th align="left"><span data-ttu-id="b233b-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b233b-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-128">Создание пакетов</span><span class="sxs-lookup"><span data-stu-id="b233b-128">Packaging</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b233b-129">Все приложения Office, которые вы хотите развернуть для пользователей, должны находиться в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="b233b-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="b233b-130">В App-V 5,1 и более поздних версиях для создания пакетов необходимо использовать средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="b233b-131">Нельзя использовать секвенсор.</span><span class="sxs-lookup"><span data-stu-id="b233b-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="b233b-132">Если вы развертываете Microsoft Visio 2013 и Microsoft Project 2013 вместе с Office, необходимо включить их в один пакет с Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-132">If you are deploying Microsoft Visio 2013 and Microsoft Project 2013 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="b233b-133">Дополнительные сведения можно найти в разделе <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> развертывание Visio 2013 и Project 2013 с Office </a> .</span><span class="sxs-lookup"><span data-stu-id="b233b-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2013 and Project 2013 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b233b-134">Публикация</span><span class="sxs-lookup"><span data-stu-id="b233b-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b233b-135">Вы можете опубликовать только один пакет Office на каждом клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="b233b-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="b233b-136">Необходимо опубликовать пакет Office глобально.</span><span class="sxs-lookup"><span data-stu-id="b233b-136">You must publish the Office package globally.</span></span> <span data-ttu-id="b233b-137">Вы не можете опубликовать пользователя.</span><span class="sxs-lookup"><span data-stu-id="b233b-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-138">Развертывание любого из перечисленных ниже продуктов на общем компьютере, например с помощью служб удаленных рабочих столов:</span><span class="sxs-lookup"><span data-stu-id="b233b-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="b233b-139">Приложения Microsoft 365 для предприятий</span><span class="sxs-lookup"><span data-stu-id="b233b-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="b233b-140">Visio Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="b233b-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="b233b-141">Project Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="b233b-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="b233b-142">Необходимо включить <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> активацию на общем компьютере </a> .</span><span class="sxs-lookup"><span data-stu-id="b233b-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
<p><span data-ttu-id="b233b-143">Активация на общем компьютере не используется, если вы разрабатываете продукт корпоративного лицензирования, например:</span><span class="sxs-lookup"><span data-stu-id="b233b-143">You don’t use shared computer activation if you’re deploying a volume licensed product, such as:</span></span></p>
<ul>
<li><p><span data-ttu-id="b233b-144">Office профессиональный плюс 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-144">Office Professional Plus 2013</span></span></p></li>
<li><p><span data-ttu-id="b233b-145">Visio профессиональный 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-145">Visio Professional 2013</span></span></p></li>
<li><p><span data-ttu-id="b233b-146">Project профессиональный 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-146">Project Professional 2013</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b233b-147">Исключение приложений Office из пакета</span><span class="sxs-lookup"><span data-stu-id="b233b-147">Excluding Office applications from a package</span></span>

<span data-ttu-id="b233b-148">В приведенной ниже таблице описаны рекомендуемые методы для исключения конкретных приложений Office из пакета.</span><span class="sxs-lookup"><span data-stu-id="b233b-148">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-149">Задача</span><span class="sxs-lookup"><span data-stu-id="b233b-149">Task</span></span></th>
<th align="left"><span data-ttu-id="b233b-150">Сведения</span><span class="sxs-lookup"><span data-stu-id="b233b-150">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-151">Используйте <strong> параметр ExcludeApp </strong> при создании пакета с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-151">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b233b-152">Позволяет исключить из пакета определенные приложения Office, когда средство развертывания Office создаст пакет.</span><span class="sxs-lookup"><span data-stu-id="b233b-152">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="b233b-153">Например, вы можете использовать этот параметр, чтобы создать пакет, содержащий только Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b233b-153">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="b233b-154">Дополнительные сведения можно найти в разделе <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp element </a> .</span><span class="sxs-lookup"><span data-stu-id="b233b-154">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b233b-155">Изменение файла DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="b233b-155">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b233b-156">Измените файл DeploymentConfig.xml после создания пакета.</span><span class="sxs-lookup"><span data-stu-id="b233b-156">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="b233b-157">Этот файл содержит параметры пакета по умолчанию для всех пользователей на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-157">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="b233b-158">Дополнительные сведения можно найти в разделе <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> Отключение приложений Office 2013 </a> .</span><span class="sxs-lookup"><span data-stu-id="b233b-158">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)">Disabling Office 2013 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="b233b-159">Создание пакета Office 2013 для App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="b233b-159">Creating an Office 2013 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="b233b-160">Выполните описанные ниже действия, чтобы создать пакет Office 2013 для App-V 5,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b233b-160">Complete the following steps to create an Office 2013 package for App-V 5.1 or later.</span></span>

**<span data-ttu-id="b233b-161">Важно.</span><span class="sxs-lookup"><span data-stu-id="b233b-161">Important</span></span>**  
<span data-ttu-id="b233b-162">В App-V 5,1 и более поздних версиях необходимо создать пакет с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-162">In App-V 5.1 and later, you must the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="b233b-163">Нельзя использовать секвенсор для создания пакетов.</span><span class="sxs-lookup"><span data-stu-id="b233b-163">You cannot use the Sequencer to create packages.</span></span>



### <span data-ttu-id="b233b-164">Проверка готовности к использованию средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="b233b-164">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="b233b-165">На компьютере, на котором устанавливается средство развертывания Office, должны быть:</span><span class="sxs-lookup"><span data-stu-id="b233b-165">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-166">Предварительные</span><span class="sxs-lookup"><span data-stu-id="b233b-166">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="b233b-167">Описание</span><span class="sxs-lookup"><span data-stu-id="b233b-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-168">Необходимое программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="b233b-168">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-169">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="b233b-169">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b233b-170">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="b233b-170">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="b233b-171">64-разрядная версия Windows 8 или более поздняя</span><span class="sxs-lookup"><span data-stu-id="b233b-171">64-bit version of Windows 8 or later</span></span></p></li>
<li><p><span data-ttu-id="b233b-172">64-разрядная версия Windows 7</span><span class="sxs-lookup"><span data-stu-id="b233b-172">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b233b-173">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b233b-173">Note</span></span>**  
<span data-ttu-id="b233b-174">В этой статье термин "пакет приложения Office 2013 App-V" относится к лицензированию подписок и корпоративному лицензированию.</span><span class="sxs-lookup"><span data-stu-id="b233b-174">In this topic, the term “Office 2013 App-V package” refers to subscription licensing and volume licensing.</span></span>



### <span data-ttu-id="b233b-175">Создание пакетов Office 2013 App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="b233b-175">Create Office 2013 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="b233b-176">Пакеты App-V для Office 2013 создаются с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-176">You create Office 2013 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="b233b-177">Ниже описано, как создать пакет Office 2013 App-V с корпоративным лицензированием или лицензией на подписку.</span><span class="sxs-lookup"><span data-stu-id="b233b-177">The following instructions explain how to create an Office 2013 App-V package with Volume Licensing or Subscription Licensing.</span></span>

<span data-ttu-id="b233b-178">Создавайте пакеты App-V для Office 2013 на компьютерах с 64-разрядной версией Windows.</span><span class="sxs-lookup"><span data-stu-id="b233b-178">Create Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="b233b-179">После создания пакет Office 2013 App-V будет работать на компьютерах с Windows 7, Windows 8,1 и Windows 10, поддерживающих 32-разрядную и 64-разр.</span><span class="sxs-lookup"><span data-stu-id="b233b-179">Once created, the Office 2013 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="b233b-180">Скачать средство развертывания Office</span><span class="sxs-lookup"><span data-stu-id="b233b-180">Download the Office Deployment Tool</span></span>

<span data-ttu-id="b233b-181">Пакеты App-V для Office 2013 создаются с помощью средства развертывания Office, которое создает пакет App-V для Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-181">Office 2013 App-V Packages are created using the Office Deployment Tool, which generates an Office 2013 App-V Package.</span></span> <span data-ttu-id="b233b-182">Пакет нельзя создать или изменить с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-182">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="b233b-183">Чтобы начать создание пакета, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b233b-183">To begin package creation:</span></span>

1.  <span data-ttu-id="b233b-184">Скачайте [средство развертывания Office для приложения "нажми и работай](https://www.microsoft.com/download/details.aspx?id=36778)".</span><span class="sxs-lookup"><span data-stu-id="b233b-184">Download the [Office Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=36778).</span></span>

2.  <span data-ttu-id="b233b-185">Запустите exe исполняемый файл и извлеките его компоненты в нужное место.</span><span class="sxs-lookup"><span data-stu-id="b233b-185">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="b233b-186">Чтобы упростить этот процесс, вы можете создать общую сетевую папку, в которой будут сохраняться функции.</span><span class="sxs-lookup"><span data-stu-id="b233b-186">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    <span data-ttu-id="b233b-187">Пример: \\\\Server\\Office2013</span><span class="sxs-lookup"><span data-stu-id="b233b-187">Example: \\\\Server\\Office2013</span></span>

3.  <span data-ttu-id="b233b-188">Убедитесь в том, что в указанном расположении есть setup.exe и configuration.xml файл.</span><span class="sxs-lookup"><span data-stu-id="b233b-188">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="b233b-189">Загрузка приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-189">Download Office 2013 applications</span></span>

<span data-ttu-id="b233b-190">После того как вы загрузили средство развертывания Office, вы можете использовать его для получения последних приложений Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-190">After you download the Office Deployment Tool, you can use it to get the latest Office 2013 applications.</span></span> <span data-ttu-id="b233b-191">После того как вы получите приложения Office, вы создадите пакет Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-191">After getting the Office applications, you create the Office 2013 App-V package.</span></span>

<span data-ttu-id="b233b-192">XML-файл, который входит в состав средства развертывания Office, определяет сведения о продукте, например языки и приложения Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-192">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1.  <span data-ttu-id="b233b-193">**Настройте образец XML-файла конфигурации.** Чтобы настроить приложения Office, используйте образец XML-файла конфигурации, который вы загрузили с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-193">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

    1.  <span data-ttu-id="b233b-194">Откройте образец XML-файла в блокноте или в любом любимом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="b233b-194">Open the sample XML file in Notepad or your favorite text editor.</span></span>

    2.  <span data-ttu-id="b233b-195">После открытия файла примера configuration.xml и его подготовки к редактированию вы можете указать продукты, языки и путь, по которому нужно сохранить приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-195">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2013 applications.</span></span> <span data-ttu-id="b233b-196">Ниже приведен простой пример файла configuration.xml.</span><span class="sxs-lookup"><span data-stu-id="b233b-196">The following is a basic example of the configuration.xml file:</span></span>

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

        **<span data-ttu-id="b233b-197">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b233b-197">Note</span></span>**  
        <span data-ttu-id="b233b-198">XML-файл конфигурации — это пример XML-файла.</span><span class="sxs-lookup"><span data-stu-id="b233b-198">The configuration XML is a sample XML file.</span></span> <span data-ttu-id="b233b-199">Файл содержит строки, которые снабжены комментариями. Вы можете "снять комментарий", чтобы настроить дополнительные параметры файла.</span><span class="sxs-lookup"><span data-stu-id="b233b-199">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span>



~~~
    The above XML configuration file specifies that Office 2013 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2013, which is the location where Office applications will be saved to. Note that the Product ID of the applications will not affect the final licensing of Office. Office 2013 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage. The table below summarizes the customizable attributes and elements of XML file:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Input</th>
    <th align="left">Description</th>
    <th align="left">Example</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Add element</p></td>
    <td align="left"><p>Specifies the products and languages to include in the package.</p></td>
    <td align="left"><p>N/A</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>OfficeClientEdition (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the edition of Office 2013 product to use: 32-bit or 64-bit. The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</p></td>
    <td align="left"><p><strong>OfficeClientEdition</strong>=&quot;32&quot;</p>
    <p><strong>OfficeClientEdition</strong>=&quot;64&quot;</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Product element</p></td>
    <td align="left"><p>Specifies the application. Project 2013 and Visio 2013 must be specified here as an added product to be included in the applications.</p></td>
    <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
    <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
    <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
    <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
    <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Language element</p></td>
    <td align="left"><p>Specifies the language supported in the applications</p></td>
    <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Version (attribute of Add element)</p></td>
    <td align="left"><p>Optional. Specifies a build to use for the package</p>
    <p>Defaults to latest advertised build (as defined in v32.CAB at the Office source).</p></td>
    <td align="left"><p><code>15.1.2.3</code></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>SourcePath (attribute of Add element)</p></td>
    <td align="left"><p>Specifies the location in which the applications will be saved to.</p></td>
    <td align="left"><p><code>Sourcepath = &quot;\\Server\Office2013”</code></p></td>
    </tr>
    </tbody>
    </table>



    After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2013 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.
~~~

2. <span data-ttu-id="b233b-200">**Скачайте приложения в указанное расположение:** Используйте командную команду с повышенными привилегиями и 64-разрядную операционную систему, чтобы скачать приложения Office 2013, которые позже будут преобразованы в пакет App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-200">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2013 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="b233b-201">Ниже приведен пример команды с описанием сведений.</span><span class="sxs-lookup"><span data-stu-id="b233b-201">Below is an example command with description of details:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   <span data-ttu-id="b233b-202">В примере:</span><span class="sxs-lookup"><span data-stu-id="b233b-202">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-203">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="b233b-203">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-204">— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b233b-204">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b233b-205">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b233b-205">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-206">— Это средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-206">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-207">/Download</span><span class="sxs-lookup"><span data-stu-id="b233b-207">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-208">загружает приложения Office 2013, указанные в customConfig.xml файле.</span><span class="sxs-lookup"><span data-stu-id="b233b-208">downloads the Office 2013 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="b233b-209">Эти биты можно позже преобразовать в пакет App-V для Office 2013 с корпоративным лицензированием.</span><span class="sxs-lookup"><span data-stu-id="b233b-209">These bits can be later converted in an Office 2013 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b233b-210">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b233b-210">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-211">передает XML-файл конфигурации, необходимый для завершения процесса загрузки, в этом примере customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b233b-211">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="b233b-212">После использования команды скачать приложения Office нужно найти в расположении, указанном в XML-файле конфигурации, в этом примере \Server\Office2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-212">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2013.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="b233b-213">Преобразование приложений Office в пакет App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-213">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="b233b-214">После загрузки приложений Office 2013 с помощью средства развертывания Office с помощью средства развертывания Office можно преобразовать их в пакет приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-214">After you download the Office 2013 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2013 App-V package.</span></span> <span data-ttu-id="b233b-215">Выполните действия, соответствующие вашей модели лицензирования.</span><span class="sxs-lookup"><span data-stu-id="b233b-215">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="b233b-216">Общие сведения о том, что вам нужно сделать:</span><span class="sxs-lookup"><span data-stu-id="b233b-216">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="b233b-217">Создавайте пакеты App-V для Office 2013 на компьютерах с 64-разрядной версией Windows.</span><span class="sxs-lookup"><span data-stu-id="b233b-217">Create the Office 2013 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="b233b-218">Однако пакет будет работать на компьютерах с операционной системой Windows 7, Windows 8 и Windows 10, а также на 32-и 64-разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="b233b-218">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8, and Windows 10 computers.</span></span>

-   <span data-ttu-id="b233b-219">Создайте пакет Office App-V для лицензирования подписки или корпоративного лицензирования с помощью средства развертывания Office, а затем измените файл конфигурации CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b233b-219">Create an Office App-V package for either Subscription Licensing package or Volume Licensing by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="b233b-220">В следующей таблице приведены значения, которые необходимо ввести в файл CustomConfig.xml для модели лицензирования, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="b233b-220">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="b233b-221">В разделах, которые следуют за таблицей, указаны точные записи, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b233b-221">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-222">Код продукта</span><span class="sxs-lookup"><span data-stu-id="b233b-222">Product ID</span></span></th>
<th align="left"><span data-ttu-id="b233b-223">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="b233b-223">Volume Licensing</span></span></th>
<th align="left"><span data-ttu-id="b233b-224">Лицензирование подписки</span><span class="sxs-lookup"><span data-stu-id="b233b-224">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b233b-225">Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-225">Office 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b233b-226">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="b233b-226">ProPlusVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-227">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="b233b-227">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b233b-228">Office 2013 с Visio 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-228">Office 2013 with Visio 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b233b-229">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="b233b-229">ProPlusVolume</span></span></p>
<p><span data-ttu-id="b233b-230">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="b233b-230">VisioProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-231">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="b233b-231">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="b233b-232">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="b233b-232">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b233b-233">Office 2013 с Visio 2013 и Project 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-233">Office 2013 with Visio 2013 and Project 2013</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="b233b-234">ProPlusVolume</span><span class="sxs-lookup"><span data-stu-id="b233b-234">ProPlusVolume</span></span></p>
<p><span data-ttu-id="b233b-235">VisioProVolume</span><span class="sxs-lookup"><span data-stu-id="b233b-235">VisioProVolume</span></span></p>
<p><span data-ttu-id="b233b-236">ProjectProVolume</span><span class="sxs-lookup"><span data-stu-id="b233b-236">ProjectProVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-237">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="b233b-237">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="b233b-238">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="b233b-238">VisioProRetail</span></span></p>
<p><span data-ttu-id="b233b-239">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="b233b-239">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="b233b-240">Преобразование приложений Office в пакет App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-240">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="b233b-241">В блокноте снова откройте файл CustomConfig.xml и внесите в него указанные ниже изменения.</span><span class="sxs-lookup"><span data-stu-id="b233b-241">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="b233b-242">Параметр</span><span class="sxs-lookup"><span data-stu-id="b233b-242">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="b233b-243">Что нужно сделать, чтобы изменить значение на</span><span class="sxs-lookup"><span data-stu-id="b233b-243">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b233b-244">Источник</span><span class="sxs-lookup"><span data-stu-id="b233b-244">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b233b-245">Наведите указатель мыши на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="b233b-245">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b233b-246">ProductID</span><span class="sxs-lookup"><span data-stu-id="b233b-246">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b233b-247">Укажите тип лицензирования, как показано в следующих примерах:</span><span class="sxs-lookup"><span data-stu-id="b233b-247">Specify the type of licensing, as shown in the following examples:</span></span></p>
   <ul>
   <li><p><span data-ttu-id="b233b-248">Лицензирование подписки</span><span class="sxs-lookup"><span data-stu-id="b233b-248">Subscription Licensing</span></span></p>
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
   <p><span data-ttu-id="b233b-249">В этом примере были сделаны следующие изменения для создания пакета с лицензией на подписку.</span><span class="sxs-lookup"><span data-stu-id="b233b-249">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-250">Источник</span><span class="sxs-lookup"><span data-stu-id="b233b-250">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-251">— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="b233b-251">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b233b-252">Код продукта</span><span class="sxs-lookup"><span data-stu-id="b233b-252">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-253">для Office изменено на <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="b233b-253">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-254">Код продукта</span><span class="sxs-lookup"><span data-stu-id="b233b-254">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-255">для Visio изменено на <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="b233b-255">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p><span data-ttu-id="b233b-256">Корпоративное лицензирование</span><span class="sxs-lookup"><span data-stu-id="b233b-256">Volume Licensing</span></span></p>
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
   <p><span data-ttu-id="b233b-257">В этом примере были сделаны следующие изменения для создания пакета с помощью программы корпоративного лицензирования.</span><span class="sxs-lookup"><span data-stu-id="b233b-257">In this example, the following changes were made to create a package with Volume licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-258">Источник</span><span class="sxs-lookup"><span data-stu-id="b233b-258">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-259">— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="b233b-259">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b233b-260">Код продукта</span><span class="sxs-lookup"><span data-stu-id="b233b-260">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-261">для Office изменено на <code>ProPlusVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="b233b-261">for Office was changed to <code>ProPlusVolume</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-262">Код продукта</span><span class="sxs-lookup"><span data-stu-id="b233b-262">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-263">для Visio изменено на <code>VisioProVolume</code> .</span><span class="sxs-lookup"><span data-stu-id="b233b-263">for Visio was changed to <code>VisioProVolume</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="b233b-264">ExcludeApp (необязательно)</span><span class="sxs-lookup"><span data-stu-id="b233b-264">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b233b-265">Позволяет указать программы Office, которые не нужно включать в пакет App-V, создаваемый средством развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-265">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="b233b-266">Например, вы можете исключить Access и InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b233b-266">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="b233b-267">PACKAGEGUID (необязательно)</span><span class="sxs-lookup"><span data-stu-id="b233b-267">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="b233b-268">По умолчанию все пакеты App-V, созданные с помощью средства развертывания Office, имеют один и тот же идентификатор пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-268">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="b233b-269">Вы можете использовать PACKAGEGUID, чтобы указать другой идентификатор пакета для каждого пакета, который позволяет публиковать несколько пакетов App-V, созданных средством развертывания Office, и управлять ими с помощью сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-269">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="b233b-270">Например, если вы хотите использовать этот параметр, если вы создаете разные пакеты для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="b233b-270">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="b233b-271">Например, вы можете создать пакет с помощью Office 2013 для некоторых пользователей и создать еще один пакет с Office 2013 и Visio 2013 для другого набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="b233b-271">For example, you can create a package with just Office 2013 for some users, and create another package with Office 2013 and Visio 2013 for another set of users.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="b233b-272">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b233b-272">Note</span></span></strong><br/><p><span data-ttu-id="b233b-273">Даже если вы используете уникальные идентификаторы пакетов, вы по-прежнему можете развернуть только один пакет App-V на одном устройстве.</span><span class="sxs-lookup"><span data-stu-id="b233b-273">Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. <span data-ttu-id="b233b-274">С помощью команды/packager можно преобразовать приложения Office в пакет Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-274">Use the /packager command to convert the Office applications to an Office 2013 App-V package.</span></span>

   <span data-ttu-id="b233b-275">Пример</span><span class="sxs-lookup"><span data-stu-id="b233b-275">For example:</span></span>

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   <span data-ttu-id="b233b-276">В примере:</span><span class="sxs-lookup"><span data-stu-id="b233b-276">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-277">\server\Office2013</span><span class="sxs-lookup"><span data-stu-id="b233b-277">\server\Office2013</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-278">— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b233b-278">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b233b-279">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b233b-279">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-280">— Это средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-280">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-281">/packager</span><span class="sxs-lookup"><span data-stu-id="b233b-281">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-282">создает пакет App-V Office 2013 с корпоративным лицензированием, как указано в файле customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="b233b-282">creates the Office 2013 App-V package with Volume Licensing as specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="b233b-283">\server\Office2013\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="b233b-283">\server\Office2013\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-284">передает XML-файл конфигурации (в данном случае customConfig), подготовленный для этапа упаковки.</span><span class="sxs-lookup"><span data-stu-id="b233b-284">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="b233b-285">\server\share\Office 2013AppV</span><span class="sxs-lookup"><span data-stu-id="b233b-285">\server\share\Office 2013AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="b233b-286">Указывает расположение только что созданного пакета Office App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-286">specifies the location of the newly created Office App-V package.</span></span></p></td>
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



3. <span data-ttu-id="b233b-287">Убедитесь в том, что пакет App-V для Office 2013 правильно работает:</span><span class="sxs-lookup"><span data-stu-id="b233b-287">Verify that the Office 2013 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="b233b-288">Опубликуйте пакет App-V Office 2013, созданный глобально, на тестовом компьютере, и убедитесь, что появились ярлыки Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-288">Publish the Office 2013 App-V package, which you created globally, to a test computer, and verify that the Office 2013 shortcuts appear.</span></span>

   2.  <span data-ttu-id="b233b-289">Запустите несколько приложений Office 2013, например Excel или Word, чтобы убедиться, что пакет работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="b233b-289">Start a few Office 2013 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="b233b-290">Публикация пакета Office для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="b233b-290">Publishing the Office package for App-V 5.1</span></span>


<span data-ttu-id="b233b-291">Используйте указанные ниже сведения, чтобы опубликовать пакет Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-291">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="b233b-292">Методы публикации пакетов приложения Office App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-292">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="b233b-293">Развертывание пакета App-V для Office 2013 с помощью тех же способов, которые вы используете для любого другого пакета:</span><span class="sxs-lookup"><span data-stu-id="b233b-293">Deploy the App-V package for Office 2013 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="b233b-294">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="b233b-294">System Center Configuration Manager</span></span>

-   <span data-ttu-id="b233b-295">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-295">App-V Server</span></span>

-   <span data-ttu-id="b233b-296">Самостоятельная работа с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="b233b-296">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="b233b-297">Необходимые условия и требования к публикации</span><span class="sxs-lookup"><span data-stu-id="b233b-297">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-298">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="b233b-298">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="b233b-299">Сведения</span><span class="sxs-lookup"><span data-stu-id="b233b-299">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-300">Включение сценариев PowerShell для клиентов App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-300">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-301">Чтобы опубликовать пакеты Office 2013, необходимо выполнить сценарий.</span><span class="sxs-lookup"><span data-stu-id="b233b-301">To publish Office 2013 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="b233b-302">Сценарии пакетов по умолчанию отключены для клиентов App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-302">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="b233b-303">Чтобы включить сценарии, выполните следующую команду PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b233b-303">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b233b-304">Публикация пакета Office 2013 в глобальном масштабе</span><span class="sxs-lookup"><span data-stu-id="b233b-304">Publish the Office 2013 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-305">Точки расширения в пакете Office App-V требуют установки на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="b233b-305">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="b233b-306">При публикации на уровне компьютера не требуется выполнять необходимые действия или распространяемые компоненты, а пакет Office 2013 глобально позволяет приложениям работать как в исходном установленном Office, устраняя необходимость настраивать пакеты для администраторов.</span><span class="sxs-lookup"><span data-stu-id="b233b-306">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2013 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="b233b-307">Публикация пакета Office</span><span class="sxs-lookup"><span data-stu-id="b233b-307">How to publish an Office package</span></span>

<span data-ttu-id="b233b-308">Выполните следующую команду, чтобы опубликовать пакет Office глобально.</span><span class="sxs-lookup"><span data-stu-id="b233b-308">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="b233b-309">С консоли управления Веба на сервере App-V можно добавлять разрешения для группы компьютеров, а не для группы пользователей, чтобы пакеты могли публиковаться на компьютерах в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="b233b-309">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="b233b-310">Настройка пакетов приложений Office App-V и управление ими</span><span class="sxs-lookup"><span data-stu-id="b233b-310">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="b233b-311">Для управления пакетами Office App-V используйте те же действия, что и для любого другого пакета, но есть несколько исключений, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="b233b-311">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="b233b-312">Включение подключаемых модулей Office с помощью групп подключений</span><span class="sxs-lookup"><span data-stu-id="b233b-312">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="b233b-313">Отключение приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-313">Disabling Office 2013 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="b233b-314">Отключение сочетаний клавиш в Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-314">Disabling Office 2013 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="b233b-315">Управление обновлениями пакетов Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-315">Managing Office 2013 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="b233b-316">Управление обновлениями лицензирования Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-316">Managing Office 2013 licensing upgrades</span></span>](#bkmk-manage-office-lic-upgrd)

-   [<span data-ttu-id="b233b-317">Развертывание Visio 2013 и Project 2013 с Office</span><span class="sxs-lookup"><span data-stu-id="b233b-317">Deploying Visio 2013 and Project 2013 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="b233b-318">Включение подключаемых модулей Office с помощью групп подключений</span><span class="sxs-lookup"><span data-stu-id="b233b-318">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="b233b-319">Выполните действия, описанные в этом разделе, чтобы включить подключаемые модули Office для пакета Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-319">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="b233b-320">Чтобы использовать подключаемые модули Office, необходимо использовать секвенсор App-V для создания отдельного пакета, содержащего только подключаемые модули. Вы не можете использовать средство развертывания Office для создания пакета подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="b233b-320">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="b233b-321">Затем создайте группу подключения, которая включает пакет Office и пакет подключаемых модулей, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="b233b-321">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="b233b-322">Чтобы включить подключаемые модули для пакетов Office App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-322">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="b233b-323">Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b233b-323">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="b233b-324">Поочередные подключаемые модули с помощью секвенсора App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="b233b-324">Sequence your plug-ins using the App-V 5.1 Sequencer.</span></span> <span data-ttu-id="b233b-325">Убедитесь, что на компьютере, используемом для последовательного подключения к сети, установлен Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-325">Ensure that Office 2013 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="b233b-326">При последовательности подключаемых модулей Office 2013 рекомендуется использовать приложения Microsoft 365 для предприятий (невиртуальные) на компьютере с виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="b233b-326">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2013 plug-ins.</span></span>

3.  <span data-ttu-id="b233b-327">Создайте пакет App-V 5,1, который содержит нужные подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="b233b-327">Create an App-V 5.1 package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="b233b-328">Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b233b-328">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="b233b-329">Добавьте пакет приложений Office 2013 App-V и подключаемый комплект, который вы последовательно расдобавили в группу подключений, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="b233b-329">Add the Office 2013 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    **<span data-ttu-id="b233b-330">Важно.</span><span class="sxs-lookup"><span data-stu-id="b233b-330">Important</span></span>**  
    <span data-ttu-id="b233b-331">Порядок пакетов в группе подключения определяет порядок, в котором будет объединено содержимое пакета.</span><span class="sxs-lookup"><span data-stu-id="b233b-331">The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="b233b-332">В файле-дескрипторе группы подключения сначала добавьте пакет Office 2013 App-V, а затем добавьте пакет App-V для плагина.</span><span class="sxs-lookup"><span data-stu-id="b233b-332">In your Connection group descriptor file, add the Office 2013 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="b233b-333">Убедитесь, что оба пакета опубликованы на целевом компьютере, и что пакет Plug-in опубликован глобально, чтобы они соответствовали глобальным параметрам опубликованного пакета Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-333">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2013 App-V package.</span></span>

7.  <span data-ttu-id="b233b-334">Убедитесь в том, что в файле конфигурации развертывания для пакета Plug-in установлены те же параметры, что и в пакете приложения Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-334">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2013 App-V package has.</span></span>

    <span data-ttu-id="b233b-335">Так как пакет Office 2013 App-V интегрируется с операционной системой, параметры комплекта для подключения должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="b233b-335">Since the Office 2013 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="b233b-336">Вы можете выполнить поиск по файлу конфигурации развертывания в режиме COM и убедиться, что для пакета подключаемых модулей установлено значение "Интеграция", и что "InProcessEnabled" и "OutOfProcessEnabled" соответствуют параметрам пакета Office 2013 App-V, который вы опубликовали.</span><span class="sxs-lookup"><span data-stu-id="b233b-336">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2013 App-V package you published.</span></span>

8.  <span data-ttu-id="b233b-337">Откройте файл конфигурации развертывания и задайте для параметра значения для **объектов** значение **false**.</span><span class="sxs-lookup"><span data-stu-id="b233b-337">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="b233b-338">Если вы внесли изменения в файл конфигурации развертывания после выполнения последовательности, убедитесь в том, что пакет Plug-in опубликован с файлом.</span><span class="sxs-lookup"><span data-stu-id="b233b-338">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="b233b-339">Убедитесь, что созданная группа подключения включена на нужном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b233b-339">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="b233b-340">Если пакет Office 2013 App-V используется, если группа подключений включена, возможно, созданная группа подключения будет "отложить".</span><span class="sxs-lookup"><span data-stu-id="b233b-340">The Connection Group created will likely “pend” if the Office 2013 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="b233b-341">В этом случае вам потребуется перезагрузить компьютер, чтобы успешно включить группу соединений.</span><span class="sxs-lookup"><span data-stu-id="b233b-341">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="b233b-342">После успешной публикации обоих пакетов и включения группы подключения запустите целевое приложение Office 2013 и убедитесь, что подключенный и добавленный в группу подключения внешний сервер работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="b233b-342">After you successfully publish both packages and enable the Connection Group, start the target Office 2013 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="b233b-343">Отключение приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-343">Disabling Office 2013 applications</span></span>

<span data-ttu-id="b233b-344">Вам может потребоваться отключить определенные приложения в пакете Office App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-344">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="b233b-345">Например, вы можете отключить Access, но оставить все остальные доступные приложения Office в главном приложении.</span><span class="sxs-lookup"><span data-stu-id="b233b-345">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="b233b-346">При отключении приложения конечный пользователь больше не увидит ярлык для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="b233b-346">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="b233b-347">Переупорядочение приложения не требуется.</span><span class="sxs-lookup"><span data-stu-id="b233b-347">You do not have to re-sequence the application.</span></span> <span data-ttu-id="b233b-348">При изменении файла конфигурации развертывания после публикации пакета Office 2013 App-V необходимо сохранить изменения, добавить пакет приложения Office 2013 и затем повторно опубликовать его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-348">When you change the Deployment Configuration File after the Office 2013 App-V package has been published, you will save the changes, add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

**<span data-ttu-id="b233b-349">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b233b-349">Note</span></span>**  
<span data-ttu-id="b233b-350">Чтобы исключить определенные приложения Office (например, Access и InfoPath) при создании пакета App-V с помощью средства развертывания Office, используйте параметр **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="b233b-350">To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span> <span data-ttu-id="b233b-351">Дополнительные сведения можно найти в разделе [ссылки на файл "нажми и работай configuration.xml"](https://technet.microsoft.com/library/jj219426.aspx).</span><span class="sxs-lookup"><span data-stu-id="b233b-351">For more information, see [Reference for Click-to-Run configuration.xml file](https://technet.microsoft.com/library/jj219426.aspx).</span></span>



**<span data-ttu-id="b233b-352">Отключение приложения Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-352">To disable an Office 2013 application</span></span>**

1.  <span data-ttu-id="b233b-353">Откройте файл конфигурации развертывания в текстовом редакторе, например в **блокноте** , и выполните поиск по слову "приложения".</span><span class="sxs-lookup"><span data-stu-id="b233b-353">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="b233b-354">Найдите приложение Office, которое вы хотите отключить, например Access 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-354">Search for the Office application you want to disable, for example, Access 2013.</span></span>

3.  <span data-ttu-id="b233b-355">Измените значение "включено" с "истина" на "ложь".</span><span class="sxs-lookup"><span data-stu-id="b233b-355">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="b233b-356">Сохраните файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="b233b-356">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="b233b-357">Добавьте пакет App-V Office 2013 с новым файлом конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="b233b-357">Add the Office 2013 App-V Package with the new Deployment Configuration File.</span></span>

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

6.  <span data-ttu-id="b233b-358">Повторно добавьте пакет Office 2013 App-V, а затем снова опубликуйте его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-358">Re-add the Office 2013 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2013 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="b233b-359">Отключение сочетаний клавиш в Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-359">Disabling Office 2013 shortcuts</span></span>

<span data-ttu-id="b233b-360">Вместо отмены публикации или удаления пакета вы можете отключить сочетания клавиш для некоторых приложений Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-360">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="b233b-361">В следующем примере показано, как отключить сочетания клавиш для Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b233b-361">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="b233b-362">Отключение сочетаний клавиш для приложений Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-362">To disable shortcuts for Office 2013 applications</span></span>**

1.  <span data-ttu-id="b233b-363">Откройте файл конфигурации развертывания в блокноте и выполните поиск по запросу "ярлыки".</span><span class="sxs-lookup"><span data-stu-id="b233b-363">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="b233b-364">Чтобы отключить определенные сочетания клавиш, удалите или закомментируйте конкретные сочетания клавиш, которые вам не нужны.</span><span class="sxs-lookup"><span data-stu-id="b233b-364">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="b233b-365">Подсистема должна быть доступна и включена.</span><span class="sxs-lookup"><span data-stu-id="b233b-365">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="b233b-366">Например, в приведенном ниже примере удалите сочетания клавиш Microsoft Access, сохранив при этом ярлыки/shortcut не &lt; &gt; &lt; &gt; смогут отключить ярлык Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b233b-366">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

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

3.  <span data-ttu-id="b233b-367">Сохраните файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="b233b-367">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="b233b-368">Повторно опубликуйте пакет Office 2013 App-V с новым файлом конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="b233b-368">Republish Office 2013 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="b233b-369">Многие дополнительные параметры можно изменить, изменив конфигурацию развертывания для пакетов App-V, например сопоставления типов файлов, виртуальной файловой системы и т. д.</span><span class="sxs-lookup"><span data-stu-id="b233b-369">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="b233b-370">Дополнительные сведения об использовании файлов конфигурации развертывания для изменения параметров пакета App-V можно найти в разделе Дополнительные ресурсы в конце документа.</span><span class="sxs-lookup"><span data-stu-id="b233b-370">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="b233b-371">Управление обновлениями пакетов Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-371">Managing Office 2013 package upgrades</span></span>

<span data-ttu-id="b233b-372">Чтобы обновить пакет Office 2013, используйте средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-372">To upgrade an Office 2013 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="b233b-373">Чтобы обновить ранее развернутый пакет Office 2013, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b233b-373">To upgrade a previously deployed Office 2013 package, perform the following steps.</span></span>

**<span data-ttu-id="b233b-374">Как обновить ранее развернутый пакет Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-374">How to upgrade a previously deployed Office 2013 package</span></span>**

1.  <span data-ttu-id="b233b-375">Создайте новый пакет Office 2013 с помощью средства развертывания Office, которое использует самую последнюю версию приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-375">Create a new Office 2013 package through the Office Deployment Tool that uses the most recent Office 2013 application software.</span></span> <span data-ttu-id="b233b-376">Последние биты Office 2013 всегда можно получить на этапе загрузки пакета App-V приложения Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-376">The most recent Office 2013 bits can always be obtained through the download stage of creating an Office 2013 App-V Package.</span></span> <span data-ttu-id="b233b-377">Недавно созданный пакет Office 2013 содержит самые последние обновления и новый идентификатор версии.</span><span class="sxs-lookup"><span data-stu-id="b233b-377">The newly created Office 2013 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="b233b-378">Все пакеты, созданные с помощью средства развертывания Office, имеют одинаковый журнал обращений.</span><span class="sxs-lookup"><span data-stu-id="b233b-378">All packages created using the Office Deployment Tool have the same lineage.</span></span>

    **<span data-ttu-id="b233b-379">Примечание.</span><span class="sxs-lookup"><span data-stu-id="b233b-379">Note</span></span>**  
    <span data-ttu-id="b233b-380">У пакетов Office App-V есть два идентификатора версии:</span><span class="sxs-lookup"><span data-stu-id="b233b-380">Office App-V packages have two Version IDs:</span></span>

    -   <span data-ttu-id="b233b-381">Идентификатор версии пакета App-V для Office 2013, уникальный для всех пакетов, созданных с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-381">An Office 2013 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span>

    -   <span data-ttu-id="b233b-382">Второй идентификатор версии пакета App-V, x. x. x. x, например, в манифесте AppX, который будет изменен только в том случае, если у вас есть новая версия Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-382">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="b233b-383">Например, если выпущена новая версия Office 2013 с обновлениями, а пакет создан с помощью средства развертывания Office для включения этих обновлений, номер версии X. X. x. X изменится, чтобы показать, что сама версия Office изменилась.</span><span class="sxs-lookup"><span data-stu-id="b233b-383">For example, if a new Office 2013 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="b233b-384">Сервер App-V использует номер версии X. X. X. X, чтобы отличать этот пакет и распознать, что он будет содержать новые обновления для ранее опубликованного пакета, и в результате его можно опубликовать как обновление для существующего пакета Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-384">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2013 package.</span></span>



2.  <span data-ttu-id="b233b-385">Глобально опубликуйте созданные пакеты Office 2013 App-V на компьютерах, на которых вы хотите применить новые обновления.</span><span class="sxs-lookup"><span data-stu-id="b233b-385">Globally publish the newly created Office 2013 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="b233b-386">Так как новый пакет имеет тот же журнал обращений к устаревшему пакету Office 2013 App-V, при публикации нового пакета с обновлениями будут применены только новые изменения старого пакета, поэтому они будут быстрее.</span><span class="sxs-lookup"><span data-stu-id="b233b-386">Since the new package has the same lineage of the older Office 2013 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3.  <span data-ttu-id="b233b-387">Обновления будут применены таким же образом для глобальных опубликованных пакетов App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-387">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="b233b-388">Так как приложения, скорее всего, будут использоваться, обновления могут быть отложены до тех пор, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b233b-388">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>

### <a href="" id="bkmk-manage-office-lic-upgrd"></a><span data-ttu-id="b233b-389">Управление обновлениями лицензирования Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-389">Managing Office 2013 licensing upgrades</span></span>

<span data-ttu-id="b233b-390">Если у нового пакета Office 2013 App-V есть лицензия, отличная от уже развернутого пакета App-V для Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-390">If a new Office 2013 App-V Package has a different license than the Office 2013 App-V Package currently deployed.</span></span> <span data-ttu-id="b233b-391">Например, развернутый пакет Office 2013 является подпиской на основе подписки на Office 2013, а новый пакет Office 2013 — на основе корпоративного лицензирования, поэтому для обеспечения беспрепятственного лицензирования необходимо следовать приведенным ниже инструкциям.</span><span class="sxs-lookup"><span data-stu-id="b233b-391">For instance, the Office 2013 package deployed is a subscription based Office 2013 and the new Office 2013 package is Volume Licensing based, the following instructions must be followed to ensure smooth licensing upgrade:</span></span>

**<span data-ttu-id="b233b-392">Как обновить лицензию на Office 2013</span><span class="sxs-lookup"><span data-stu-id="b233b-392">How to upgrade an Office 2013 License</span></span>**

1.  <span data-ttu-id="b233b-393">Отменить публикацию уже развернутого пакета приложения лицензированных подписок на Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-393">Unpublish the already deployed Office 2013 Subscription Licensing App-V package.</span></span>

2.  <span data-ttu-id="b233b-394">Удалите неопубликованный пакет приложения для лицензирования подписки на Office 2013.</span><span class="sxs-lookup"><span data-stu-id="b233b-394">Remove the unpublished Office 2013 Subscription Licensing App-V package.</span></span>

3.  <span data-ttu-id="b233b-395">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="b233b-395">Restart the computer.</span></span>

4.  <span data-ttu-id="b233b-396">Добавьте новый пакет корпоративного лицензирования Office 2013 App-V.</span><span class="sxs-lookup"><span data-stu-id="b233b-396">Add the new Office 2013 App-V Package Volume Licensing.</span></span>

5.  <span data-ttu-id="b233b-397">Опубликуйте добавленный пакет App-V Office 2013 с помощью программы корпоративного лицензирования.</span><span class="sxs-lookup"><span data-stu-id="b233b-397">Publish the added Office 2013 App-V Package with Volume Licensing.</span></span>

<span data-ttu-id="b233b-398">Пакет Office 2013 App-V с выбранным лицензированием будет успешно развернут.</span><span class="sxs-lookup"><span data-stu-id="b233b-398">An Office 2013 App-V Package with your chosen licensing will be successfully deployed.</span></span>

### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="b233b-399">Развертывание Visio 2013 и Project 2013 с Office</span><span class="sxs-lookup"><span data-stu-id="b233b-399">Deploying Visio 2013 and Project 2013 with Office</span></span>

<span data-ttu-id="b233b-400">В таблице ниже описаны требования и параметры для развертывания Visio 2013 и Project 2013 с Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-400">The following table describes the requirements and options for deploying Visio 2013 and Project 2013 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-401">Задача</span><span class="sxs-lookup"><span data-stu-id="b233b-401">Task</span></span></th>
<th align="left"><span data-ttu-id="b233b-402">Сведения</span><span class="sxs-lookup"><span data-stu-id="b233b-402">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-403">Как упаковать и опубликовать Visio 2013 и Project 2013 с Office?</span><span class="sxs-lookup"><span data-stu-id="b233b-403">How do I package and publish Visio 2013 and Project 2013 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-404">Вы должны включить Visio 2013 и Project 2013 в один и тот же пакет для Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-404">You must include Visio 2013 and Project 2013 in the same package with Office.</span></span></p>
<p><span data-ttu-id="b233b-405">Если вы не развертываете Office, вы можете создать пакет, содержащий Visio и/или Project, при условии, что вы подпишитесь на <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> развертывание Microsoft Office 2010 с помощью App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="b233b-405">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)">Deploying Microsoft Office 2010 by Using App-V</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b233b-406">Как развернуть Visio 2013 и Project 2013 для определенных пользователей?</span><span class="sxs-lookup"><span data-stu-id="b233b-406">How can I deploy Visio 2013 and Project 2013 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-407">Воспользуйтесь одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="b233b-407">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b233b-408">Если вы хотите...</span><span class="sxs-lookup"><span data-stu-id="b233b-408">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="b233b-409">... затем используйте этот метод</span><span class="sxs-lookup"><span data-stu-id="b233b-409">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b233b-410">Создание двух разных пакетов и развертывание каждого из них в другой группе пользователей</span><span class="sxs-lookup"><span data-stu-id="b233b-410">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-411">Создание и развертывание следующих пакетов:</span><span class="sxs-lookup"><span data-stu-id="b233b-411">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="b233b-412">Пакет, содержащий только Office — развертывание на компьютерах, пользователям которых требуется только Office.</span><span class="sxs-lookup"><span data-stu-id="b233b-412">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="b233b-413">Пакет, содержащий Office, Visio и Project-deploy, на компьютеры, для пользователей которых нужны все три приложения.</span><span class="sxs-lookup"><span data-stu-id="b233b-413">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b233b-414">Если вам нужен только один пакет для всей организации или если у вас есть пользователи, которым предоставлен доступ к компьютерам:</span><span class="sxs-lookup"><span data-stu-id="b233b-414">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="b233b-415">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="b233b-415">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="b233b-416">Создание пакета, содержащего Office, Visio и Project.</span><span class="sxs-lookup"><span data-stu-id="b233b-416">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="b233b-417">Развертывание пакета для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="b233b-417">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="b233b-418">Используйте <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , чтобы запретить определенным пользователям использовать Visio и Project.</span><span class="sxs-lookup"><span data-stu-id="b233b-418">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="b233b-419">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b233b-419">Additional resources</span></span>


**<span data-ttu-id="b233b-420">Дополнительные ресурсы в пакетах Office 2013 App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-420">Office 2013 App-V Packages Additional Resources</span></span>**

[<span data-ttu-id="b233b-421">Средство развертывания Office для "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="b233b-421">Office Deployment Tool for Click-to-Run</span></span>](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[<span data-ttu-id="b233b-422">Поддерживаемые сценарии для развертывания Microsoft Office в последовательном пакете App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-422">Supported scenarios for deploying Microsoft Office as a sequenced App-V Package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**<span data-ttu-id="b233b-423">Пакеты приложения Office 2010 App-V</span><span class="sxs-lookup"><span data-stu-id="b233b-423">Office 2010 App-V Packages</span></span>**

[<span data-ttu-id="b233b-424">Комплект виртуализации Microsoft Office 2010 для Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b233b-424">Microsoft Office 2010 Sequencing Kit for Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[<span data-ttu-id="b233b-425">Известные проблемы, возникающие при создании или использовании пакета Office 2010 для App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b233b-425">Known issues when you create or use an App-V 5.0 Office 2010 package</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[<span data-ttu-id="b233b-426">Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b233b-426">How to sequence Microsoft Office 2010 in Microsoft Application Virtualization 5.0</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**<span data-ttu-id="b233b-427">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="b233b-427">Connection Groups</span></span>**

[<span data-ttu-id="b233b-428">Развертывание групп подключений в Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="b233b-428">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="b233b-429">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="b233b-429">Managing Connection Groups</span></span>](managing-connection-groups51.md)

**<span data-ttu-id="b233b-430">Динамическая настройка</span><span class="sxs-lookup"><span data-stu-id="b233b-430">Dynamic Configuration</span></span>**

[<span data-ttu-id="b233b-431">Сведения о динамической конфигурации App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="b233b-431">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)














