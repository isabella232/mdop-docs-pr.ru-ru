---
title: Заметки о выпуске App-V 4.6 с пакетом обновления 1 (SP1)
description: Заметки о выпуске App-V 4.6 с пакетом обновления 1 (SP1)
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819839"
---
# <span data-ttu-id="5565c-103">Заметки о выпуске App-V 4.6 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="5565c-103">App-V 4.6 SP1 Release Notes</span></span>


<span data-ttu-id="5565c-104">Чтобы найти заметки о выпуске, нажмите клавиши CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="5565c-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="5565c-105">**Важно!**  Внимательно прочтите эти заметки о выпуске, прежде чем устанавливать систему управления Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="5565c-105">**Important** Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="5565c-106">Эти заметки о выпуске содержат сведения, которые помогут вам успешно установить Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="5565c-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="5565c-107">Этот документ содержит сведения, недоступные в документации по продукту.</span><span class="sxs-lookup"><span data-stu-id="5565c-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="5565c-108">Если между этими заметками о выпуске и другой документацией приложения App-V есть разница, Последнее изменение должно считаться полномочным.</span><span class="sxs-lookup"><span data-stu-id="5565c-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span>

 

## <span data-ttu-id="5565c-109">Защита от уязвимостей и вирусов в системе безопасности</span><span class="sxs-lookup"><span data-stu-id="5565c-109">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="5565c-110">Для защиты от уязвимостей и вирусов в системе безопасности важно установить последние обновления безопасности для любого нового программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="5565c-110">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="5565c-111">Дополнительные сведения можно найти на [веб-сайте Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="5565c-111">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="5565c-112">Известные проблемы с виртуализацией приложений версии 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="5565c-112">Known Issues with Application Virtualization4.6 SP1</span></span>


<span data-ttu-id="5565c-113">Этот раздел содержит наиболее актуальные сведения о проблемах, связанных с Microsoft Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="5565c-113">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="5565c-114">Эти проблемы не отображаются в документации на продукт, и в некоторых случаях может привести к противоречию с существующим документом о продукте.</span><span class="sxs-lookup"><span data-stu-id="5565c-114">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="5565c-115">По возможности эти проблемы будут рассмотрены в более поздних выпусках.</span><span class="sxs-lookup"><span data-stu-id="5565c-115">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="5565c-116">Путь из SPRT теряется, если он не заканчивается косой чертой (/)</span><span class="sxs-lookup"><span data-stu-id="5565c-116">Path from SPRT is lost if it does not end in forward slash ( / )</span></span>

<span data-ttu-id="5565c-117">Если путь в HREF в шаблоне проекта не заканчивается косой чертой ( **/** ), созданный элемент HREF не включает путь.</span><span class="sxs-lookup"><span data-stu-id="5565c-117">When the path in an HREF in a project template does not end with a forward slash (**/**), the generated HREF does not include the path.</span></span> <span data-ttu-id="5565c-118">Это случается, когда пользователь вручную управляет файлом **. SPRT** .</span><span class="sxs-lookup"><span data-stu-id="5565c-118">This occurs when the user manually manipulates the **.sprt** file.</span></span> <span data-ttu-id="5565c-119">Если используется секвенсор, он всегда добавляет косую черту ( **/** ) после пути.</span><span class="sxs-lookup"><span data-stu-id="5565c-119">If you use the sequencer it always adds the forward slash (**/**) after the path.</span></span>

<span data-ttu-id="5565c-120">ВРЕМЕННОе решение убедитесь, что в HREF есть завершающая косая черта ( **/** ).</span><span class="sxs-lookup"><span data-stu-id="5565c-120">WORKAROUND Make sure that the HREF has a trailing forward slash (**/**).</span></span>

### <span data-ttu-id="5565c-121">Имя папки пользователя не соответствует имени пакета</span><span class="sxs-lookup"><span data-stu-id="5565c-121">User folder name do not correspond to the package name</span></span>

