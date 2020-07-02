---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795968"
---
# <span data-ttu-id="6a108-103">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="6a108-103">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>

>[!NOTE]
><span data-ttu-id="6a108-104">Эта документация является версией UE-V, которая входит в состав пакета оптимизации рабочего стола (MDOP) (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="6a108-104">This documentation is a for version of UE-V that was included in the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="6a108-105">Сведения о последней версии UE-V, которая входит в состав Windows 10 Enterprise, приведены в разделе [Начало работы с UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span><span class="sxs-lookup"><span data-stu-id="6a108-105">For information about the latest version of UE-V which is included in Windows 10 Enterprise, see [Get Started with UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).</span></span>


<span data-ttu-id="6a108-106">Соблюдайте и разработайте параметры приложения и ОС Windows, выполнив виртуализацию Microsoft User Experience (UE-V) 2,0 или 2,1.</span><span class="sxs-lookup"><span data-stu-id="6a108-106">Capture and centralize your users’ application settings and Windows OS settings by implementing Microsoft User Experience Virtualization (UE-V) 2.0 or 2.1.</span></span> <span data-ttu-id="6a108-107">Затем примените эти параметры к устройствам, которые пользователи получают доступ к вашим организациям, таким как настольные компьютеры, Ноутбуки и сеансы инфраструктуры виртуальных рабочих столов (VDI).</span><span class="sxs-lookup"><span data-stu-id="6a108-107">Then, apply these settings to the devices users access in your enterprise, like desktop computers, laptops, or virtual desktop infrastructure (VDI) sessions.</span></span>

**<span data-ttu-id="6a108-108">С UE-V вы можете...</span><span class="sxs-lookup"><span data-stu-id="6a108-108">With UE-V you can…</span></span>**

-   <span data-ttu-id="6a108-109">Укажите, какие параметры приложения и рабочего стола следует синхронизировать</span><span class="sxs-lookup"><span data-stu-id="6a108-109">Specify which application and desktop settings synchronize</span></span>

-   <span data-ttu-id="6a108-110">доставлять параметры в любое время, где бы на территории организации не работал пользователь;</span><span class="sxs-lookup"><span data-stu-id="6a108-110">Deliver the settings anytime and anywhere users work throughout the enterprise</span></span>

-   <span data-ttu-id="6a108-111">создавать пользовательские шаблоны для сторонних приложений или бизнес-приложений;</span><span class="sxs-lookup"><span data-stu-id="6a108-111">Create custom templates for your third-party or line-of-business applications</span></span>

-   <span data-ttu-id="6a108-112">Восстановление параметров после замены оборудования или обновления или после reimaging виртуальной машины в исходное состояние</span><span class="sxs-lookup"><span data-stu-id="6a108-112">Recover settings after hardware replacement or upgrade, or after reimaging a virtual machine to its initial state</span></span>

## <span data-ttu-id="6a108-113">Компоненты UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6a108-113">Components of UE-V 2.x</span></span>


<span data-ttu-id="6a108-114">На этой схеме показано, как совместно развернутые компоненты UE-V работают вместе для синхронизации параметров.</span><span class="sxs-lookup"><span data-stu-id="6a108-114">This diagram shows how deployed UE-V components work together to synchronize settings.</span></span>

![Архитектурная схема uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a108-116">Компонент</span><span class="sxs-lookup"><span data-stu-id="6a108-116">Component</span></span></th>
<th align="left"><span data-ttu-id="6a108-117">Функция</span><span class="sxs-lookup"><span data-stu-id="6a108-117">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a108-118">Агент UE-V</span><span class="sxs-lookup"><span data-stu-id="6a108-118">UE-V Agent</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-119">Установлен на всех компьютерах, которые должны синхронизировать параметры, <strong> Агент UE-V Agent </strong> отслеживает зарегистрированные приложения и операционную систему на предмет изменений параметров, а затем синхронизирует эти параметры между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="6a108-119">Installed on every computer that needs to synchronize settings, the <strong>UE-V Agent</strong> monitors registered applications and the operating system for any settings changes, then synchronizes those settings between computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a108-120">Пакеты параметров</span><span class="sxs-lookup"><span data-stu-id="6a108-120">Settings packages</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-121">Параметры приложения и параметры Windows хранятся в <strong> пакетах параметров, </strong> созданных агентом UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="6a108-121">Application settings and Windows settings are stored in <strong>settings packages</strong> created by the UE-V Agent.</span></span> <span data-ttu-id="6a108-122">Параметры пакетов формируются, сохраняются локально и копируются в место хранения параметров.</span><span class="sxs-lookup"><span data-stu-id="6a108-122">Settings packages are built, locally stored, and copied to the settings storage location.</span></span></p>
<ul>
<li><p><span data-ttu-id="6a108-123">Значения параметров для <strong> классических приложений </strong> сохраняются, когда пользователь закрывает приложение.</span><span class="sxs-lookup"><span data-stu-id="6a108-123">The setting values for <strong>desktop applications</strong> are stored when the user closes the application.</span></span></p></li>
<li><p><span data-ttu-id="6a108-124">Значения <strong> параметров Windows </strong> сохраняются при выходе пользователя из системы, при блокировке компьютера или при удаленном отключении от компьютера.</span><span class="sxs-lookup"><span data-stu-id="6a108-124">Values for <strong>Windows settings</strong> are stored when the user logs off, when the computer is locked, or when the user disconnects remotely from a computer.</span></span></p></li>
</ul>
<p><span data-ttu-id="6a108-125">Поставщик синхронизации определяет, когда параметры приложения или операционной системы считываются из <strong> пакетов параметров </strong> и синхронизируются.</span><span class="sxs-lookup"><span data-stu-id="6a108-125">The sync provider determines when the application or operating system settings are read from the <strong>Settings Packages</strong> and synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a108-126">Место хранения параметров</span><span class="sxs-lookup"><span data-stu-id="6a108-126">Settings storage location</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-127">Это стандартная сетевая демонстрация, к которой пользователи могут получить доступ.</span><span class="sxs-lookup"><span data-stu-id="6a108-127">This is a standard network share that your users can access.</span></span> <span data-ttu-id="6a108-128">Агент UE-V проверяет расположение и создает скрытую системную папку, в которой хранятся и извлекаются параметры пользователей.</span><span class="sxs-lookup"><span data-stu-id="6a108-128">The UE-V Agent verifies the location and creates a hidden system folder in which to store and retrieve user settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a108-129">Шаблоны расположений параметров</span><span class="sxs-lookup"><span data-stu-id="6a108-129">Settings location templates</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-130">UE-V использует XML-файлы в качестве шаблонов расположения параметров для отслеживания и синхронизации параметров классических приложений и рабочего стола Windows между компьютерами пользователя.</span><span class="sxs-lookup"><span data-stu-id="6a108-130">UE-V uses XML files as settings location templates to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="6a108-131">По умолчанию некоторые шаблоны расположений параметров включены в UE-V.</span><span class="sxs-lookup"><span data-stu-id="6a108-131">By default, some settings location templates are included in UE-V .</span></span> <span data-ttu-id="6a108-132">Вы также можете создавать, изменять и проверять шаблоны расположений настраиваемых параметров, <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> управляя синхронизацией параметров для настраиваемых приложений </a> .</span><span class="sxs-lookup"><span data-stu-id="6a108-132">You can also create, edit, or validate custom settings location templates by <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)">managing settings synchronization for custom applications</a>.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6a108-133">Примечание.</span><span class="sxs-lookup"><span data-stu-id="6a108-133">Note</span></span></strong><br/><p><span data-ttu-id="6a108-134">Шаблоны расположений параметров не требуются для приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="6a108-134">Settings location templates are not required for Windows apps.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a108-135">Список приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="6a108-135">Windows app list</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-136">Параметры приложений для Windows записываются и применяются динамически.</span><span class="sxs-lookup"><span data-stu-id="6a108-136">Settings for Windows apps are captured and applied dynamically.</span></span> <span data-ttu-id="6a108-137">Разработчик приложений определяет параметры, которые синхронизируются для каждого приложения.</span><span class="sxs-lookup"><span data-stu-id="6a108-137">The app developer specifies the settings that are synchronized for each app.</span></span> <span data-ttu-id="6a108-138">UE-V определяет, какие приложения для Windows включены для синхронизации параметров с помощью управляемого списка приложений.</span><span class="sxs-lookup"><span data-stu-id="6a108-138">UE-V determines which Windows apps are enabled for settings synchronization using a managed list of apps.</span></span> <span data-ttu-id="6a108-139">По умолчанию этот список содержит большинство приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="6a108-139">By default, this list includes most Windows apps.</span></span></p>
<p><span data-ttu-id="6a108-140">Вы можете добавлять и удалять приложения в списке приложений для Windows, выполнив указанные <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> ниже действия </a> .</span><span class="sxs-lookup"><span data-stu-id="6a108-140">You can add or remove applications in the Windows app list by following the procedures shown <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)">here</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a><span data-ttu-id="6a108-141">Управление синхронизацией параметров для настраиваемых приложений</span><span class="sxs-lookup"><span data-stu-id="6a108-141">Managing Settings Synchronization for Custom Applications</span></span>

<span data-ttu-id="6a108-142">Используйте эти компоненты UE-V для создания и управления пользовательскими шаблонами для бизнес-приложений сторонних разработчиков.</span><span class="sxs-lookup"><span data-stu-id="6a108-142">Use these UE-V components to create and manage custom templates for your third-party or line-of-business applications.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6a108-143">Генератор UE-V</span><span class="sxs-lookup"><span data-stu-id="6a108-143">UE-V Generator</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-144">Используйте <strong> генератор UE-V </strong> для создания настраиваемых шаблонов расположений параметров, которые затем можно распространять на компьютеры пользователей.</span><span class="sxs-lookup"><span data-stu-id="6a108-144">Use the <strong>UE-V Generator</strong> to create custom settings location templates that you can then distribute to user computers.</span></span> <span data-ttu-id="6a108-145">Генератор UE-V также позволяет редактировать существующий шаблон или проверять шаблон, созданный с помощью другого редактора XML.</span><span class="sxs-lookup"><span data-stu-id="6a108-145">The UE-V Generator also lets you edit an existing template or validate a template that was created by using another XML editor.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6a108-146">Каталог шаблонов параметров</span><span class="sxs-lookup"><span data-stu-id="6a108-146">Settings template catalog</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6a108-147"><strong>Каталог шаблонов параметров </strong> — это путь к папке на компьютерах UE-V или сетевая папка SMB, в которой хранятся пользовательские шаблоны расположения параметров.</span><span class="sxs-lookup"><span data-stu-id="6a108-147">The <strong>settings template catalog</strong> is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores the custom settings location templates.</span></span> <span data-ttu-id="6a108-148">Агент UE-V проверяет это расположение один раз в день, извлекает новые или обновленные шаблоны и обновляет поведение синхронизации.</span><span class="sxs-lookup"><span data-stu-id="6a108-148">The UE-V Agent checks this location once a day, retrieves new or updated templates, and updates its synchronization behavior.</span></span></p>
<p><span data-ttu-id="6a108-149">Если используются только шаблоны расположений параметров по умолчанию UE-V, каталог шаблонов параметров не нужен.</span><span class="sxs-lookup"><span data-stu-id="6a108-149">If you use only the UE-V default settings location templates, then a settings template catalog is unnecessary.</span></span> <span data-ttu-id="6a108-150">Дополнительные сведения о каталогах развертывания параметров можно найти <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> в разделе Настройка каталога шаблонов параметров ue-V </a> .</span><span class="sxs-lookup"><span data-stu-id="6a108-150">For more information about settings deployment catalogs, see <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)">Configure a UE-V settings template catalog</a>.</span></span></p></td>
</tr>
</tbody>
</table>



