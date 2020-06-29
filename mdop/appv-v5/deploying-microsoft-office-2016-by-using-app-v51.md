---
title: Развертывание Microsoft Office 2016 с помощью App-V
description: Развертывание Microsoft Office 2016 с помощью App-V
author: dansimp
ms.assetid: e0f4876-da99-4b89-977e-2fb6e89ea3d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: b47fd46c8dc368bbce819b24f18fa30328fbbaf0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814608"
---
# <span data-ttu-id="e53b4-103">Развертывание Microsoft Office 2016 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-103">Deploying Microsoft Office 2016 by Using App-V</span></span>


<span data-ttu-id="e53b4-104">В этой статье описано, как использовать Microsoft Application Virtualization (App-V) 5,1 или более поздних версий для поставки Microsoft Office 2016 как виртуализированного приложения на компьютерах организации.</span><span class="sxs-lookup"><span data-stu-id="e53b4-104">Use the information in this article to use Microsoft Application Virtualization (App-V) 5.1, or later versions, to deliver Microsoft Office 2016 as a virtualized application to computers in your organization.</span></span> <span data-ttu-id="e53b4-105">Сведения о том, как использовать App-V для отправки Office 2013, можно найти в разделе [развертывание Microsoft office 2013 с помощью App-V](deploying-microsoft-office-2013-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="e53b4-105">For information about using App-V to deliver Office 2013, see [Deploying Microsoft Office 2013 by Using App-V](deploying-microsoft-office-2013-by-using-app-v51.md).</span></span> <span data-ttu-id="e53b4-106">Сведения о том, как использовать App-V для отправки Office 2010, можно найти в разделе [развертывание Microsoft office 2010 с помощью App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="e53b4-106">For information about using App-V to deliver Office 2010, see [Deploying Microsoft Office 2010 by Using App-V](deploying-microsoft-office-2010-by-using-app-v51.md).</span></span>

<span data-ttu-id="e53b4-107">Этот раздел включает в себя следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="e53b4-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e53b4-108">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="e53b4-108">What to know before you start</span></span>](#bkmk-before-you-start)

-   [<span data-ttu-id="e53b4-109">Создание пакета Office 2016 для App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-109">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>](#bkmk-create-office-pkg)

-   [<span data-ttu-id="e53b4-110">Публикация пакета Office для App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="e53b4-110">Publishing the Office package for App-V 5.1</span></span>](#bkmk-pub-pkg-office)

-   [<span data-ttu-id="e53b4-111">Настройка пакетов приложений Office App-V и управление ими</span><span class="sxs-lookup"><span data-stu-id="e53b4-111">Customizing and managing Office App-V packages</span></span>](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a><span data-ttu-id="e53b4-112">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="e53b4-112">What to know before you start</span></span>


<span data-ttu-id="e53b4-113">Перед развертыванием Office 2016 с помощью App-V ознакомьтесь со следующими сведениями о планировании.</span><span class="sxs-lookup"><span data-stu-id="e53b4-113">Before you deploy Office 2016 by using App-V, review the following planning information.</span></span>

### <a href="" id="bkmk-supp-vers-coexist"></a><span data-ttu-id="e53b4-114">Поддерживаемые версии Office и сосуществование Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-114">Supported Office versions and Office coexistence</span></span>

<span data-ttu-id="e53b4-115">В следующей таблице приведены сведения о поддерживаемых версиях Office и о том, как работать с имеющимися версиями Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-115">Use the following table to get information about supported versions of Office and about running coexisting versions of Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-116">Сведения для проверки</span><span class="sxs-lookup"><span data-stu-id="e53b4-116">Information to review</span></span></th>
<th align="left"><span data-ttu-id="e53b4-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e53b4-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)"><span data-ttu-id="e53b4-118">Поддерживаемые версии Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-118">Supported versions of Microsoft Office</span></span></a></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e53b4-119">Поддерживаемые версии Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-119">Supported versions of Office</span></span></p></li>
<li><p><span data-ttu-id="e53b4-120">Поддерживаемые типы развертывания (например, классическое приложение, инфраструктура личных виртуальных рабочих столов (VDI), в составе пула VDI)</span><span class="sxs-lookup"><span data-stu-id="e53b4-120">Supported deployment types (for example, desktop, personal Virtual Desktop Infrastructure (VDI), pooled VDI)</span></span></p></li>
<li><p><span data-ttu-id="e53b4-121">Варианты лицензирования Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-121">Office licensing options</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)"><span data-ttu-id="e53b4-122">Планирование использования App-V с помощью косуществующих версий Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-122">Planning for Using App-V with coexisting versions of Office</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="e53b4-123">Рекомендации по установке разных версий Office на одном компьютере</span><span class="sxs-lookup"><span data-stu-id="e53b4-123">Considerations for installing different versions of Office on the same computer</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a><span data-ttu-id="e53b4-124">Требования к пакетированию, публикации и развертыванию</span><span class="sxs-lookup"><span data-stu-id="e53b4-124">Packaging, publishing, and deployment requirements</span></span>

<span data-ttu-id="e53b4-125">Перед развертыванием Office с помощью App-V ознакомьтесь с приведенными ниже требованиями.</span><span class="sxs-lookup"><span data-stu-id="e53b4-125">Before you deploy Office by using App-V, review the following requirements.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-126">Задача</span><span class="sxs-lookup"><span data-stu-id="e53b4-126">Task</span></span></th>
<th align="left"><span data-ttu-id="e53b4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e53b4-127">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-128">Создание пакетов</span><span class="sxs-lookup"><span data-stu-id="e53b4-128">Packaging</span></span></p></td>
<td align="left">
<ul>
<li><p><span data-ttu-id="e53b4-129">Все приложения Office, которые вы хотите развернуть для пользователей, должны находиться в одном пакете.</span><span class="sxs-lookup"><span data-stu-id="e53b4-129">All of the Office applications that you want to deploy to users must be in a single package.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-130">В App-V 5,1 и более поздних версиях для создания пакетов необходимо использовать средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-130">In App-V 5.1 and later, you must use the Office Deployment Tool to create packages.</span></span> <span data-ttu-id="e53b4-131">Нельзя использовать секвенсор.</span><span class="sxs-lookup"><span data-stu-id="e53b4-131">You cannot use the Sequencer.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-132">Если вы развертываете Microsoft Visio 2016 и Microsoft Project 2016 вместе с Office, необходимо включить их в один пакет с Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-132">If you are deploying Microsoft Visio 2016 and Microsoft Project 2016 along with Office, you must include them in the same package with Office.</span></span> <span data-ttu-id="e53b4-133">Дополнительные сведения можно найти в разделе <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> развертывание Visio 2016 и Project 2016 с Office </a> .</span><span class="sxs-lookup"><span data-stu-id="e53b4-133">For more information, see <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)">Deploying Visio 2016 and Project 2016 with Office</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e53b4-134">Публикация</span><span class="sxs-lookup"><span data-stu-id="e53b4-134">Publishing</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e53b4-135">Вы можете опубликовать только один пакет Office на каждом клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="e53b4-135">You can publish only one Office package to each client computer.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-136">Необходимо опубликовать пакет Office глобально.</span><span class="sxs-lookup"><span data-stu-id="e53b4-136">You must publish the Office package globally.</span></span> <span data-ttu-id="e53b4-137">Вы не можете опубликовать пользователя.</span><span class="sxs-lookup"><span data-stu-id="e53b4-137">You cannot publish to the user.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-138">Развертывание любого из перечисленных ниже продуктов на общем компьютере, например с помощью служб удаленных рабочих столов:</span><span class="sxs-lookup"><span data-stu-id="e53b4-138">Deploying any of the following products to a shared computer, for example, by using Remote Desktop Services:</span></span></p>
<ul>
<li><p><span data-ttu-id="e53b4-139">Приложения Microsoft 365 для предприятий</span><span class="sxs-lookup"><span data-stu-id="e53b4-139">Microsoft 365 Apps for enterprise</span></span></p></li>
<li><p><span data-ttu-id="e53b4-140">Visio Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="e53b4-140">Visio Pro for Office 365</span></span></p></li>
<li><p><span data-ttu-id="e53b4-141">Project Pro для Office 365</span><span class="sxs-lookup"><span data-stu-id="e53b4-141">Project Pro for Office 365</span></span></p></li>
</ul></td>
<td align="left"><p><span data-ttu-id="e53b4-142">Необходимо включить <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> активацию на общем компьютере </a> .</span><span class="sxs-lookup"><span data-stu-id="e53b4-142">You must enable <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)">shared computer activation</a>.</span></span></p>
</td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e53b4-143">Исключение приложений Office из пакета</span><span class="sxs-lookup"><span data-stu-id="e53b4-143">Excluding Office applications from a package</span></span>

<span data-ttu-id="e53b4-144">В приведенной ниже таблице описаны рекомендуемые методы для исключения конкретных приложений Office из пакета.</span><span class="sxs-lookup"><span data-stu-id="e53b4-144">The following table describes the recommended methods for excluding specific Office applications from a package.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-145">Задача</span><span class="sxs-lookup"><span data-stu-id="e53b4-145">Task</span></span></th>
<th align="left"><span data-ttu-id="e53b4-146">Сведения</span><span class="sxs-lookup"><span data-stu-id="e53b4-146">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-147">Используйте <strong> параметр ExcludeApp </strong> при создании пакета с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-147">Use the <strong>ExcludeApp</strong> setting when you create the package by using the Office Deployment Tool.</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e53b4-148">Позволяет исключить из пакета определенные приложения Office, когда средство развертывания Office создаст пакет.</span><span class="sxs-lookup"><span data-stu-id="e53b4-148">Enables you to exclude specific Office applications from the package when the Office Deployment Tool creates the package.</span></span> <span data-ttu-id="e53b4-149">Например, вы можете использовать этот параметр, чтобы создать пакет, содержащий только Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="e53b4-149">For example, you can use this setting to create a package that contains only Microsoft Word.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-150">Дополнительные сведения можно найти в разделе <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp element </a> .</span><span class="sxs-lookup"><span data-stu-id="e53b4-150">For more information, see <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)">ExcludeApp element</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e53b4-151">Изменение файла DeploymentConfig.xml</span><span class="sxs-lookup"><span data-stu-id="e53b4-151">Modify the DeploymentConfig.xml file</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e53b4-152">Измените файл DeploymentConfig.xml после создания пакета.</span><span class="sxs-lookup"><span data-stu-id="e53b4-152">Modify the DeploymentConfig.xml file after the package has been created.</span></span> <span data-ttu-id="e53b4-153">Этот файл содержит параметры пакета по умолчанию для всех пользователей на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-153">This file contains the default package settings for all users on a computer that is running the App-V Client.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-154">Дополнительные сведения можно найти в разделе <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> Отключение приложений Office 2016 </a> .</span><span class="sxs-lookup"><span data-stu-id="e53b4-154">For more information, see <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)">Disabling Office 2016 applications</a>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a><span data-ttu-id="e53b4-155">Создание пакета Office 2016 для App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-155">Creating an Office 2016 package for App-V with the Office Deployment Tool</span></span>


<span data-ttu-id="e53b4-156">Выполните описанные ниже действия, чтобы создать пакет Office 2016 для App-V 5,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e53b4-156">Complete the following steps to create an Office 2016 package for App-V 5.1 or later.</span></span>

><span data-ttu-id="e53b4-157">**Важно!** &nbsp; &nbsp; В App-V 5,1 и более поздних версиях для создания пакета необходимо использовать средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-157">**Important**&nbsp;&nbsp;In App-V 5.1 and later, you must use the Office Deployment Tool to create a package.</span></span> <span data-ttu-id="e53b4-158">Нельзя использовать секвенсор для создания пакетов.</span><span class="sxs-lookup"><span data-stu-id="e53b4-158">You cannot use the Sequencer to create packages.</span></span>

### <span data-ttu-id="e53b4-159">Проверка готовности к использованию средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-159">Review prerequisites for using the Office Deployment Tool</span></span>

<span data-ttu-id="e53b4-160">На компьютере, на котором устанавливается средство развертывания Office, должны быть:</span><span class="sxs-lookup"><span data-stu-id="e53b4-160">The computer on which you are installing the Office Deployment Tool must have:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-161">Предварительные</span><span class="sxs-lookup"><span data-stu-id="e53b4-161">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="e53b4-162">Описание</span><span class="sxs-lookup"><span data-stu-id="e53b4-162">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-163">Необходимое программное обеспечение</span><span class="sxs-lookup"><span data-stu-id="e53b4-163">Prerequisite software</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-164">.NET Framework 4</span><span class="sxs-lookup"><span data-stu-id="e53b4-164">.Net Framework 4</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e53b4-165">Поддерживаемые операционные системы</span><span class="sxs-lookup"><span data-stu-id="e53b4-165">Supported operating systems</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="e53b4-166">64-разрядная версия Windows 10</span><span class="sxs-lookup"><span data-stu-id="e53b4-166">64-bit version of Windows 10</span></span></p></li>
<li><p><span data-ttu-id="e53b4-167">64-разрядная версия Windows 8 или 8,1</span><span class="sxs-lookup"><span data-stu-id="e53b4-167">64-bit version of Windows 8 or 8.1</span></span></p></li>
<li><p><span data-ttu-id="e53b4-168">64-разрядная версия Windows 7</span><span class="sxs-lookup"><span data-stu-id="e53b4-168">64-bit version of Windows 7</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


><span data-ttu-id="e53b4-169">**Примечание**  В этой статье термин "пакет приложения Office 2016 App-V" относится к лицензии на подписку.</span><span class="sxs-lookup"><span data-stu-id="e53b4-169">**Note**  In this topic, the term “Office 2016 App-V package” refers to subscription licensing.</span></span>


### <span data-ttu-id="e53b4-170">Создание пакетов Office 2016 App-V с помощью средства развертывания Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-170">Create Office 2016 App-V Packages Using Office Deployment Tool</span></span>

<span data-ttu-id="e53b4-171">Пакеты App-V для Office 2016 создаются с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-171">You create Office 2016 App-V packages by using the Office Deployment Tool.</span></span> <span data-ttu-id="e53b4-172">Ниже приведены инструкции по созданию пакета App-V для Office 2016 с лицензией на подписку.</span><span class="sxs-lookup"><span data-stu-id="e53b4-172">The following instructions explain how to create an Office 2016 App-V package with Subscription Licensing.</span></span>

<span data-ttu-id="e53b4-173">Создавайте пакеты App-V для Office 2016 на компьютерах с 64-разрядной версией Windows.</span><span class="sxs-lookup"><span data-stu-id="e53b4-173">Create Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="e53b4-174">После создания пакет Office 2016 App-V будет работать на компьютерах с Windows 7, Windows 8,1 и Windows 10, поддерживающих 32-разрядную и 64-разр.</span><span class="sxs-lookup"><span data-stu-id="e53b4-174">Once created, the Office 2016 App-V package will run on 32-bit and 64-bit Windows 7, Windows 8.1, and Windows 10 computers.</span></span>

### <span data-ttu-id="e53b4-175">Скачать средство развертывания Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-175">Download the Office Deployment Tool</span></span>

<span data-ttu-id="e53b4-176">Пакеты App-V для Office 2016 создаются с помощью средства развертывания Office, которое создает пакет App-V для Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-176">Office 2016 App-V Packages are created using the Office Deployment Tool, which generates an Office 2016 App-V Package.</span></span> <span data-ttu-id="e53b4-177">Пакет нельзя создать или изменить с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-177">The package cannot be created or modified through the App-V sequencer.</span></span> <span data-ttu-id="e53b4-178">Чтобы начать создание пакета, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e53b4-178">To begin package creation:</span></span>

1.  <span data-ttu-id="e53b4-179">Скачайте [средство развертывания Office 2016 для программы "нажми и работай](https://www.microsoft.com/download/details.aspx?id=49117)".</span><span class="sxs-lookup"><span data-stu-id="e53b4-179">Download the [Office 2016 Deployment Tool for Click-to-Run](https://www.microsoft.com/download/details.aspx?id=49117).</span></span>

> <span data-ttu-id="e53b4-180">**Важно!** Для создания пакетов App-V для Office 2016 необходимо использовать средство развертывания Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-180">**Important** You must use the Office 2016 Deployment Tool to create Office 2016 App-V Packages.</span></span>
> 2. <span data-ttu-id="e53b4-181">Запустите exe исполняемый файл и извлеките его компоненты в нужное место.</span><span class="sxs-lookup"><span data-stu-id="e53b4-181">Run the .exe file and extract its features into the desired location.</span></span> <span data-ttu-id="e53b4-182">Чтобы упростить этот процесс, вы можете создать общую сетевую папку, в которой будут сохраняться функции.</span><span class="sxs-lookup"><span data-stu-id="e53b4-182">To make this process easier, you can create a shared network folder where the features will be saved.</span></span>

    Example: \\\\Server\\Office2016

3. <span data-ttu-id="e53b4-183">Убедитесь в том, что в указанном расположении есть setup.exe и configuration.xml файл.</span><span class="sxs-lookup"><span data-stu-id="e53b4-183">Check that a setup.exe and a configuration.xml file exist and are in the location you specified.</span></span>

### <span data-ttu-id="e53b4-184">Загрузка приложений Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-184">Download Office 2016 applications</span></span>

<span data-ttu-id="e53b4-185">После того как вы загрузили средство развертывания Office, вы можете использовать его для получения последних приложений Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-185">After you download the Office Deployment Tool, you can use it to get the latest Office 2016 applications.</span></span> <span data-ttu-id="e53b4-186">После того как вы получите приложения Office, вы создадите пакет Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-186">After getting the Office applications, you create the Office 2016 App-V package.</span></span>

<span data-ttu-id="e53b4-187">XML-файл, который входит в состав средства развертывания Office, определяет сведения о продукте, например языки и приложения Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-187">The XML file that is included in the Office Deployment Tool specifies the product details, such as the languages and Office applications included.</span></span>

1. <span data-ttu-id="e53b4-188">**Настройте образец XML-файла конфигурации.** Чтобы настроить приложения Office, используйте образец XML-файла конфигурации, который вы загрузили с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-188">**Customize the sample XML configuration file:** Use the sample XML configuration file that you downloaded with the Office Deployment Tool to customize the Office applications:</span></span>

   1. <span data-ttu-id="e53b4-189">Откройте образец XML-файла в блокноте или в любом любимом текстовом редакторе.</span><span class="sxs-lookup"><span data-stu-id="e53b4-189">Open the sample XML file in Notepad or your favorite text editor.</span></span>

   2. <span data-ttu-id="e53b4-190">После открытия файла примера configuration.xml и его подготовки к редактированию вы можете указать продукты, языки и путь, по которому нужно сохранить приложения Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-190">With the sample configuration.xml file open and ready for editing, you can specify products, languages, and the path to which you save the Office 2016 applications.</span></span> <span data-ttu-id="e53b4-191">Ниже приведен простой пример файла configuration.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-191">The following is a basic example of the configuration.xml file:</span></span>

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      ><span data-ttu-id="e53b4-192">**Примечание**  XML-файл конфигурации — это пример XML-файла.</span><span class="sxs-lookup"><span data-stu-id="e53b4-192">**Note**  The configuration XML is a sample XML file.</span></span> <span data-ttu-id="e53b4-193">Файл содержит строки, которые снабжены комментариями. Вы можете "снять комментарий", чтобы настроить дополнительные параметры файла.</span><span class="sxs-lookup"><span data-stu-id="e53b4-193">The file includes lines that are commented out. You can “uncomment” these lines to customize additional settings with the file.</span></span> <span data-ttu-id="e53b4-194">Чтобы "снять комментарий", удалите строку "<!</span><span class="sxs-lookup"><span data-stu-id="e53b4-194">To “uncomment” these lines, remove the "<!</span></span> <span data-ttu-id="e53b4-195">--"от начала строки и"--> ", начиная с конца строки.</span><span class="sxs-lookup"><span data-stu-id="e53b4-195">- -" from the beginning of the line, and the "-- >" from the end of the line.</span></span>

      <span data-ttu-id="e53b4-196">Вышеприведенный XML-файл конфигурации указывает на то, что версия Office 2016 ProPlus 32-bit Edition, включая Visio профессиональный плюс, будет загружена на английском языке в \\\\server\\Office 2016 (это расположение, в которое будут сохранены приложения Office).</span><span class="sxs-lookup"><span data-stu-id="e53b4-196">The above XML configuration file specifies that Office 2016 ProPlus 32-bit edition, including Visio ProPlus, will be downloaded in English to the \\\\server\\Office 2016, which is the location where Office applications will be saved to.</span></span> <span data-ttu-id="e53b4-197">Обратите внимание, что код продукта приложения не влияет на финальное лицензирование Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-197">Note that the Product ID of the applications will not affect the final licensing of Office.</span></span> <span data-ttu-id="e53b4-198">Пакеты App-V для Office 2016 с различными лицензированиями можно создавать из одних и тех же приложений, выдавая лицензирование на более поздней стадии.</span><span class="sxs-lookup"><span data-stu-id="e53b4-198">Office 2016 App-V packages with various licensing can be created from the same applications through specifying licensing in a later stage.</span></span> <span data-ttu-id="e53b4-199">В таблице ниже перечислены настраиваемые атрибуты и элементы XML-файла.</span><span class="sxs-lookup"><span data-stu-id="e53b4-199">The table below summarizes the customizable attributes and elements of XML file:</span></span>

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left"><span data-ttu-id="e53b4-200">Ввод</span><span class="sxs-lookup"><span data-stu-id="e53b4-200">Input</span></span></th>
      <th align="left"><span data-ttu-id="e53b4-201">Описание</span><span class="sxs-lookup"><span data-stu-id="e53b4-201">Description</span></span></th>
      <th align="left"><span data-ttu-id="e53b4-202">Пример.</span><span class="sxs-lookup"><span data-stu-id="e53b4-202">Example</span></span></th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="e53b4-203">Добавить элемент</span><span class="sxs-lookup"><span data-stu-id="e53b4-203">Add element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-204">Указывает продукты и языки, которые нужно включить в пакет.</span><span class="sxs-lookup"><span data-stu-id="e53b4-204">Specifies the products and languages to include in the package.</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-205">Н/Д</span><span class="sxs-lookup"><span data-stu-id="e53b4-205">N/A</span></span></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="e53b4-206">OfficeClientEdition (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="e53b4-206">OfficeClientEdition (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-207">Указывает выпуск Office 2016, который будет использоваться: с 32 или 64-bit.</span><span class="sxs-lookup"><span data-stu-id="e53b4-207">Specifies the edition of Office 2016 product to use: 32-bit or 64-bit.</span></span> <span data-ttu-id="e53b4-208">Операция завершается сбоем, если <strong> </strong> для OfficeClientEdition не задано допустимое значение.</span><span class="sxs-lookup"><span data-stu-id="e53b4-208">The operation fails if <strong>OfficeClientEdition</strong> is not set to a valid value.</span></span></p></td>
      <td align="left"><p><strong><span data-ttu-id="e53b4-209">OfficeClientEdition </strong> = &quot; 32&quot;</span><span class="sxs-lookup"><span data-stu-id="e53b4-209">OfficeClientEdition</strong>=&quot;32&quot;</span></span></p>
      <p><strong><span data-ttu-id="e53b4-210">OfficeClientEdition </strong> = &quot; 64&quot;</span><span class="sxs-lookup"><span data-stu-id="e53b4-210">OfficeClientEdition</strong>=&quot;64&quot;</span></span></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="e53b4-211">Элемент Product</span><span class="sxs-lookup"><span data-stu-id="e53b4-211">Product element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-212">Указывает приложение.</span><span class="sxs-lookup"><span data-stu-id="e53b4-212">Specifies the application.</span></span> <span data-ttu-id="e53b4-213">Проект 2016 и Visio 2016 должны быть указаны в качестве добавленного продукта для включения в приложения.</span><span class="sxs-lookup"><span data-stu-id="e53b4-213">Project 2016 and Visio 2016 must be specified here as an added product to be included in the applications.</span></span>

      <span data-ttu-id="e53b4-214">Дополнительные сведения о кодах продуктов можно найти в статьях <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> коды продуктов, которые поддерживаются средством развертывания Office для "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="e53b4-214">For more information about the product IDs, see <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)">Product IDs that are supported by the Office Deployment Tool for Click-to-Run</span></span></a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="e53b4-215">Элемент Language</span><span class="sxs-lookup"><span data-stu-id="e53b4-215">Language element</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-216">Указывает язык, поддерживаемый в приложениях.</span><span class="sxs-lookup"><span data-stu-id="e53b4-216">Specifies the language supported in the applications</span></span></p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p><span data-ttu-id="e53b4-217">Версия (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="e53b4-217">Version (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-218">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="e53b4-218">Optional.</span></span> <span data-ttu-id="e53b4-219">Задает сборку, используемую для пакета.</span><span class="sxs-lookup"><span data-stu-id="e53b4-219">Specifies a build to use for the package</span></span></p>
      <p><span data-ttu-id="e53b4-220">По умолчанию — это новейшая объявленная сборка (определенная в v32.CAB на источнике Office).</span><span class="sxs-lookup"><span data-stu-id="e53b4-220">Defaults to latest advertised build (as defined in v32.CAB at the Office source).</span></span></p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="e53b4-221">Источник (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="e53b4-221">SourcePath (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-222">Указывает расположение, в которое будут сохраняться приложения.</span><span class="sxs-lookup"><span data-stu-id="e53b4-222">Specifies the location in which the applications will be saved to.</span></span></p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p><span data-ttu-id="e53b4-223">Branch (атрибут элемента Add)</span><span class="sxs-lookup"><span data-stu-id="e53b4-223">Branch (attribute of Add element)</span></span></p></td>
      <td align="left"><p><span data-ttu-id="e53b4-224">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="e53b4-224">Optional.</span></span> <span data-ttu-id="e53b4-225">Указывает ветвь обновления для продукта, который вы хотите скачать или установить.</span><span class="sxs-lookup"><span data-stu-id="e53b4-225">Specifies the update branch for the product that you want to download or install.</span></span> </p><p><span data-ttu-id="e53b4-226">Дополнительные сведения об обновлениях ветвей можно найти в статье Обзор ветвей обновлений для приложений Microsoft 365 для предприятий.</span><span class="sxs-lookup"><span data-stu-id="e53b4-226">For more information about update branches, see Overview of update branches for Microsoft 365 Apps for enterprise.</span></span></p></td>
      <td align="left"><p><code>Branch = &quot;Business&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      <span data-ttu-id="e53b4-227">После редактирования файла configuration.xml, чтобы указать необходимый продукт, язык и расположение, в котором будут сохраняться приложения Office 2016, вы можете сохранить файл конфигурации, например Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-227">After editing the configuration.xml file to specify the desired product, languages, and also the location which the Office 2016 applications will be saved onto, you can save the configuration file, for example, as Customconfig.xml.</span></span>

2. <span data-ttu-id="e53b4-228">**Скачайте приложения в указанное расположение:** Используйте командную команду с повышенными привилегиями и 64-разрядную операционную систему, чтобы скачать приложения Office 2016, которые позже будут преобразованы в пакет App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-228">**Download the applications into the specified location:** Use an elevated command prompt and a 64 bit operating system to download the Office 2016 applications that will later be converted into an App-V package.</span></span> <span data-ttu-id="e53b4-229">Ниже приведен пример команды с описанием подробных сведений.</span><span class="sxs-lookup"><span data-stu-id="e53b4-229">Below is an example command with a description of details:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   <span data-ttu-id="e53b4-230">В примере:</span><span class="sxs-lookup"><span data-stu-id="e53b4-230">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-231">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-231">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-232">— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-232">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e53b4-233">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="e53b4-233">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-234">— Это средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-234">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-235">/Download</span><span class="sxs-lookup"><span data-stu-id="e53b4-235">/download</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-236">загружает приложения Office 2016, указанные в customConfig.xml файле.</span><span class="sxs-lookup"><span data-stu-id="e53b4-236">downloads the Office 2016 applications that you specify in the customConfig.xml file.</span></span> <span data-ttu-id="e53b4-237">Эти биты можно позже преобразовать в пакет App-V для Office 2016 с корпоративным лицензированием.</span><span class="sxs-lookup"><span data-stu-id="e53b4-237">These bits can be later converted in an Office 2016 App-V package with Volume Licensing.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e53b4-238">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="e53b4-238">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-239">передает XML-файл конфигурации, необходимый для завершения процесса загрузки, в этом примере customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-239">passes the XML configuration file required to complete the download process, in this example, customconfig.xml.</span></span> <span data-ttu-id="e53b4-240">После использования команды скачать приложения Office нужно найти в расположении, указанном в XML-файле конфигурации, в этом примере \Server\Office2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-240">After using the download command, Office applications should be found in the location specified in the configuration xml file, in this example \Server\Office2016.</span></span></p></td>
   </tr>
   </tbody>
   </table>



### <span data-ttu-id="e53b4-241">Преобразование приложений Office в пакет App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-241">Convert the Office applications into an App-V package</span></span>

<span data-ttu-id="e53b4-242">После загрузки приложений Office 2016 с помощью средства развертывания Office с помощью средства развертывания Office можно преобразовать их в пакет приложения Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-242">After you download the Office 2016 applications through the Office Deployment Tool, use the Office Deployment Tool to convert them into an Office 2016 App-V package.</span></span> <span data-ttu-id="e53b4-243">Выполните действия, соответствующие вашей модели лицензирования.</span><span class="sxs-lookup"><span data-stu-id="e53b4-243">Complete the steps that correspond to your licensing model.</span></span>

**<span data-ttu-id="e53b4-244">Общие сведения о том, что вам нужно сделать:</span><span class="sxs-lookup"><span data-stu-id="e53b4-244">Summary of what you’ll need to do:</span></span>**

-   <span data-ttu-id="e53b4-245">Создавайте пакеты App-V для Office 2016 на компьютерах с 64-разрядной версией Windows.</span><span class="sxs-lookup"><span data-stu-id="e53b4-245">Create the Office 2016 App-V packages on 64-bit Windows computers.</span></span> <span data-ttu-id="e53b4-246">Тем не менее, пакет будет работать на компьютерах с Windows 7, Windows 8, 8,1 и Windows 10, а также в 32-и 64-разрядных версиях.</span><span class="sxs-lookup"><span data-stu-id="e53b4-246">However, the package will run on 32-bit and 64-bit Windows 7, Windows 8 or 8.1, and Windows 10 computers.</span></span>

-   <span data-ttu-id="e53b4-247">Создайте пакет Office App-V для подписки с помощью средства развертывания Office, а затем измените файл конфигурации CustomConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-247">Create an Office App-V package for Subscription Licensing package by using the Office Deployment Tool, and then modify the CustomConfig.xml configuration file.</span></span>

    <span data-ttu-id="e53b4-248">В следующей таблице приведены значения, которые необходимо ввести в файл CustomConfig.xml для модели лицензирования, которую вы используете.</span><span class="sxs-lookup"><span data-stu-id="e53b4-248">The following table summarizes the values you need to enter in the CustomConfig.xml file for the licensing model you’re using.</span></span> <span data-ttu-id="e53b4-249">В разделах, которые следуют за таблицей, указаны точные записи, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="e53b4-249">The steps in the sections that follow the table will specify the exact entries you need to make.</span></span>

><span data-ttu-id="e53b4-250">**Note** &nbsp; Примечание &nbsp; Вы можете использовать средство развертывания Office для создания пакетов App-V для приложений Microsoft 365 для предприятий.</span><span class="sxs-lookup"><span data-stu-id="e53b4-250">**Note**&nbsp;&nbsp;You can use the Office Deployment Tool to create App-V packages for Microsoft 365 Apps for enterprise.</span></span> <span data-ttu-id="e53b4-251">Создание пакетов для версий Office профессиональный плюс и Office Стандартный, лицензированных для корпоративных лицензий, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e53b4-251">Creating packages for the volume-licensed versions of Office Professional Plus or Office Standard is not supported.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-252">Код продукта</span><span class="sxs-lookup"><span data-stu-id="e53b4-252">Product ID</span></span></th>
<th align="left"><span data-ttu-id="e53b4-253">Лицензирование подписки</span><span class="sxs-lookup"><span data-stu-id="e53b4-253">Subscription Licensing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e53b4-254">Office2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-254">Office 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e53b4-255">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="e53b4-255">O365ProPlusRetail</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="e53b4-256">Office 2016 с Visio 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-256">Office 2016 with Visio 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e53b4-257">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="e53b4-257">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="e53b4-258">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="e53b4-258">VisioProRetail</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="e53b4-259">Office 2016 с Visio 2016 и Project 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-259">Office 2016 with Visio 2016 and Project 2016</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="e53b4-260">O365ProPlusRetail</span><span class="sxs-lookup"><span data-stu-id="e53b4-260">O365ProPlusRetail</span></span></p>
<p><span data-ttu-id="e53b4-261">VisioProRetail</span><span class="sxs-lookup"><span data-stu-id="e53b4-261">VisioProRetail</span></span></p>
<p><span data-ttu-id="e53b4-262">ProjectProRetail</span><span class="sxs-lookup"><span data-stu-id="e53b4-262">ProjectProRetail</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="e53b4-263">Преобразование приложений Office в пакет App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-263">How to convert the Office applications into an App-V package</span></span>**

1. <span data-ttu-id="e53b4-264">В блокноте снова откройте файл CustomConfig.xml и внесите в него указанные ниже изменения.</span><span class="sxs-lookup"><span data-stu-id="e53b4-264">In Notepad, reopen the CustomConfig.xml file, and make the following changes to the file:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="e53b4-265">Параметр</span><span class="sxs-lookup"><span data-stu-id="e53b4-265">Parameter</span></span></th>
   <th align="left"><span data-ttu-id="e53b4-266">Что нужно сделать, чтобы изменить значение на</span><span class="sxs-lookup"><span data-stu-id="e53b4-266">What to change the value to</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="e53b4-267">Источник</span><span class="sxs-lookup"><span data-stu-id="e53b4-267">SourcePath</span></span></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-268">Наведите указатель мыши на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="e53b4-268">Point to the Office applications downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="e53b4-269">ProductID</span><span class="sxs-lookup"><span data-stu-id="e53b4-269">ProductID</span></span></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-270">Укажите лицензию на подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="e53b4-270">Specify Subscription licensing, as shown in the following example:</span></span></p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p><span data-ttu-id="e53b4-271">В этом примере были сделаны следующие изменения для создания пакета с лицензией на подписку.</span><span class="sxs-lookup"><span data-stu-id="e53b4-271">In this example, the following changes were made to create a package with Subscription licensing:</span></span></p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-272">Источник</span><span class="sxs-lookup"><span data-stu-id="e53b4-272">SourcePath</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-273">— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</span><span class="sxs-lookup"><span data-stu-id="e53b4-273">is the path, which was changed to point to the Office applications that were downloaded earlier.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e53b4-274">Код продукта</span><span class="sxs-lookup"><span data-stu-id="e53b4-274">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-275">для Office изменено на <code>O365ProPlusRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="e53b4-275">for Office was changed to <code>O365ProPlusRetail</code>.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-276">Код продукта</span><span class="sxs-lookup"><span data-stu-id="e53b4-276">Product ID</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-277">для Visio изменено на <code>VisioProRetail</code> .</span><span class="sxs-lookup"><span data-stu-id="e53b4-277">for Visio was changed to <code>VisioProRetail</code>.</span></span></p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="e53b4-278">ExcludeApp (необязательно)</span><span class="sxs-lookup"><span data-stu-id="e53b4-278">ExcludeApp (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-279">Позволяет указать программы Office, которые не нужно включать в пакет App-V, создаваемый средством развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-279">Lets you specify Office programs that you don’t want included in the App-V package that the Office Deployment Tool creates.</span></span> <span data-ttu-id="e53b4-280">Например, вы можете исключить Access и InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e53b4-280">For example, you can exclude Access and InfoPath.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="e53b4-281">PACKAGEGUID (необязательно)</span><span class="sxs-lookup"><span data-stu-id="e53b4-281">PACKAGEGUID (optional)</span></span></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-282">По умолчанию все пакеты App-V, созданные с помощью средства развертывания Office, имеют один и тот же идентификатор пакета App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-282">By default, all App-V packages created by the Office Deployment Tool share the same App-V Package ID.</span></span> <span data-ttu-id="e53b4-283">Вы можете использовать PACKAGEGUID, чтобы указать другой идентификатор пакета для каждого пакета, который позволяет публиковать несколько пакетов App-V, созданных средством развертывания Office, и управлять ими с помощью сервера App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-283">You can use PACKAGEGUID to specify a different package ID for each package, which allows you to publish multiple App-V packages, created by the Office Deployment Tool, and manage them by using the App-V Server.</span></span></p>
   <p><span data-ttu-id="e53b4-284">Например, если вы хотите использовать этот параметр, если вы создаете разные пакеты для разных пользователей.</span><span class="sxs-lookup"><span data-stu-id="e53b4-284">An example of when to use this parameter is if you create different packages for different users.</span></span> <span data-ttu-id="e53b4-285">Например, вы можете создать пакет с помощью Office 2016 для некоторых пользователей и создать еще один пакет с Office 2016 и Visio 2016 для другого набора пользователей.</span><span class="sxs-lookup"><span data-stu-id="e53b4-285">For example, you can create a package with just Office 2016 for some users, and create another package with Office 2016 and Visio 2016 for another set of users.</span></span></p>

   <span data-ttu-id="e53b4-286">&gt;<strong>Примечание </strong> . даже если вы используете уникальные идентификаторы пакетов, вы по-прежнему можете развернуть только один пакет App-V на одном устройстве.</span><span class="sxs-lookup"><span data-stu-id="e53b4-286">&gt;<strong>Note</strong> Even if you use unique package IDs, you can still deploy only one App-V package to a single device.</span></span>
   </td>
   </tr>
   </tbody>
   </table>


2. <span data-ttu-id="e53b4-287">С помощью команды/packager можно преобразовать приложения Office в пакет Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-287">Use the /packager command to convert the Office applications to an Office 2016 App-V package.</span></span>

   <span data-ttu-id="e53b4-288">Пример</span><span class="sxs-lookup"><span data-stu-id="e53b4-288">For example:</span></span>

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   <span data-ttu-id="e53b4-289">В примере:</span><span class="sxs-lookup"><span data-stu-id="e53b4-289">In the example:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-290">\server\Office2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-290">\server\Office2016</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-291">— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-291">is the network share location that contains the Office Deployment Tool and the custom Configuration.xml file, Customconfig.xml.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e53b4-292">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="e53b4-292">Setup.exe</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-293">— Это средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-293">is the Office Deployment Tool.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-294">/packager</span><span class="sxs-lookup"><span data-stu-id="e53b4-294">/packager</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-295">создает пакет App-V Office 2016 с типом лицензирования, указанным в файле customConfig.xml.</span><span class="sxs-lookup"><span data-stu-id="e53b4-295">creates the Office 2016 App-V package with the type of licensing specified in the customConfig.xml file.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong><span data-ttu-id="e53b4-296">\server\Office2016\Customconfig.xml</span><span class="sxs-lookup"><span data-stu-id="e53b4-296">\server\Office2016\Customconfig.xml</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-297">передает XML-файл конфигурации (в данном случае customConfig), подготовленный для этапа упаковки.</span><span class="sxs-lookup"><span data-stu-id="e53b4-297">passes the configuration XML file (in this case customConfig) that has been prepared for the packaging stage.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="e53b4-298">\server\share\Office 2016AppV</span><span class="sxs-lookup"><span data-stu-id="e53b4-298">\server\share\Office 2016AppV</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="e53b4-299">Указывает расположение только что созданного пакета Office App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-299">specifies the location of the newly created Office App-V package.</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. <span data-ttu-id="e53b4-300">Убедитесь в том, что пакет App-V для Office 2016 правильно работает:</span><span class="sxs-lookup"><span data-stu-id="e53b4-300">Verify that the Office 2016 App-V package works correctly:</span></span>

   1.  <span data-ttu-id="e53b4-301">Опубликуйте пакет App-V Office 2016, созданный глобально, на тестовом компьютере, и убедитесь, что появились ярлыки Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-301">Publish the Office 2016 App-V package, which you created globally, to a test computer, and verify that the Office 2016 shortcuts appear.</span></span>

   2.  <span data-ttu-id="e53b4-302">Запустите несколько приложений Office 2016, например Excel или Word, чтобы убедиться, что пакет работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="e53b4-302">Start a few Office 2016 applications, such as Excel or Word, to ensure that your package is working as expected.</span></span>

## <a href="" id="bkmk-pub-pkg-office"></a><span data-ttu-id="e53b4-303">Публикация пакета Office для App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-303">Publishing the Office package for App-V</span></span>


<span data-ttu-id="e53b4-304">Используйте указанные ниже сведения, чтобы опубликовать пакет Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-304">Use the following information to publish an Office package.</span></span>

### <span data-ttu-id="e53b4-305">Методы публикации пакетов приложения Office App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-305">Methods for publishing Office App-V packages</span></span>

<span data-ttu-id="e53b4-306">Развертывание пакета App-V для Office 2016 с помощью тех же способов, которые вы используете для любого другого пакета:</span><span class="sxs-lookup"><span data-stu-id="e53b4-306">Deploy the App-V package for Office 2016 by using the same methods you use for any other package:</span></span>

-   <span data-ttu-id="e53b4-307">System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e53b4-307">System Center Configuration Manager</span></span>

-   <span data-ttu-id="e53b4-308">Сервер App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-308">App-V Server</span></span>

-   <span data-ttu-id="e53b4-309">Самостоятельная работа с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="e53b4-309">Stand-alone through PowerShell commands</span></span>

### <span data-ttu-id="e53b4-310">Необходимые условия и требования к публикации</span><span class="sxs-lookup"><span data-stu-id="e53b4-310">Publishing prerequisites and requirements</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-311">Необходимые условия и требования</span><span class="sxs-lookup"><span data-stu-id="e53b4-311">Prerequisite or requirement</span></span></th>
<th align="left"><span data-ttu-id="e53b4-312">Сведения</span><span class="sxs-lookup"><span data-stu-id="e53b4-312">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-313">Включение сценариев PowerShell для клиентов App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-313">Enable PowerShell scripting on the App-V clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-314">Чтобы опубликовать пакеты Office 2016, необходимо выполнить сценарий.</span><span class="sxs-lookup"><span data-stu-id="e53b4-314">To publish Office 2016 packages, you must run a script.</span></span></p>
<p><span data-ttu-id="e53b4-315">Сценарии пакетов по умолчанию отключены для клиентов App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-315">Package scripts are disabled by default on App-V clients.</span></span> <span data-ttu-id="e53b4-316">Чтобы включить сценарии, выполните следующую команду PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e53b4-316">To enable scripting, run the following PowerShell command:</span></span></p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e53b4-317">Публикация пакета Office 2016 в глобальном масштабе</span><span class="sxs-lookup"><span data-stu-id="e53b4-317">Publish the Office 2016 package globally</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-318">Точки расширения в пакете Office App-V требуют установки на уровне компьютера.</span><span class="sxs-lookup"><span data-stu-id="e53b4-318">Extension points in the Office App-V package require installation at the computer level.</span></span></p>
<p><span data-ttu-id="e53b4-319">При публикации на уровне компьютера не требуется выполнять необходимые действия или распространяемые компоненты, а пакет Office 2016 глобально позволяет приложениям работать как в исходном установленном Office, устраняя необходимость настраивать пакеты для администраторов.</span><span class="sxs-lookup"><span data-stu-id="e53b4-319">When you publish at the computer level, no prerequisite actions or redistributables are needed, and the Office 2016 package globally enables its applications to work like natively installed Office, eliminating the need for administrators to customize packages.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="e53b4-320">Публикация пакета Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-320">How to publish an Office package</span></span>

<span data-ttu-id="e53b4-321">Выполните следующую команду, чтобы опубликовать пакет Office глобально.</span><span class="sxs-lookup"><span data-stu-id="e53b4-321">Run the following command to publish an Office package globally:</span></span>

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   <span data-ttu-id="e53b4-322">С консоли управления Веба на сервере App-V можно добавлять разрешения для группы компьютеров, а не для группы пользователей, чтобы пакеты могли публиковаться на компьютерах в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="e53b4-322">From the Web Management Console on the App-V Server, you can add permissions to a group of computers instead of to a user group to enable packages to be published globally to the computers in the corresponding group.</span></span>

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a><span data-ttu-id="e53b4-323">Настройка пакетов приложений Office App-V и управление ими</span><span class="sxs-lookup"><span data-stu-id="e53b4-323">Customizing and managing Office App-V packages</span></span>


<span data-ttu-id="e53b4-324">Для управления пакетами Office App-V используйте те же действия, что и для любого другого пакета, но есть несколько исключений, как описано в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="e53b4-324">To manage your Office App-V packages, use the same operations as you would for any other package, but there are a few exceptions, as outlined in the following sections.</span></span>

-   [<span data-ttu-id="e53b4-325">Включение подключаемых модулей Office с помощью групп подключений</span><span class="sxs-lookup"><span data-stu-id="e53b4-325">Enabling Office plug-ins by using connection groups</span></span>](#bkmk-enable-office-plugins)

-   [<span data-ttu-id="e53b4-326">Отключение приложений Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-326">Disabling Office 2016 applications</span></span>](#bkmk-disable-office-apps)

-   [<span data-ttu-id="e53b4-327">Отключение сочетаний клавиш в Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-327">Disabling Office 2016 shortcuts</span></span>](#bkmk-disable-shortcuts)

-   [<span data-ttu-id="e53b4-328">Управление обновлениями пакетов Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-328">Managing Office 2016 package upgrades</span></span>](#bkmk-manage-office-pkg-upgrd)

-   [<span data-ttu-id="e53b4-329">Развертывание Visio 2016 и Project 2016 с Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-329">Deploying Visio 2016 and Project 2016 with Office</span></span>](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a><span data-ttu-id="e53b4-330">Включение подключаемых модулей Office с помощью групп подключений</span><span class="sxs-lookup"><span data-stu-id="e53b4-330">Enabling Office plug-ins by using connection groups</span></span>

<span data-ttu-id="e53b4-331">Выполните действия, описанные в этом разделе, чтобы включить подключаемые модули Office для пакета Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-331">Use the steps in this section to enable Office plug-ins with your Office package.</span></span> <span data-ttu-id="e53b4-332">Чтобы использовать подключаемые модули Office, необходимо использовать секвенсор App-V для создания отдельного пакета, содержащего только подключаемые модули. Вы не можете использовать средство развертывания Office для создания пакета подключаемых модулей.</span><span class="sxs-lookup"><span data-stu-id="e53b4-332">To use Office plug-ins, you must use the App-V Sequencer to create a separate package that contains just the plug-ins. You cannot use the Office Deployment Tool to create the plug-ins package.</span></span> <span data-ttu-id="e53b4-333">Затем создайте группу подключения, которая включает пакет Office и пакет подключаемых модулей, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="e53b4-333">You then create a connection group that contains the Office package and the plug-ins package, as described in the following steps.</span></span>

**<span data-ttu-id="e53b4-334">Чтобы включить подключаемые модули для пакетов Office App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-334">To enable plug-ins for Office App-V packages</span></span>**

1.  <span data-ttu-id="e53b4-335">Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e53b4-335">Add a Connection Group through App-V Server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

2.  <span data-ttu-id="e53b4-336">Поочередные подключаемые модули с помощью секвенсора App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-336">Sequence your plug-ins using the App-V Sequencer.</span></span> <span data-ttu-id="e53b4-337">Убедитесь, что на компьютере, используемом для последовательного подключения к сети, установлен Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-337">Ensure that Office 2016 is installed on the computer being used to sequence the plug-in.</span></span> <span data-ttu-id="e53b4-338">При последовательности подключаемых модулей Office 2016 рекомендуется использовать приложения Microsoft 365 для предприятий (невиртуальные) на компьютере с виртуализацией.</span><span class="sxs-lookup"><span data-stu-id="e53b4-338">It is recommended you use Microsoft 365 Apps for enterprise(non-virtual) on the sequencing computer when you sequence Office 2016 plug-ins.</span></span>

3.  <span data-ttu-id="e53b4-339">Создайте пакет App-V, который содержит нужные подключаемые модули.</span><span class="sxs-lookup"><span data-stu-id="e53b4-339">Create an App-V package that includes the desired plug-ins.</span></span>

4.  <span data-ttu-id="e53b4-340">Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e53b4-340">Add a Connection Group through App-V server, System Center Configuration Manager, or a PowerShell cmdlet.</span></span>

5.  <span data-ttu-id="e53b4-341">Добавьте пакет приложений Office 2016 App-V и подключаемый комплект, который вы последовательно расдобавили в группу подключений, которую вы создали.</span><span class="sxs-lookup"><span data-stu-id="e53b4-341">Add the Office 2016 App-V package and the plug-ins package you sequenced to the Connection Group you created.</span></span>

    ><span data-ttu-id="e53b4-342">**Важно!** Порядок пакетов в группе подключения определяет порядок, в котором будет объединено содержимое пакета.</span><span class="sxs-lookup"><span data-stu-id="e53b4-342">**Important** The order of the packages in the Connection Group determines the order in which the package contents are merged.</span></span> <span data-ttu-id="e53b4-343">В файле-дескрипторе группы подключения сначала добавьте пакет Office 2016 App-V, а затем добавьте пакет App-V для плагина.</span><span class="sxs-lookup"><span data-stu-id="e53b4-343">In your Connection group descriptor file, add the Office 2016 App-V package first, and then add the plug-in App-V package.</span></span>



6.  <span data-ttu-id="e53b4-344">Убедитесь, что оба пакета опубликованы на целевом компьютере, и что пакет Plug-in опубликован глобально, чтобы они соответствовали глобальным параметрам опубликованного пакета Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-344">Ensure that both packages are published to the target computer and that the plug-in package is published globally to match the global settings of the published Office 2016 App-V package.</span></span>

7.  <span data-ttu-id="e53b4-345">Убедитесь в том, что в файле конфигурации развертывания для пакета Plug-in установлены те же параметры, что и в пакете приложения Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-345">Verify that the Deployment Configuration File of the plug-in package has the same settings that the Office 2016 App-V package has.</span></span>

    <span data-ttu-id="e53b4-346">Так как пакет Office 2016 App-V интегрируется с операционной системой, параметры комплекта для подключения должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="e53b4-346">Since the Office 2016 App-V package is integrated with the operating system, the plug-in package settings should match.</span></span> <span data-ttu-id="e53b4-347">Вы можете выполнить поиск по файлу конфигурации развертывания в режиме COM и убедиться, что для пакета подключаемых модулей установлено значение "Интеграция", и что "InProcessEnabled" и "OutOfProcessEnabled" соответствуют параметрам пакета Office 2016 App-V, который вы опубликовали.</span><span class="sxs-lookup"><span data-stu-id="e53b4-347">You can search the Deployment Configuration File for “COM Mode” and ensure that your plug-ins package has that value set as “Integrated” and that both "InProcessEnabled" and "OutOfProcessEnabled" match the settings of the Office 2016 App-V package you published.</span></span>

8.  <span data-ttu-id="e53b4-348">Откройте файл конфигурации развертывания и задайте для параметра значения для **объектов** значение **false**.</span><span class="sxs-lookup"><span data-stu-id="e53b4-348">Open the Deployment Configuration File and set the value for **Objects Enabled** to **false**.</span></span>

9.  <span data-ttu-id="e53b4-349">Если вы внесли изменения в файл конфигурации развертывания после выполнения последовательности, убедитесь в том, что пакет Plug-in опубликован с файлом.</span><span class="sxs-lookup"><span data-stu-id="e53b4-349">If you made any changes to the Deployment Configuration file after sequencing, ensure that the plug-in package is published with the file.</span></span>

10. <span data-ttu-id="e53b4-350">Убедитесь, что созданная группа подключения включена на нужном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e53b4-350">Ensure that the Connection Group you created is enabled onto your desired computer.</span></span> <span data-ttu-id="e53b4-351">Если пакет Office 2016 App-V используется, если группа подключений включена, возможно, созданная группа подключения будет "отложить".</span><span class="sxs-lookup"><span data-stu-id="e53b4-351">The Connection Group created will likely “pend” if the Office 2016 App-V package is in use when the Connection Group is enabled.</span></span> <span data-ttu-id="e53b4-352">В этом случае вам потребуется перезагрузить компьютер, чтобы успешно включить группу соединений.</span><span class="sxs-lookup"><span data-stu-id="e53b4-352">If that happens, you have to reboot to successfully enable the Connection Group.</span></span>

11. <span data-ttu-id="e53b4-353">После успешной публикации обоих пакетов и включения группы подключения запустите целевое приложение Office 2016 и убедитесь, что подключенный и добавленный в группу подключения внешний сервер работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="e53b4-353">After you successfully publish both packages and enable the Connection Group, start the target Office 2016 application and verify that the plug-in you published and added to the connection group works as expected.</span></span>

### <a href="" id="bkmk-disable-office-apps"></a><span data-ttu-id="e53b4-354">Отключение приложений Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-354">Disabling Office 2016 applications</span></span>

<span data-ttu-id="e53b4-355">Вам может потребоваться отключить определенные приложения в пакете Office App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-355">You may want to disable specific applications in your Office App-V package.</span></span> <span data-ttu-id="e53b4-356">Например, вы можете отключить Access, но оставить все остальные доступные приложения Office в главном приложении.</span><span class="sxs-lookup"><span data-stu-id="e53b4-356">For instance, you can disable Access, but leave all other Office application main available.</span></span> <span data-ttu-id="e53b4-357">При отключении приложения конечный пользователь больше не увидит ярлык для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="e53b4-357">When you disable an application, the end user will no longer see the shortcut for that application.</span></span> <span data-ttu-id="e53b4-358">Переупорядочение приложения не требуется.</span><span class="sxs-lookup"><span data-stu-id="e53b4-358">You do not have to re-sequence the application.</span></span> <span data-ttu-id="e53b4-359">При изменении файла конфигурации развертывания после публикации пакета Office 2016 App-V необходимо сохранить изменения, добавить пакет приложения Office 2016 и затем повторно опубликовать его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-359">When you change the Deployment Configuration File after the Office 2016 App-V package has been published, you will save the changes, add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

><span data-ttu-id="e53b4-360">**Примечание** Чтобы исключить определенные приложения Office (например, Access и InfoPath) при создании пакета App-V с помощью средства развертывания Office, используйте параметр **ExcludeApp** .</span><span class="sxs-lookup"><span data-stu-id="e53b4-360">**Note** To exclude specific Office applications (for example, Access and InfoPath) when you create the App-V package with the Office Deployment Tool, use the **ExcludeApp** setting.</span></span>


**<span data-ttu-id="e53b4-361">Отключение приложения Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-361">To disable an Office 2016 application</span></span>**

1.  <span data-ttu-id="e53b4-362">Откройте файл конфигурации развертывания в текстовом редакторе, например в **блокноте** , и выполните поиск по слову "приложения".</span><span class="sxs-lookup"><span data-stu-id="e53b4-362">Open a Deployment Configuration File with a text editor such as **Notepad** and search for “Applications."</span></span>

2.  <span data-ttu-id="e53b4-363">Найдите приложение Office, которое вы хотите отключить, например Access 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-363">Search for the Office application you want to disable, for example, Access 2016.</span></span>

3.  <span data-ttu-id="e53b4-364">Измените значение "включено" с "истина" на "ложь".</span><span class="sxs-lookup"><span data-stu-id="e53b4-364">Change the value of "Enabled" from "true" to "false."</span></span>

4.  <span data-ttu-id="e53b4-365">Сохраните файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="e53b4-365">Save the Deployment Configuration File.</span></span>

5.  <span data-ttu-id="e53b4-366">Добавьте пакет App-V Office 2016 с новым файлом конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="e53b4-366">Add the Office 2016 App-V Package with the new Deployment Configuration File.</span></span>

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  <span data-ttu-id="e53b4-367">Повторно добавьте пакет Office 2016 App-V, а затем снова опубликуйте его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2016 App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-367">Re-add the Office 2016 App-V package, and then republish it with the new Deployment Configuration File to apply the new settings to Office 2016 App-V Package applications.</span></span>

### <a href="" id="bkmk-disable-shortcuts"></a><span data-ttu-id="e53b4-368">Отключение сочетаний клавиш в Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-368">Disabling Office 2016 shortcuts</span></span>

<span data-ttu-id="e53b4-369">Вместо отмены публикации или удаления пакета вы можете отключить сочетания клавиш для некоторых приложений Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-369">You may want to disable shortcuts for certain Office applications instead of unpublishing or removing the package.</span></span> <span data-ttu-id="e53b4-370">В следующем примере показано, как отключить сочетания клавиш для Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e53b4-370">The following example shows how to disable shortcuts for Microsoft Access.</span></span>

**<span data-ttu-id="e53b4-371">Отключение сочетаний клавиш для приложений Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-371">To disable shortcuts for Office 2016 applications</span></span>**

1.  <span data-ttu-id="e53b4-372">Откройте файл конфигурации развертывания в блокноте и выполните поиск по запросу "ярлыки".</span><span class="sxs-lookup"><span data-stu-id="e53b4-372">Open a Deployment Configuration File in Notepad and search for “Shortcuts”.</span></span>

2.  <span data-ttu-id="e53b4-373">Чтобы отключить определенные сочетания клавиш, удалите или закомментируйте конкретные сочетания клавиш, которые вам не нужны.</span><span class="sxs-lookup"><span data-stu-id="e53b4-373">To disable certain shortcuts, delete or comment out the specific shortcuts you don’t want.</span></span> <span data-ttu-id="e53b4-374">Подсистема должна быть доступна и включена.</span><span class="sxs-lookup"><span data-stu-id="e53b4-374">You must keep the subsystem present and enabled.</span></span> <span data-ttu-id="e53b4-375">Например, в приведенном ниже примере удалите сочетания клавиш Microsoft Access, сохранив при этом ярлыки/shortcut не &lt; &gt; &lt; &gt; смогут отключить ярлык Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e53b4-375">For example, in the example below, delete the Microsoft Access shortcuts, while keeping the subsystems &lt;shortcut&gt; &lt;/shortcut&gt; intact to disable the Microsoft Access shortcut.</span></span>

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  <span data-ttu-id="e53b4-376">Сохраните файл конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="e53b4-376">Save the Deployment Configuration File.</span></span>

4.  <span data-ttu-id="e53b4-377">Повторно опубликуйте пакет Office 2016 App-V с новым файлом конфигурации развертывания.</span><span class="sxs-lookup"><span data-stu-id="e53b4-377">Republish Office 2016 App-V Package with new Deployment Configuration File.</span></span>

<span data-ttu-id="e53b4-378">Многие дополнительные параметры можно изменить, изменив конфигурацию развертывания для пакетов App-V, например сопоставления типов файлов, виртуальной файловой системы и т. д.</span><span class="sxs-lookup"><span data-stu-id="e53b4-378">Many additional settings can be changed through modifying the Deployment Configuration for App-V packages, for example, file type associations, Virtual File System, and more.</span></span> <span data-ttu-id="e53b4-379">Дополнительные сведения об использовании файлов конфигурации развертывания для изменения параметров пакета App-V можно найти в разделе Дополнительные ресурсы в конце документа.</span><span class="sxs-lookup"><span data-stu-id="e53b4-379">For additional information on how to use Deployment Configuration Files to change App-V package settings, refer to the additional resources section at the end of this document.</span></span>

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a><span data-ttu-id="e53b4-380">Управление обновлениями пакетов Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-380">Managing Office 2016 package upgrades</span></span>

<span data-ttu-id="e53b4-381">Чтобы обновить пакет Office 2016, используйте средство развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-381">To upgrade an Office 2016 package, use the Office Deployment Tool.</span></span> <span data-ttu-id="e53b4-382">Чтобы обновить ранее развернутый пакет Office 2016, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e53b4-382">To upgrade a previously deployed Office 2016 package, perform the following steps.</span></span>

**<span data-ttu-id="e53b4-383">Как обновить ранее развернутый пакет Office 2016</span><span class="sxs-lookup"><span data-stu-id="e53b4-383">How to upgrade a previously deployed Office 2016 package</span></span>**

1. <span data-ttu-id="e53b4-384">Создайте новый пакет Office 2016 с помощью средства развертывания Office, которое использует самую последнюю версию приложения Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-384">Create a new Office 2016 package through the Office Deployment Tool that uses the most recent Office 2016 application software.</span></span> <span data-ttu-id="e53b4-385">Последние биты Office 2016 всегда можно получить на этапе загрузки пакета App-V приложения Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-385">The most recent Office 2016 bits can always be obtained through the download stage of creating an Office 2016 App-V Package.</span></span> <span data-ttu-id="e53b4-386">Недавно созданный пакет Office 2016 содержит самые последние обновления и новый идентификатор версии.</span><span class="sxs-lookup"><span data-stu-id="e53b4-386">The newly created Office 2016 package will have the most recent updates and a new Version ID.</span></span> <span data-ttu-id="e53b4-387">Все пакеты, созданные с помощью средства развертывания Office, имеют одинаковый журнал обращений.</span><span class="sxs-lookup"><span data-stu-id="e53b4-387">All packages created using the Office Deployment Tool have the same lineage.</span></span>

   > <span data-ttu-id="e53b4-388">**Примечание** У пакетов Office App-V есть два идентификатора версии:</span><span class="sxs-lookup"><span data-stu-id="e53b4-388">**Note** Office App-V packages have two Version IDs:</span></span>
   > <ul>
   > <li><span data-ttu-id="e53b4-389">Идентификатор версии пакета App-V для Office 2016, уникальный для всех пакетов, созданных с помощью средства развертывания Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-389">An Office 2016 App-V Package Version ID that is unique across all packages created using the Office Deployment Tool.</span></span></li>
   > <li><span data-ttu-id="e53b4-390">Второй идентификатор версии пакета App-V, x. x. x. x, например, в манифесте AppX, который будет изменен только в том случае, если у вас есть новая версия Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-390">A second App-V Package Version ID, x.x.x.x for example, in the AppX manifest that will only change if there is a new version of Office itself.</span></span> <span data-ttu-id="e53b4-391">Например, если выпущена новая версия Office 2016 с обновлениями, а пакет создан с помощью средства развертывания Office для включения этих обновлений, номер версии X. X. x. X изменится, чтобы показать, что сама версия Office изменилась.</span><span class="sxs-lookup"><span data-stu-id="e53b4-391">For example, if a new Office 2016 release with upgrades is available, and a package is created through the Office Deployment Tool to incorporate these upgrades, the X.X.X.X version ID will change to reflect that the Office version itself has changed.</span></span> <span data-ttu-id="e53b4-392">Сервер App-V использует номер версии X. X. X. X, чтобы отличать этот пакет и распознать, что он будет содержать новые обновления для ранее опубликованного пакета, и в результате его можно опубликовать как обновление для существующего пакета Office 2016.</span><span class="sxs-lookup"><span data-stu-id="e53b4-392">The App-V server will use the X.X.X.X version ID to differentiate this package and recognize that it contains new upgrades to the previously published package, and as a result, publish it as an upgrade to the existing Office 2016 package.</span></span></li>
   > </ul>


2. <span data-ttu-id="e53b4-393">Глобально опубликуйте созданные пакеты Office 2016 App-V на компьютерах, на которых вы хотите применить новые обновления.</span><span class="sxs-lookup"><span data-stu-id="e53b4-393">Globally publish the newly created Office 2016 App-V Packages onto computers where you would like to apply the new updates.</span></span> <span data-ttu-id="e53b4-394">Так как новый пакет имеет тот же журнал обращений к устаревшему пакету Office 2016 App-V, при публикации нового пакета с обновлениями будут применены только новые изменения старого пакета, поэтому они будут быстрее.</span><span class="sxs-lookup"><span data-stu-id="e53b4-394">Since the new package has the same lineage of the older Office 2016 App-V Package, publishing the new package with the updates will only apply the new changes to the old package, and thus will be fast.</span></span>

3. <span data-ttu-id="e53b4-395">Обновления будут применены таким же образом для глобальных опубликованных пакетов App-V.</span><span class="sxs-lookup"><span data-stu-id="e53b4-395">Upgrades will be applied in the same manner of any globally published App-V Packages.</span></span> <span data-ttu-id="e53b4-396">Так как приложения, скорее всего, будут использоваться, обновления могут быть отложены до тех пор, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="e53b4-396">Because applications will probably be in use, upgrades might be delayed until the computer is rebooted.</span></span>


### <a href="" id="bkmk-deploy-visio-project"></a><span data-ttu-id="e53b4-397">Развертывание Visio 2016 и Project 2016 с Office</span><span class="sxs-lookup"><span data-stu-id="e53b4-397">Deploying Visio 2016 and Project 2016 with Office</span></span>

<span data-ttu-id="e53b4-398">В таблице ниже описаны требования и параметры для развертывания Visio 2016 и Project 2016 с Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-398">The following table describes the requirements and options for deploying Visio 2016 and Project 2016 with Office.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-399">Задача</span><span class="sxs-lookup"><span data-stu-id="e53b4-399">Task</span></span></th>
<th align="left"><span data-ttu-id="e53b4-400">Сведения</span><span class="sxs-lookup"><span data-stu-id="e53b4-400">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-401">Как упаковать и опубликовать Visio 2016 и Project 2016 с Office?</span><span class="sxs-lookup"><span data-stu-id="e53b4-401">How do I package and publish Visio 2016 and Project 2016 with Office?</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-402">Вы должны включить Visio 2016 и Project 2016 в один и тот же пакет для Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-402">You must include Visio 2016 and Project 2016 in the same package with Office.</span></span></p>
<p><span data-ttu-id="e53b4-403">Если вы не развертываете Office, вы можете создать пакет, содержащий Visio и/или Project, при условии соблюдения требований к упаковке, публикации и развертыванию, описанным в этой статье.</span><span class="sxs-lookup"><span data-stu-id="e53b4-403">If you aren’t deploying Office, you can create a package that contains Visio and/or Project, as long as you follow the packaging, publishing, and deployment requirements described in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e53b4-404">Как развернуть Visio 2016 и Project 2016 для определенных пользователей?</span><span class="sxs-lookup"><span data-stu-id="e53b4-404">How can I deploy Visio 2016 and Project 2016 to specific users?</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-405">Воспользуйтесь одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="e53b4-405">Use one of the following methods:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e53b4-406">Если вы хотите...</span><span class="sxs-lookup"><span data-stu-id="e53b4-406">If you want to...</span></span></th>
<th align="left"><span data-ttu-id="e53b4-407">... затем используйте этот метод</span><span class="sxs-lookup"><span data-stu-id="e53b4-407">...then use this method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e53b4-408">Создание двух разных пакетов и развертывание каждого из них в другой группе пользователей</span><span class="sxs-lookup"><span data-stu-id="e53b4-408">Create two different packages and deploy each one to a different group of users</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-409">Создание и развертывание следующих пакетов:</span><span class="sxs-lookup"><span data-stu-id="e53b4-409">Create and deploy the following packages:</span></span></p>
<ul>
<li><p><span data-ttu-id="e53b4-410">Пакет, содержащий только Office — развертывание на компьютерах, пользователям которых требуется только Office.</span><span class="sxs-lookup"><span data-stu-id="e53b4-410">A package that contains only Office - deploy to computers whose users need only Office.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-411">Пакет, содержащий Office, Visio и Project-deploy, на компьютеры, для пользователей которых нужны все три приложения.</span><span class="sxs-lookup"><span data-stu-id="e53b4-411">A package that contains Office, Visio, and Project - deploy to computers whose users need all three applications.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e53b4-412">Если вам нужен только один пакет для всей организации или если у вас есть пользователи, которым предоставлен доступ к компьютерам:</span><span class="sxs-lookup"><span data-stu-id="e53b4-412">If you want only one package for the whole organization, or if you have users who share computers:</span></span></p></td>
<td align="left"><p><span data-ttu-id="e53b4-413">Выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="e53b4-413">Follows these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="e53b4-414">Создание пакета, содержащего Office, Visio и Project.</span><span class="sxs-lookup"><span data-stu-id="e53b4-414">Create a package that contains Office, Visio, and Project.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-415">Развертывание пакета для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="e53b4-415">Deploy the package to all users.</span></span></p></li>
<li><p><span data-ttu-id="e53b4-416">Используйте <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , чтобы запретить определенным пользователям использовать Visio и Project.</span><span class="sxs-lookup"><span data-stu-id="e53b4-416">Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)">Microsoft AppLocker</a> to prevent specific users from using Visio and Project.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>


## <span data-ttu-id="e53b4-417">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e53b4-417">Additional resources</span></span>


[<span data-ttu-id="e53b4-418">Развертывание Microsoft Office 2013 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-418">Deploying Microsoft Office 2013 by Using App-V</span></span>](deploying-microsoft-office-2013-by-using-app-v.md)

[<span data-ttu-id="e53b4-419">Развертывание Microsoft Office 2010 с помощью App-V</span><span class="sxs-lookup"><span data-stu-id="e53b4-419">Deploying Microsoft Office 2010 by Using App-V</span></span>](deploying-microsoft-office-2010-by-using-app-v.md)

[<span data-ttu-id="e53b4-420">Средство развертывания Office 2016 для "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="e53b4-420">Office 2016 Deployment Tool for Click-to-Run</span></span>](https://www.microsoft.com/download/details.aspx?id=49117)

**<span data-ttu-id="e53b4-421">Группы подключения</span><span class="sxs-lookup"><span data-stu-id="e53b4-421">Connection Groups</span></span>**

[<span data-ttu-id="e53b4-422">Развертывание групп подключений в Microsoft App-V V5</span><span class="sxs-lookup"><span data-stu-id="e53b4-422">Deploying Connection Groups in Microsoft App-V v5</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[<span data-ttu-id="e53b4-423">Управление связывающими группами</span><span class="sxs-lookup"><span data-stu-id="e53b4-423">Managing Connection Groups</span></span>](managing-connection-groups.md)

**<span data-ttu-id="e53b4-424">Динамическая настройка</span><span class="sxs-lookup"><span data-stu-id="e53b4-424">Dynamic Configuration</span></span>**

[<span data-ttu-id="e53b4-425">Сведения о динамической конфигурации App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="e53b4-425">About App-V 5.1 Dynamic Configuration</span></span>](about-app-v-51-dynamic-configuration.md)