<span data-ttu-id="5565c-122">Папки, содержащие файлы Users и Global. pkg, больше не содержат имя пакета.</span><span class="sxs-lookup"><span data-stu-id="5565c-122">Folders that contain user and global .pkg files no longer include the package name.</span></span> <span data-ttu-id="5565c-123">Ранее в клиенте App-V используется краткое имя корневой папки пакета 8,3 в качестве части имени папки.</span><span class="sxs-lookup"><span data-stu-id="5565c-123">Previously, the App-V client used to use the package root folder 8.3 short name as part of the folder name.</span></span> <span data-ttu-id="5565c-124">Это позволяет легко определить его.</span><span class="sxs-lookup"><span data-stu-id="5565c-124">This lets you easily identify it.</span></span> <span data-ttu-id="5565c-125">При использовании секвенсора App-V 4,6 с пакетом обновления 1 (SP1) корневой папки пакета 8,3 короткие имена теперь являются случайными строками.</span><span class="sxs-lookup"><span data-stu-id="5565c-125">When you use the App-V 4.6 SP1 sequencer, the package root folder 8.3 short names are now random strings.</span></span> <span data-ttu-id="5565c-126">Это затрудняет определение папок, содержащих файлы пакета **. pkg** на компьютере, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="5565c-126">This makes it difficult to identify the folders that contain the package’s **.pkg** files on the computer that is running the App-V client.</span></span>

<span data-ttu-id="5565c-127">ВРЕМЕННОе решение для упрощения идентификации этих папок пакета используйте один из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="5565c-127">WORKAROUND Use one of the following methods to more easily identify these package folders:</span></span>

1.  <span data-ttu-id="5565c-128">Когда вы создаете пакет с помощью секвенсора, укажите имя папки, которое соответствует соглашению об именовании 8,3 для основного каталога приложения.</span><span class="sxs-lookup"><span data-stu-id="5565c-128">When you create the package by using the Sequencer, specify a folder name that follows the 8.3 naming convention for the primary application folder.</span></span> <span data-ttu-id="5565c-129">Это имя будет использоваться в качестве части имени папки пользователя, как это было в App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="5565c-129">This name will then be used as part of the user folder name as was the case in App-V 4.6.</span></span>

2.  <span data-ttu-id="5565c-130">Файл. SPRJ теперь содержит тег, отображающий строку, которая используется в качестве начала имени папки пользователя.</span><span class="sxs-lookup"><span data-stu-id="5565c-130">The .sprj file now contains a tag that displays the string that is used as the beginning of the user folder name.</span></span> <span data-ttu-id="5565c-131">Вы можете использовать элемент **SHORTNAME** элемента **PACKAGEROOTFOLDER** для определения имени.</span><span class="sxs-lookup"><span data-stu-id="5565c-131">You can use the **SHORTNAME** element of the **PACKAGEROOTFOLDER** element to determine the name.</span></span>

### <span data-ttu-id="5565c-132">Выполнение App-V 4,6 SP1 на компьютерах с более чем 64 процессорами</span><span class="sxs-lookup"><span data-stu-id="5565c-132">Running App-V 4.6 SP1 on computers that have more than 64 processors</span></span>

<span data-ttu-id="5565c-133">При запуске App-V 4,6 SP1 на компьютерах, на которых установлено более 64 процессоров, клиент App-V завершает работу со сбоем.</span><span class="sxs-lookup"><span data-stu-id="5565c-133">When you run App-V 4.6 SP1 on computers that have more than 64 processors installed, the App-V client fails.</span></span>

<span data-ttu-id="5565c-134">ВРЕМЕННОе решение None.</span><span class="sxs-lookup"><span data-stu-id="5565c-134">WORKAROUND None.</span></span> <span data-ttu-id="5565c-135">Эта конфигурация не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5565c-135">This configuration is not supported.</span></span> <span data-ttu-id="5565c-136">Вы должны запустить App-V 4,6 SP1on на компьютерах с менее чем 64 процессорами.</span><span class="sxs-lookup"><span data-stu-id="5565c-136">You must run App-V 4.6 SP1on computers that have fewer than 64 processors.</span></span>

### <span data-ttu-id="5565c-137">Обновление Application Virtualization 4,6 с пакетом обновления 1 (SP1) не предлагается на всех языках, использующих Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="5565c-137">Application Virtualization 4.6 SP1 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="5565c-138">При использовании центра обновления Майкрософт Обновление для App-V 4,6 SP1 недоступно для языковых стандартов, указанных ниже.</span><span class="sxs-lookup"><span data-stu-id="5565c-138">When you use Microsoft Update, the update for App-V 4.6 SP1 is not available for the following language locales:</span></span>

-   <span data-ttu-id="5565c-139">Казахский</span><span class="sxs-lookup"><span data-stu-id="5565c-139">Kazakh</span></span>

-   <span data-ttu-id="5565c-140">Хинди</span><span class="sxs-lookup"><span data-stu-id="5565c-140">Hindi</span></span>

-   <span data-ttu-id="5565c-141">Сербский (кириллица)</span><span class="sxs-lookup"><span data-stu-id="5565c-141">Serbian-Cyrillic</span></span>