![процесс генератора UE-v](images/ue-vgeneratorprocess.gif)

## <span data-ttu-id="6a108-152">Параметры, синхронизированные по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6a108-152">Settings Synchronized by Default</span></span>


<span data-ttu-id="6a108-153">UE-V синхронизирует параметры для этих приложений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a108-153">UE-V synchronizes settings for these applications by default.</span></span> <span data-ttu-id="6a108-154">Полный список и более подробные сведения можно найти в разделе [Параметры, которые автоматически синхронизируются в развертывании UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="6a108-154">For a complete list and more detailed information, see [Settings that are automatically synchronized in a UE-V deployment](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span>

<span data-ttu-id="6a108-155">Приложения Microsoft Office 2013 (UE-V 2,1 SP1 и 2,1)</span><span class="sxs-lookup"><span data-stu-id="6a108-155">Microsoft Office 2013 applications (UE-V 2.1 SP1 and 2.1)</span></span>

<span data-ttu-id="6a108-156">Приложения Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 и 2,0)</span><span class="sxs-lookup"><span data-stu-id="6a108-156">Microsoft Office 2010 applications (UE-V 2.1 SP1, 2.1, and 2.0)</span></span>

<span data-ttu-id="6a108-157">Приложения Microsoft Office 2007 (только для UE-V 2,0)</span><span class="sxs-lookup"><span data-stu-id="6a108-157">Microsoft Office 2007 applications (UE-V 2.0 only)</span></span>

