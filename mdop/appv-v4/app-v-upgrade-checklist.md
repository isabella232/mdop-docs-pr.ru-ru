---
title: Контрольный список обновления App-V
description: Контрольный список обновления App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819739"
---
# <span data-ttu-id="09907-103">Контрольный список обновления App-V</span><span class="sxs-lookup"><span data-stu-id="09907-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="09907-104">Перед обновлением до приложения Microsoft Application Virtualization (App-V) 4,5 или более поздней версии все версии, предшествующие App-V 4,1, должны быть обновлены до App-V 4,1.</span><span class="sxs-lookup"><span data-stu-id="09907-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="09907-105">Прежде чем обновлять серверные компоненты, необходимо предварительно запланировать обновление клиентов.</span><span class="sxs-lookup"><span data-stu-id="09907-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="09907-106">Клиенты App-V, обновленные до App-V 4,5, продолжают работать с серверами App-V, которые еще не были обновлены.</span><span class="sxs-lookup"><span data-stu-id="09907-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="09907-107">Более ранние версии клиента не поддерживаются на серверах, которые были обновлены до версии App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="09907-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09907-108">Шаг</span><span class="sxs-lookup"><span data-stu-id="09907-108">Step</span></span></th>
<th align="left"><span data-ttu-id="09907-109">Справочные материалы</span><span class="sxs-lookup"><span data-stu-id="09907-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-110">Обновите клиенты App-V.</span><span class="sxs-lookup"><span data-stu-id="09907-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="09907-111">Обновление клиента Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="09907-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-112">Обновите серверы и базу данных App-V.</span><span class="sxs-lookup"><span data-stu-id="09907-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="09907-113">Важно.</span><span class="sxs-lookup"><span data-stu-id="09907-113">Important</span></span></strong><br/><p><span data-ttu-id="09907-114">Если у вас больше одного сервера, доступ к базе данных App-V, то во время обновления базы данных все эти серверы должны быть переведены в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="09907-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="09907-115">Вы должны следовать обычным бизнес-рекомендациям по обновлению базы данных, но мы рекомендуем проверить ее на использование резервной копии базы данных на тестовом сервере.</span><span class="sxs-lookup"><span data-stu-id="09907-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="09907-116">Затем необходимо выбрать один из серверов для первого обновления, который обновит схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="09907-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="09907-117">После успешного обновления рабочей базы данных вы можете обновить программное обеспечение App-V на других серверах.</span><span class="sxs-lookup"><span data-stu-id="09907-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="09907-118">Обновление серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="09907-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-119">Обновите веб-службу управления App-V.</span><span class="sxs-lookup"><span data-stu-id="09907-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="09907-120">Это действие применяется только в том случае, если веб-служба управления находится на отдельном сервере, для обновления веб-службы управления требуется запустить программу установщика сервера на отдельном сервере.</span><span class="sxs-lookup"><span data-stu-id="09907-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="09907-121">В противном случае Предыдущая операция обновления сервера будет автоматически обновлять веб-службу управления.</span><span class="sxs-lookup"><span data-stu-id="09907-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="09907-122">Обновление серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="09907-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-123">Обновите консоль управления App-V.</span><span class="sxs-lookup"><span data-stu-id="09907-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="09907-124">Это действие применимо только в том случае, если консоль управления находится на отдельном компьютере, для обновления консоли которого требуется запустить программу установщика сервера на отдельном компьютере.</span><span class="sxs-lookup"><span data-stu-id="09907-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="09907-125">В противном случае предыдущий шаг обновления сервера обновит консоль управления.</span><span class="sxs-lookup"><span data-stu-id="09907-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="09907-126">Обновление серверов и компонентов системы</span><span class="sxs-lookup"><span data-stu-id="09907-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-127">Обновите секвенсор App-V.</span><span class="sxs-lookup"><span data-stu-id="09907-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="09907-128">Обновление программы Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="09907-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="09907-129">Дополнительные вопросы по обновлению</span><span class="sxs-lookup"><span data-stu-id="09907-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="09907-130">Любые виртуальные пакеты приложения, упорядоченные в версии 4,2, не должны повторно использоваться для использования с версией 4,5.</span><span class="sxs-lookup"><span data-stu-id="09907-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="09907-131">Однако рекомендуется обновить виртуальные пакеты до формата Microsoft Application Virtualization 4,5, если вы хотите применить стандартные списки управления доступом (ACL) или создать файл установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="09907-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="09907-132">Это простой процесс, и необходимо, чтобы в приложении App-V 4,5 был открыт и сохранен существующий пакет виртуального приложения.</span><span class="sxs-lookup"><span data-stu-id="09907-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="09907-133">Это можно автоматизировать с помощью интерфейса командной строки App-VSequencer.</span><span class="sxs-lookup"><span data-stu-id="09907-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="09907-134">Дополнительные сведения [можно найти в разделе Создание и обновление виртуальных приложений с помощью секвенсора App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md) .</span><span class="sxs-lookup"><span data-stu-id="09907-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="09907-135">Одной из функций секвенсора 4,5 является возможность создания файлов установщика Windows (MSI) как контрольных точек для обеспечения взаимодействия виртуальных пакетов приложений с помощью электронных средств распространения программного обеспечения (например, Microsoft Endpoint Configuration Manager).</span><span class="sxs-lookup"><span data-stu-id="09907-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="09907-136">Предыдущие файлы установщика Windows, созданные с помощью средства MSI для виртуализации приложений, которые были установлены в клиенте App-V 4,1 или 4,2, которые впоследствии будут обновлены до версии App-V 4,5, продолжают работать, но не могут быть установлены в клиенте App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="09907-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="09907-137">Тем не менее, они не могут быть удалены или обновлены, если они не были обновлены в секвенсоре App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="09907-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="09907-138">Исходный пакет App-V, более ранний, чем 4,5, должен быть открыт в секвенсоре App-V 4,5, а затем сохранен как файл установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="09907-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="09907-139">Примечание.</span><span class="sxs-lookup"><span data-stu-id="09907-139">Note</span></span>**  
    <span data-ttu-id="09907-140">Если клиент App-V 4,2 уже обновлен до App-V 4,5, возможно, вы можете создать сценарий временного решения, чтобы сохранить пакеты версии 4,2 на клиентах версии 4,5 и позволить им управлять ими.</span><span class="sxs-lookup"><span data-stu-id="09907-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="09907-141">Этот сценарий должен скопировать два файла, msvcp71.dll и msvcr71.dll в папку установки App-V и указать следующие значения в разделе реестра: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="09907-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="09907-142">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="09907-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="09907-143">"GlobalDataDirectory" = "C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (доступное для записи глобальное расположение)</span><span class="sxs-lookup"><span data-stu-id="09907-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="09907-144">Файлы установщика Windows, созданные с помощью секвенсора App-V 4,5, выводят сообщение об ошибке "для этого пакета требуется клиент Microsoft Application Virtualization 4,5 или более поздней версии при попытке запустить их в клиенте App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="09907-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="09907-145">Откройте старый пакет с помощью секвенсора App-V 4,5 с пакетом обновления 1 (SP1) или секвенсор App-V 4,6, а затем создайте новый MSI-файл для пакета.</span><span class="sxs-lookup"><span data-stu-id="09907-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="09907-146">Любые созданные и сохраненные отчеты версии 4,2 будут перезаписаны при обновлении сервера до версии 4,5.</span><span class="sxs-lookup"><span data-stu-id="09907-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="09907-147">Если вы хотите сохранить эти отчеты, необходимо сохранить резервную копию файла SftMMC. msc, расположенную в папке консоли управления SoftGrid на сервере, и использовать эту копию для замены нового SftMMC. msc, установленного во время обновления.</span><span class="sxs-lookup"><span data-stu-id="09907-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="09907-148">Дополнительные сведения об обновлении предыдущей версии [можно найти в статье обновление до Microsoft Application Virtualization 4,5 (вопросы и ответы](https://go.microsoft.com/fwlink/?LinkId=120358) ) https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="09907-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="09907-149">Поддержка пакета клиента App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="09907-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="09907-150">Вы можете развертывать пакеты, созданные в предыдущих версиях App-V, в клиентах App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="09907-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="09907-151">Тем не менее, необходимо изменить связанный OSD файл, чтобы он включал соответствующую информацию об операционной системе и архитектуре микросхем.</span><span class="sxs-lookup"><span data-stu-id="09907-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="09907-152">Можно использовать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="09907-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="09907-153">Значение ОС</span><span class="sxs-lookup"><span data-stu-id="09907-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-154">&lt;ЗНАЧЕНИЕ ОС = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-155">&lt;ЗНАЧЕНИЕ ОС = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-156">&lt;ЗНАЧЕНИЕ ОС = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-157">&lt;ЗНАЧЕНИЕ ОС = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-158">&lt;ЗНАЧЕНИЕ ОС = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-159">&lt;ЗНАЧЕНИЕ ОС = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-160">&lt;ЗНАЧЕНИЕ ОС = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-161">&lt;ЗНАЧЕНИЕ ОС = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-162">&lt;ЗНАЧЕНИЕ ОС = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-163">&lt;ЗНАЧЕНИЕ ОС = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-164">&lt;ЗНАЧЕНИЕ ОС = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="09907-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="09907-165">Чтобы запустить созданный 32-разрядный пакет, необходимо последовательное приложение на компьютере с 32-разрядной операционной системой, с установленным приложением Sequencer App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="09907-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="09907-166">После упорядочения приложения в консоли секвенсор щелкните вкладку **развертывание** и укажите нужную архитектуру операционной системы и микросхемы.</span><span class="sxs-lookup"><span data-stu-id="09907-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="09907-167">Важно.</span><span class="sxs-lookup"><span data-stu-id="09907-167">Important</span></span>**  
<span data-ttu-id="09907-168">Приложения, упорядоченные на компьютере под управлением 64-разрядной операционной системы, должны развертываться на компьютерах с 64-разрядной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="09907-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="09907-169">Новые 32-разрядные пакеты, созданные с помощью программы Sequencer App-v 4,6, не выполняются на компьютерах, на которых запущен клиент App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="09907-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="09907-170">Для выполнения новых 64-разрядных пакетов в клиенте App-V 4,6 необходимо последовательное приложение на компьютере с запущенным приложением Sequencer App-V 4,6 и работающей под управлением 64-разрядной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="09907-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="09907-171">После того как приложение будет упорядочено, откройте вкладку " **развертывание** ", а затем укажите нужную архитектуру операционной системы и микросхемы.</span><span class="sxs-lookup"><span data-stu-id="09907-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="09907-172">В следующей таблице перечислены клиентские версии, которые будут запускать пакеты, созданные с использованием различных версий секвенсора.</span><span class="sxs-lookup"><span data-stu-id="09907-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

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
<th align="left"></th>
<th align="left"><span data-ttu-id="09907-173">Упорядочение с помощью секвенсора App-V 4,2</span><span class="sxs-lookup"><span data-stu-id="09907-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="09907-174">Упорядочение с помощью секвенсора App-V 4,5</span><span class="sxs-lookup"><span data-stu-id="09907-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="09907-175">Последовательное использование 32-разрядного приложения Sequencer-V 4,6</span><span class="sxs-lookup"><span data-stu-id="09907-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="09907-176">Последовательное использование 64-разрядного приложения Sequencer-V 4,6</span><span class="sxs-lookup"><span data-stu-id="09907-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-177">клиент 4,2</span><span class="sxs-lookup"><span data-stu-id="09907-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-178">Да</span><span class="sxs-lookup"><span data-stu-id="09907-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-179">Нет</span><span class="sxs-lookup"><span data-stu-id="09907-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-180">Нет</span><span class="sxs-lookup"><span data-stu-id="09907-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-181">Нет</span><span class="sxs-lookup"><span data-stu-id="09907-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-182">клиент 4,5 ¹</span><span class="sxs-lookup"><span data-stu-id="09907-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-183">Да</span><span class="sxs-lookup"><span data-stu-id="09907-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-184">Да</span><span class="sxs-lookup"><span data-stu-id="09907-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-185">Нет</span><span class="sxs-lookup"><span data-stu-id="09907-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-186">Нет</span><span class="sxs-lookup"><span data-stu-id="09907-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="09907-187">клиент 4,6 (32-разр.)</span><span class="sxs-lookup"><span data-stu-id="09907-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-188">Да</span><span class="sxs-lookup"><span data-stu-id="09907-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-189">Да</span><span class="sxs-lookup"><span data-stu-id="09907-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-190">Да</span><span class="sxs-lookup"><span data-stu-id="09907-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-191">Нет</span><span class="sxs-lookup"><span data-stu-id="09907-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="09907-192">клиент 4,6 (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="09907-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-193">Да</span><span class="sxs-lookup"><span data-stu-id="09907-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-194">Да</span><span class="sxs-lookup"><span data-stu-id="09907-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-195">Да</span><span class="sxs-lookup"><span data-stu-id="09907-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="09907-196">Да</span><span class="sxs-lookup"><span data-stu-id="09907-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="09907-197">¹ применимы ко всем версиям клиента App-V 4,5, включая App-V 4,5, App-v 4,5 CU1 и App-V 4,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="09907-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