<span data-ttu-id="5565c-142">ВРЕМЕННОе решение если вы используете Microsoft Windows Server Update Services (WSUS), используйте английскую версию обновления или загрузите обновление из каталога Центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5565c-142">WORKAROUND If you are using Microsoft Windows Server Update Services (WSUS) use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

### <span data-ttu-id="5565c-143">После того как вы разворачиваете родительский пакет, вы не можете последовательное соединение с помощью компонентов параллельных устройств</span><span class="sxs-lookup"><span data-stu-id="5565c-143">After expanding the parent package, you cannot sequence a plug-in with side by side components</span></span>

<span data-ttu-id="5565c-144">Если вы развернете родительский пакет с помощью **средств**  /  **распаковать пакет в локальную систему** на консоли секвенсора App-V и вы попытаетесь поочередно использовать плагин с компонентами на стороне стороны, будет возвращена ошибка установки.</span><span class="sxs-lookup"><span data-stu-id="5565c-144">When you expand a parent package by using **Tools** / **Expand Package to Local System** in the App-V Sequencer console and you sequence a plug-in with side by side components, an installation error is returned.</span></span> <span data-ttu-id="5565c-145">Пример</span><span class="sxs-lookup"><span data-stu-id="5565c-145">For example:</span></span>

-   **<span data-ttu-id="5565c-146">HRESULT 0x80073712</span><span class="sxs-lookup"><span data-stu-id="5565c-146">HRESULT 0x80073712</span></span>**

<span data-ttu-id="5565c-147">Это происходит, когда секвенсор записывает в реестр параллельный компонент, но не очищает значение для следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="5565c-147">This is caused when the sequencer writes the side-by-side component to the registry but does not clear the value for the following registry key:</span></span>

<span data-ttu-id="5565c-148">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="5565c-148">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="5565c-149">ВРЕМЕННОе решение после развертывания родительского пакета на компьютере, на котором запущен секвенсор, необходимо удалить значение для следующего раздела реестра:</span><span class="sxs-lookup"><span data-stu-id="5565c-149">WORKAROUND After expanding the parent package on the computer that is running the sequencer, you have to delete the value for the following registry key:</span></span>

<span data-ttu-id="5565c-150">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="5565c-150">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="5565c-151">После того как вы удалите значение, поочередно Подключите плагин.</span><span class="sxs-lookup"><span data-stu-id="5565c-151">After you have deleted the value, sequence the plug-in.</span></span>

### <span data-ttu-id="5565c-152">Сведения о заметках об авторском праве</span><span class="sxs-lookup"><span data-stu-id="5565c-152">Release Notes Copyright Information</span></span>

<span data-ttu-id="5565c-153">Этот документ предоставляется "как есть".</span><span class="sxs-lookup"><span data-stu-id="5565c-153">This document is provided “as-is”.</span></span> <span data-ttu-id="5565c-154">Данные и представления, представленные в этом документе, такие как URL-адреса и другие ссылки на веб-сайты, могут измениться без предварительного уведомления.</span><span class="sxs-lookup"><span data-stu-id="5565c-154">Information and views expressed in this document, such as URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="5565c-155">Вы несете ответственность за ее использование.</span><span class="sxs-lookup"><span data-stu-id="5565c-155">You bear the risk of using it.</span></span>

<span data-ttu-id="5565c-156">Некоторые примеры, представленные в этом документе, предназначены только для иллюстрации и являются вымышленными.</span><span class="sxs-lookup"><span data-stu-id="5565c-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="5565c-157">Фактическая ассоциация или соединение не предназначены для использования или должны выводиться.</span><span class="sxs-lookup"><span data-stu-id="5565c-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="5565c-158">Настоящий документ не предоставляет никаких законных прав на интеллектуальную собственность в любом продукте Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="5565c-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="5565c-159">Вы можете копировать и использовать настоящий документ для внутреннего использования и в справочных целях.</span><span class="sxs-lookup"><span data-stu-id="5565c-159">You may copy and use this document for your internal, reference purposes.</span></span> <span data-ttu-id="5565c-160">Вы можете изменить этот документ для внутренних целей и ссылок.</span><span class="sxs-lookup"><span data-stu-id="5565c-160">You may modify this document for your internal, reference purposes.</span></span>



<span data-ttu-id="5565c-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server и Windows Vista — охраняемые товарные знаки в группе компании Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5565c-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="5565c-162">Все прочие товарные знаки являются собственностью соответствующих владельцев.</span><span class="sxs-lookup"><span data-stu-id="5565c-162">All other trademarks are property of their respective owners.</span></span>

 

 