<span data-ttu-id="6a108-158">Internet Explorer 8, 9 и 10</span><span class="sxs-lookup"><span data-stu-id="6a108-158">Internet Explorer 8, 9, and 10</span></span>

<span data-ttu-id="6a108-159">Internet Explorer 11 в UE-V 2,1 с пакетом обновления 1 (SP1) и 2,1</span><span class="sxs-lookup"><span data-stu-id="6a108-159">Internet Explorer 11 in UE-V 2.1 SP1 and 2.1</span></span>

<span data-ttu-id="6a108-160">Многие приложения для Windows, например Xbox</span><span class="sxs-lookup"><span data-stu-id="6a108-160">Many Windows applications, such as Xbox</span></span>

<span data-ttu-id="6a108-161">Многие приложения для Windows для настольных систем, например Блокнот</span><span class="sxs-lookup"><span data-stu-id="6a108-161">Many Windows desktop applications, such as Notepad</span></span>

<span data-ttu-id="6a108-162">Многие параметры Windows, например фоновый рисунок рабочего стола или фоновый рисунок</span><span class="sxs-lookup"><span data-stu-id="6a108-162">Many Windows settings, such as desktop background or wallpaper</span></span>

**<span data-ttu-id="6a108-163">Примечание.</span><span class="sxs-lookup"><span data-stu-id="6a108-163">Note</span></span>**  
<span data-ttu-id="6a108-164">Вы также можете [настроить UE-V для синхронизации параметров](https://technet.microsoft.com/library/dn458942.aspx) для других приложений, кроме тех, которые синхронизированы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6a108-164">You can also [customize UE-V to synchronize settings](https://technet.microsoft.com/library/dn458942.aspx) for applications other than those synchronized by default.</span></span>



## <span data-ttu-id="6a108-165">Сравнение UE-V с другими продуктами Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6a108-165">Compare UE-V to other Microsoft products</span></span>


<span data-ttu-id="6a108-166">Используйте эту таблицу для сравнения UE-V и синхронизации профилей в Windows 7, синхронизации профилей в Windows 8 и компонента "Синхронизация параметров компьютера" учетной записи Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="6a108-166">Use this table to compare UE-V to Synchronize Profiles in Windows 7, Synchronize Profiles in Windows 8, and the Sync PC Settings feature of Microsoft account.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6a108-167">Функция</span><span class="sxs-lookup"><span data-stu-id="6a108-167">Feature</span></span></th>
<th align="left"><span data-ttu-id="6a108-168">Синхронизация профилей с помощью Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a108-168">Synchronize Profiles using Windows 7</span></span></th>
<th align="left"><span data-ttu-id="6a108-169">Синхронизация профилей в Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a108-169">Synchronize Profiles using Windows 8</span></span></th>
<th align="left"><span data-ttu-id="6a108-170">Синхронизация профилей с помощью Windows 10</span><span class="sxs-lookup"><span data-stu-id="6a108-170">Synchronize Profiles using Windows 10</span></span></th>
<th align="left"><span data-ttu-id="6a108-171">Учетная запись Майкрософт</span><span class="sxs-lookup"><span data-stu-id="6a108-171">Microsoft account</span></span></th>
<th align="left"><span data-ttu-id="6a108-172">UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="6a108-172">UE-V 2.0</span></span></th>
<th align="left"><span data-ttu-id="6a108-173">UE-V 2,1 и 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="6a108-173">UE-V 2.1 and 2.1 SP1</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a108-174">Синхронизация параметров на нескольких компьютерах</span><span class="sxs-lookup"><span data-stu-id="6a108-174">Synchronize settings between multiple computers</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-175">●</span><span class="sxs-lookup"><span data-stu-id="6a108-175">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-176">●</span><span class="sxs-lookup"><span data-stu-id="6a108-176">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-177">●</span><span class="sxs-lookup"><span data-stu-id="6a108-177">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-178">●</span><span class="sxs-lookup"><span data-stu-id="6a108-178">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-179">●</span><span class="sxs-lookup"><span data-stu-id="6a108-179">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-180">●</span><span class="sxs-lookup"><span data-stu-id="6a108-180">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a108-181">Синхронизация параметров между физическими и виртуальными приложениями</span><span class="sxs-lookup"><span data-stu-id="6a108-181">Synchronize settings between physical and virtual apps</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-182">●</span><span class="sxs-lookup"><span data-stu-id="6a108-182">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-183">●</span><span class="sxs-lookup"><span data-stu-id="6a108-183">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a108-184">Синхронизация параметров приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="6a108-184">Synchronize Windows app settings</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-185">●</span><span class="sxs-lookup"><span data-stu-id="6a108-185">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-186">●</span><span class="sxs-lookup"><span data-stu-id="6a108-186">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-187">●</span><span class="sxs-lookup"><span data-stu-id="6a108-187">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a108-188">Управление через WMI</span><span class="sxs-lookup"><span data-stu-id="6a108-188">Manage via WMI</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-189">●</span><span class="sxs-lookup"><span data-stu-id="6a108-189">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-190">●</span><span class="sxs-lookup"><span data-stu-id="6a108-190">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-191">●</span><span class="sxs-lookup"><span data-stu-id="6a108-191">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-192">●</span><span class="sxs-lookup"><span data-stu-id="6a108-192">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a108-193">Регулярно синхронизировать изменения параметров</span><span class="sxs-lookup"><span data-stu-id="6a108-193">Synchronize settings changes on a regular basis</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-194">●</span><span class="sxs-lookup"><span data-stu-id="6a108-194">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-195">●</span><span class="sxs-lookup"><span data-stu-id="6a108-195">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-196">●</span><span class="sxs-lookup"><span data-stu-id="6a108-196">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a108-197">Минимальная конфигурация для настройки</span><span class="sxs-lookup"><span data-stu-id="6a108-197">Minimal configuration for Setup</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-198">●</span><span class="sxs-lookup"><span data-stu-id="6a108-198">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-199">●</span><span class="sxs-lookup"><span data-stu-id="6a108-199">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-200">●</span><span class="sxs-lookup"><span data-stu-id="6a108-200">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-201">●</span><span class="sxs-lookup"><span data-stu-id="6a108-201">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-202">●</span><span class="sxs-lookup"><span data-stu-id="6a108-202">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-203">●</span><span class="sxs-lookup"><span data-stu-id="6a108-203">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a108-204">Поддерживается на компьютерах, не подключенных к домену</span><span class="sxs-lookup"><span data-stu-id="6a108-204">Supported on non-domain joined computers</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-205">●</span><span class="sxs-lookup"><span data-stu-id="6a108-205">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a108-206">Поддержка атрибута основного компьютера (Active Directory)</span><span class="sxs-lookup"><span data-stu-id="6a108-206">Supports Primary Computer Active Directory attribute</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-207">●</span><span class="sxs-lookup"><span data-stu-id="6a108-207">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-208">●</span><span class="sxs-lookup"><span data-stu-id="6a108-208">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a108-209">Синхронизация параметров между инфраструктурой виртуальных рабочих столов (VDI)/Remote Desktop Services (RDS) и богатыми рабочими столами</span><span class="sxs-lookup"><span data-stu-id="6a108-209">Synchronizes settings between virtual desktop infrastructure (VDI)/Remote Desktop Services (RDS) and rich desktops</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-210">●</span><span class="sxs-lookup"><span data-stu-id="6a108-210">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-211">●</span><span class="sxs-lookup"><span data-stu-id="6a108-211">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a108-212">Неограниченный объем хранилища</span><span class="sxs-lookup"><span data-stu-id="6a108-212">Unlimited setting storage space</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-213">●</span><span class="sxs-lookup"><span data-stu-id="6a108-213">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-214">●</span><span class="sxs-lookup"><span data-stu-id="6a108-214">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-215">●</span><span class="sxs-lookup"><span data-stu-id="6a108-215">●</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-216">●</span><span class="sxs-lookup"><span data-stu-id="6a108-216">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-217">●</span><span class="sxs-lookup"><span data-stu-id="6a108-217">●</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6a108-218">Выбор параметров приложения для синхронизации</span><span class="sxs-lookup"><span data-stu-id="6a108-218">Choice in which app settings to synchronize</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-219">●</span><span class="sxs-lookup"><span data-stu-id="6a108-219">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-220">●</span><span class="sxs-lookup"><span data-stu-id="6a108-220">●</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6a108-221">Резервное копирование и восстановление для ИТ-специалистов</span><span class="sxs-lookup"><span data-stu-id="6a108-221">Backup/Restore for IT Pro</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="6a108-222">●</span><span class="sxs-lookup"><span data-stu-id="6a108-222">●</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-223">Частично</span><span class="sxs-lookup"><span data-stu-id="6a108-223">Partial</span></span></p></td>
<td align="left"><p><span data-ttu-id="6a108-224">●</span><span class="sxs-lookup"><span data-stu-id="6a108-224">●</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6a108-225">Заметки о выпуске UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6a108-225">UE-V 2.x Release Notes</span></span>


<span data-ttu-id="6a108-226">Дополнительные сведения и последние новости, которые не были внесены в документацию, приведены в статье</span><span class="sxs-lookup"><span data-stu-id="6a108-226">For more information, and for late-breaking news that did not make it into the documentation, see</span></span>

-   [<span data-ttu-id="6a108-227">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="6a108-227">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [<span data-ttu-id="6a108-228">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="6a108-228">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [<span data-ttu-id="6a108-229">Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="6a108-229">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <span data-ttu-id="6a108-230">Другие ресурсы для этого продукта</span><span class="sxs-lookup"><span data-stu-id="6a108-230">Other resources for this product</span></span>


-   [<span data-ttu-id="6a108-231">Начало работы с UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="6a108-231">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="6a108-232">Подготовка к развертыванию UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6a108-232">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="6a108-233">Администрирование UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6a108-233">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="6a108-234">Устранение неполадок UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6a108-234">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="6a108-235">Технический справочник по UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="6a108-235">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)

### <span data-ttu-id="6a108-236">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="6a108-236">More information</span></span>

<a href="" id="mdop-techcenter-page"></a><span data-ttu-id="6a108-237">[Страница TechCenter для MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Узнайте о последних сведениях и ресурсах для MDOP.</span><span class="sxs-lookup"><span data-stu-id="6a108-237">[MDOP TechCenter Page](https://go.microsoft.com/fwlink/p/?LinkId=225286) Learn about the latest MDOP information and resources.</span></span>

<a href="" id="mdop-information-experience"></a><span data-ttu-id="6a108-238">[Информационные функции для MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Ознакомьтесь с документацией, видеороликами и прочими материалами, посвященными технологиям MDOP.</span><span class="sxs-lookup"><span data-stu-id="6a108-238">[MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) Find documentation, videos, and other resources for MDOP technologies.</span></span> <span data-ttu-id="6a108-239">Вы также можете [отправить нам отзыв](mailto:MDOPDocs@microsoft.com) и узнать об обновлениях, перейдя в [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) или [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="6a108-239">You can also [send us feedback](mailto:MDOPDocs@microsoft.com) or learn about updates by following us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>














