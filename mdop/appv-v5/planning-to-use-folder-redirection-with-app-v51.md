---
title: Планирование использования перенаправления папок с App-V
description: Планирование использования перенаправления папок с App-V
author: dansimp
ms.assetid: 6bea9a8f-a915-4d7d-be67-ef1cca1398ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 507aef186579da0efdb3af7b6e1088a5e725ad70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813384"
---
# <span data-ttu-id="a3017-103">Планирование использования перенаправления папок с App-V</span><span class="sxs-lookup"><span data-stu-id="a3017-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="a3017-104">Microsoft Application Virtualization (App-V) 5,1 поддерживает использование функции перенаправления папок, позволяющей пользователям и администраторам перенаправлять путь к папке в новое расположение.</span><span class="sxs-lookup"><span data-stu-id="a3017-104">Microsoft Application Virtualization (App-V) 5.1 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="a3017-105">Этот раздел включает в себя следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="a3017-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="a3017-106">Требования для использования перенаправления папок</span><span class="sxs-lookup"><span data-stu-id="a3017-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="a3017-107">Настройка перенаправления папок для использования с App-V</span><span class="sxs-lookup"><span data-stu-id="a3017-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="a3017-108">Как работает перенаправление папок в App-V</span><span class="sxs-lookup"><span data-stu-id="a3017-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="a3017-109">Общие сведения о перенаправлении папок</span><span class="sxs-lookup"><span data-stu-id="a3017-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="a3017-110">Требования и неподдерживаемые сценарии использования перенаправления папок</span><span class="sxs-lookup"><span data-stu-id="a3017-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3017-111">Требования</span><span class="sxs-lookup"><span data-stu-id="a3017-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-112">Чтобы использовать перенаправление папок% AppData%, необходимо выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a3017-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="a3017-113">У вас есть пакет App-V с папкой виртуальной файловой системы AppData (VFS).</span><span class="sxs-lookup"><span data-stu-id="a3017-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="a3017-114">Включить перенаправление папок и перенаправить папки пользователей в общую папку (обычно это сетевая папка).</span><span class="sxs-lookup"><span data-stu-id="a3017-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="a3017-115">Перемещайте оба или ни один из указанных ниже вариантов.</span><span class="sxs-lookup"><span data-stu-id="a3017-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="a3017-116">Файлы в разделе%appdata%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="a3017-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="a3017-117">Параметры реестра в разделе HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</span><span class="sxs-lookup"><span data-stu-id="a3017-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="a3017-118">Более подробную информацию можно найти в разделе <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> Публикация приложений и взаимодействие с клиентами </a> .</span><span class="sxs-lookup"><span data-stu-id="a3017-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="a3017-119">Убедитесь, что следующие папки доступны каждому пользователю, который входит в систему на компьютере, на котором запущен клиент App-V 5,0 SP2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="a3017-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="a3017-120">% AppData% настроено на нужное сетевое расположение (с <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> поддержкой автономных файлов или без нее </a> ).</span><span class="sxs-lookup"><span data-stu-id="a3017-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="a3017-121">% LocalAppData% настроен на нужную локальную папку.</span><span class="sxs-lookup"><span data-stu-id="a3017-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3017-122">Неподдерживаемые сценарии</span><span class="sxs-lookup"><span data-stu-id="a3017-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="a3017-123">Настройка% LocalAppData% в качестве сетевого диска.</span><span class="sxs-lookup"><span data-stu-id="a3017-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="a3017-124">Перенаправление меню "Пуск" в одну папку для нескольких пользователей.</span><span class="sxs-lookup"><span data-stu-id="a3017-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="a3017-125">Если перемещаемая папка AppData (% AppData%) перенаправляется на недоступную сетевую ошибку, приложения App-V не будут запускаться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a3017-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a3017-126">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="a3017-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="a3017-127">Описание сценария</span><span class="sxs-lookup"><span data-stu-id="a3017-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3017-128">В App-V 5,0 с помощью App-V 5,0 SP2 и исправлений</span><span class="sxs-lookup"><span data-stu-id="a3017-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-129">Этот сбой будет происходить независимо от того, включены ли автономные файлы.</span><span class="sxs-lookup"><span data-stu-id="a3017-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3017-130">В App-V 5,0 SP3 и более поздних версиях</span><span class="sxs-lookup"><span data-stu-id="a3017-130">In App-V 5.0 SP3 and later</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-131">Если для автономных файлов отключена доступная сетевая доступная, приложение App-V запустится успешно.</span><span class="sxs-lookup"><span data-stu-id="a3017-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="a3017-132">Настройка перенаправления папок для использования с App-V</span><span class="sxs-lookup"><span data-stu-id="a3017-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="a3017-133">Перенаправление папок можно применять к различным папкам, таким как "Рабочий стол", "Мои документы", "Мои рисунки" и т. д. Тем не менее, единственная папка, влияющая на использование приложений App-V, — это папка для перемещаемой AppData пользователя (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="a3017-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="a3017-134">Перенаправление папок можно применить ко всем другим поддерживаемым папкам, не влияя на App-V.</span><span class="sxs-lookup"><span data-stu-id="a3017-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="a3017-135">Как работает перенаправление папок в App-V</span><span class="sxs-lookup"><span data-stu-id="a3017-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="a3017-136">В приведенной ниже таблице показано, как работает перенаправление папок, когда пользователь% AppData% перенаправляется в сеть и после того, как вы удовлетворены требованиями, описанными выше в этой статье.</span><span class="sxs-lookup"><span data-stu-id="a3017-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a3017-137">Состояние виртуальной среды</span><span class="sxs-lookup"><span data-stu-id="a3017-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="a3017-138">Выполняемое действие</span><span class="sxs-lookup"><span data-stu-id="a3017-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3017-139">При запуске виртуальной среды</span><span class="sxs-lookup"><span data-stu-id="a3017-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-140">Папка AppData виртуальной файловой системы (VFS) сопоставлена с локальной папкой AppData (% LocalAppData%) вместо ссылки на перемещаемую папку AppData пользователя (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="a3017-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="a3017-141">LocalAppData включает локальный кэш папки с перемещаемой AppData пользователя для используемого пакета.</span><span class="sxs-lookup"><span data-stu-id="a3017-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="a3017-142">Локальный кэш находится в разделе:</span><span class="sxs-lookup"><span data-stu-id="a3017-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="a3017-143">Последние данные из папки перемещаемой оснастки пользователя копируются в и заменяют данные в локальном кэше.</span><span class="sxs-lookup"><span data-stu-id="a3017-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="a3017-144">При запуске виртуальной среды данные сохраняются в локальном кэше.</span><span class="sxs-lookup"><span data-stu-id="a3017-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="a3017-145">Данные выдаются только из% LocalAppData% и не перемещаются или синхронизируются с помощью% AppData%, пока конечный пользователь не завершит работу компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3017-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="a3017-146">Элементы в папку AppData выполняются с помощью контекста пользователя, а не контекста системы.</span><span class="sxs-lookup"><span data-stu-id="a3017-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="a3017-147">Примечание.</span><span class="sxs-lookup"><span data-stu-id="a3017-147">Note</span></span></strong><br/><p><span data-ttu-id="a3017-148">Иногда перенаправление папки клиента App-V не может переносить файлы из% AppData% в% LocalAppData%.</span><span class="sxs-lookup"><span data-stu-id="a3017-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="a3017-149">Ознакомьтесь <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> с заметками о выпуске для App-V 5,0 SP2 </a> .</span><span class="sxs-lookup"><span data-stu-id="a3017-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3017-150">При завершении работы виртуальной среды</span><span class="sxs-lookup"><span data-stu-id="a3017-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-151">Локальные кэшированные данные в AppData (роуминге) заархивированы и скопированы в папку "Real" перемещаемой папки AppData в% AppData%.</span><span class="sxs-lookup"><span data-stu-id="a3017-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="a3017-152">Метка времени, указывающая на последнюю известную отправку, одновременно сохраняется как раздел реестра в разделе:</span><span class="sxs-lookup"><span data-stu-id="a3017-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="a3017-153">Для обеспечения избыточности приложение App-V хранит три последние копии сжатых данных в разделе% AppData%.</span><span class="sxs-lookup"><span data-stu-id="a3017-153">To provide redundancy, App-V keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="a3017-154">Общие сведения о перенаправлении папок</span><span class="sxs-lookup"><span data-stu-id="a3017-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3017-155">Описание</span><span class="sxs-lookup"><span data-stu-id="a3017-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-156">Позволяет конечным пользователям работать с файлами, которые были перенаправлены в другую папку, как если бы они находились на локальном диске.</span><span class="sxs-lookup"><span data-stu-id="a3017-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3017-157">Описание</span><span class="sxs-lookup"><span data-stu-id="a3017-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-158">Перенаправление папок позволяет пользователям и администраторам перенаправлять путь к папке в сетевое расположение.</span><span class="sxs-lookup"><span data-stu-id="a3017-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="a3017-159">Документы в папке доступны для пользователя на любом компьютере в сети.</span><span class="sxs-lookup"><span data-stu-id="a3017-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="a3017-160">Перенаправление папок позволяет пользователям и администраторам перенаправлять путь к папке в сетевое расположение.</span><span class="sxs-lookup"><span data-stu-id="a3017-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="a3017-161">Документы в папке доступны для пользователя на любом компьютере в сети.</span><span class="sxs-lookup"><span data-stu-id="a3017-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="a3017-162">Новое расположение может представлять собой папку на локальном компьютере или в общей сетевой папке.</span><span class="sxs-lookup"><span data-stu-id="a3017-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="a3017-163">Перенаправление папок немедленно обновляет файлы, а перемещаемые данные обычно синхронизируются, когда пользователь входит в систему или выходит из нее.</span><span class="sxs-lookup"><span data-stu-id="a3017-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a3017-164">Пример использования</span><span class="sxs-lookup"><span data-stu-id="a3017-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="a3017-165">Вы можете перенаправить папку "документы", которая обычно хранится на локальном жестком диске компьютера&#39;s, в сетевое расположение.</span><span class="sxs-lookup"><span data-stu-id="a3017-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="a3017-166">Пользователь может получить доступ к документам в папке с любого компьютера в сети.</span><span class="sxs-lookup"><span data-stu-id="a3017-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a3017-167">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a3017-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="a3017-168">Общие сведения о перенаправлении папок</span><span class="sxs-lookup"><span data-stu-id="a3017-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>
















