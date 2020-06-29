---
title: Планирование миграции с предыдущих версий
description: Планирование миграции с предыдущих версий
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815929"
---
# <span data-ttu-id="6928e-103">Планирование миграции с предыдущих версий</span><span class="sxs-lookup"><span data-stu-id="6928e-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="6928e-104">Перед переходом на Microsoft Application Virtualization 4.5 или более поздней версии все версии 4.1 должны быть обновлены до версии 4.1.</span><span class="sxs-lookup"><span data-stu-id="6928e-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="6928e-105">Прежде чем обновлять серверные компоненты, необходимо предварительно запланировать обновление ваших клиентов.</span><span class="sxs-lookup"><span data-stu-id="6928e-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="6928e-106">Клиенты, которые были обновлены до версии 4.5, продолжат работу с серверами Application Virtualization, которые еще не были обновлены.</span><span class="sxs-lookup"><span data-stu-id="6928e-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="6928e-107">Более ранние версии клиента не поддерживаются на серверах, которые были обновлены до версии 4.5.</span><span class="sxs-lookup"><span data-stu-id="6928e-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="6928e-108">Дополнительные сведения об обновлении компонентов системы можно найти в разделе [рекомендации по развертыванию и обновлению Application Virtualization](application-virtualization-deployment-and-upgrade-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="6928e-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="6928e-109">Для обеспечения успешной миграции компоненты системы Application Virtualization следует обновлять в указанном ниже порядке.</span><span class="sxs-lookup"><span data-stu-id="6928e-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="6928e-110">Клиенты Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6928e-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="6928e-111">Пошаговые инструкции по обновлению можно найти в статье [обновление клиента Application Virtualization](how-to-upgrade-the-application-virtualization-client.md).</span><span class="sxs-lookup"><span data-stu-id="6928e-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="6928e-112">Серверы и база данных Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="6928e-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="6928e-113">Пошаговые инструкции по обновлению можно найти в статье [как обновить серверы и компоненты системы](how-to-upgrade-the-servers-and-system-components.md).</span><span class="sxs-lookup"><span data-stu-id="6928e-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="6928e-114">**Примечание**  Если к базе данных Application Virtualization подключено больше одного сервера, то во время обновления базы данных все эти серверы должны быть переведены в автономный режим.</span><span class="sxs-lookup"><span data-stu-id="6928e-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="6928e-115">Вы должны следовать обычным бизнес-рекомендациям по обновлению базы данных, но настоятельно рекомендуется протестировать обновление базы данных с помощью резервной копии базы данных на тестовом сервере.</span><span class="sxs-lookup"><span data-stu-id="6928e-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="6928e-116">Затем необходимо выбрать один из серверов для первого обновления, который обновит схему базы данных.</span><span class="sxs-lookup"><span data-stu-id="6928e-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="6928e-117">После успешного обновления рабочей базы данных вы можете обновить другие серверы.</span><span class="sxs-lookup"><span data-stu-id="6928e-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="6928e-118">Веб-служба управления виртуализацией приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6928e-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="6928e-119">Это действие применимо только в том случае, если веб-служба управления находится на отдельном сервере, для обновления веб-службы которой требуется запустить программу установщика сервера на отдельном сервере.</span><span class="sxs-lookup"><span data-stu-id="6928e-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="6928e-120">В противном случае Предыдущая операция обновления сервера будет автоматически обновлять веб-службу управления.</span><span class="sxs-lookup"><span data-stu-id="6928e-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="6928e-121">Консоль управления виртуализацией приложений Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6928e-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="6928e-122">Это действие применимо только в том случае, если консоль управления находится на отдельном компьютере, для обновления консоли которого требуется запустить программу установщика сервера на отдельном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6928e-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="6928e-123">В противном случае предыдущий шаг обновления сервера обновит консоль управления.</span><span class="sxs-lookup"><span data-stu-id="6928e-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="6928e-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6928e-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="6928e-125">Пошаговые инструкции можно найти [в статье Установка Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="6928e-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="6928e-126">Любые пакеты виртуальных приложений, упорядоченные в версии 4.2, не нужно будет повторно обрабатывать для использования с версией 4.5.</span><span class="sxs-lookup"><span data-stu-id="6928e-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="6928e-127">Однако рекомендуется обновить виртуальные пакеты до формата Microsoft Application Virtualization 4.5, если вы хотите применить стандартные списки управления доступом (ACL) или создать файл установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="6928e-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="6928e-128">Это простой процесс, и необходимо, чтобы только существующий виртуальный пакет приложения был открыт и сохранен с помощью средства Sequencer 4.5.</span><span class="sxs-lookup"><span data-stu-id="6928e-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="6928e-129">Это можно автоматизировать с помощью интерфейса командной строки Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6928e-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="6928e-130">Поддержка клиентского пакета App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="6928e-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="6928e-131">Вы можете развертывать пакеты, созданные в предыдущих версиях App-V для клиентов App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="6928e-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="6928e-132">Тем не менее, необходимо изменить связанный **OSD** файл, чтобы он включал соответствующую информацию об операционной системе и архитектуре микросхем.</span><span class="sxs-lookup"><span data-stu-id="6928e-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="6928e-133">Используйте указанные ниже значения.</span><span class="sxs-lookup"><span data-stu-id="6928e-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6928e-134">Значение ОС</span><span class="sxs-lookup"><span data-stu-id="6928e-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-135">&lt;ЗНАЧЕНИЕ ОС = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-136">&lt;ЗНАЧЕНИЕ ОС = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-137">&lt;ЗНАЧЕНИЕ ОС = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-138">&lt;ЗНАЧЕНИЕ ОС = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-139">&lt;ЗНАЧЕНИЕ ОС = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-140">&lt;ЗНАЧЕНИЕ ОС = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-141">&lt;ЗНАЧЕНИЕ ОС = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-142">&lt;ЗНАЧЕНИЕ ОС = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-143">&lt;ЗНАЧЕНИЕ ОС = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-144">&lt;ЗНАЧЕНИЕ ОС = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-145">&lt;ЗНАЧЕНИЕ ОС = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="6928e-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6928e-146">Чтобы запустить созданный 32-разрядный пакет, необходимо последовательное пошаговое выполнение приложения на компьютере с 32-разрядной операционной системой с установленным секвенсором App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="6928e-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="6928e-147">После упорядочения приложения в консоли секвенсор выберите вкладку **развертывание** и укажите нужную архитектуру операционной системы и микросхемы.</span><span class="sxs-lookup"><span data-stu-id="6928e-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="6928e-148">**Важно!**  Приложения, упорядоченные на компьютере под управлением 64-разрядной операционной системы, должны развертываться на компьютерах с 64-разрядной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="6928e-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="6928e-149">Новые 32-разрядные пакеты, созданные с помощью программы Sequencer App-V 4.6, не будут работать на компьютерах, на которых запущен клиент App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="6928e-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="6928e-150">Для выполнения новых 64-разрядных пакетов в клиенте App-V 4.6 необходимо последовательное приложение на компьютере с Windows App-V 4.6 и работающем с 64-разрядной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="6928e-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="6928e-151">После упорядочения приложения в консоли секвенсор выберите вкладку **развертывание** и укажите нужную архитектуру операционной системы и микросхемы.</span><span class="sxs-lookup"><span data-stu-id="6928e-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="6928e-152">В следующей таблице перечислены клиентские версии, которые будут запускать пакеты, созданные с использованием различных версий секвенсора.</span><span class="sxs-lookup"><span data-stu-id="6928e-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

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
<th align="left"></th>
<th align="left"><span data-ttu-id="6928e-153">Упорядочение с помощью секвенсора App-V 4,2</span><span class="sxs-lookup"><span data-stu-id="6928e-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="6928e-154">Упорядочение с помощью секвенсора App-V 4,5</span><span class="sxs-lookup"><span data-stu-id="6928e-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="6928e-155">Последовательное использование 32-разрядного приложения Sequencer-V 4,6</span><span class="sxs-lookup"><span data-stu-id="6928e-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="6928e-156">Последовательное использование 64-разрядного приложения Sequencer-V 4,6</span><span class="sxs-lookup"><span data-stu-id="6928e-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="6928e-157">Последовательное использование 32-разрядного приложения Sequencer-V 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="6928e-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="6928e-158">Последовательное использование 64-разрядного приложения Sequencer-V 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="6928e-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-159">клиент 4,2</span><span class="sxs-lookup"><span data-stu-id="6928e-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-160">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-161">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-162">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-163">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-164">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-165">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-166">клиент 4,5 ¹</span><span class="sxs-lookup"><span data-stu-id="6928e-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-167">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-168">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-169">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-170">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-171">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-172">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-173">клиент 4,6 (32-разр.)</span><span class="sxs-lookup"><span data-stu-id="6928e-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-174">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-175">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-176">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-177">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-178">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-179">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-180">клиент 4,6 (64-разр.)</span><span class="sxs-lookup"><span data-stu-id="6928e-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-181">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-182">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-183">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-184">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-185">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-186">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6928e-187">Клиент 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="6928e-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-188">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-189">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-190">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-191">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-192">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-193">Нет</span><span class="sxs-lookup"><span data-stu-id="6928e-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6928e-194">Клиент 4,6 SP1 (64-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="6928e-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-195">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-196">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-197">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-198">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-199">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="6928e-200">Да</span><span class="sxs-lookup"><span data-stu-id="6928e-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6928e-201">¹ применяется ко всем версиям клиента App-V 4.5, включая App-V 4.5, App-v 4.5 CU1 и App-V 4.5 SP1.</span><span class="sxs-lookup"><span data-stu-id="6928e-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="6928e-202">Дополнительные вопросы миграции</span><span class="sxs-lookup"><span data-stu-id="6928e-202">Additional Migration Considerations</span></span>


<span data-ttu-id="6928e-203">Одной из функций приложения App-V 4.5 является возможность создания файлов установщика Windows (MSI) в качестве контрольных точек для обеспечения взаимодействия виртуальных пакетов приложений с помощью встроенных в электронную систему программного обеспечения (например, Microsoft Endpoint Configuration Manager).</span><span class="sxs-lookup"><span data-stu-id="6928e-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="6928e-204">Предыдущие файлы установщика Windows, созданные с помощью средства. msi для виртуализации приложений, которые были установлены в клиенте App-V 4.1 или 4.2, которые впоследствии обновлены до версии 4.5, продолжают работать, но не могут быть установлены на клиенте 4.5.</span><span class="sxs-lookup"><span data-stu-id="6928e-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="6928e-205">Однако они не могут быть удалены или обновлены до тех пор, пока они не будут обновлены в секвенсоре 4.5.</span><span class="sxs-lookup"><span data-stu-id="6928e-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="6928e-206">Первоначальный виртуальный пакет приложения до 4,5 должен быть открыт в секвенсоре 4.5 и сохранен как файл установщика Windows.</span><span class="sxs-lookup"><span data-stu-id="6928e-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="6928e-207">**Примечание**  Если клиент App-V 4.2 уже обновлен до версии 4.5, вы можете использовать сценарии для решения проблем с сохранением пакетов 4.2 на 4,5 клиентах и предоставления им возможности управления.</span><span class="sxs-lookup"><span data-stu-id="6928e-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="6928e-208">Этот сценарий должен скопировать два файла, msvcp71.dll и msvcr71.dll в папку установки App-V и установить следующие значения в разделе реестра \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="6928e-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="6928e-209">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="6928e-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="6928e-210">"GlobalDataDirectory" = "C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (доступное для записи глобальное расположение)</span><span class="sxs-lookup"><span data-stu-id="6928e-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="6928e-211">Файлы установщика Windows, созданные с помощью секвенсора App-V 4,5, выводят сообщение об ошибке "Этот пакет требует клиента Microsoft Application Virtualization 4,5 или более поздней версии" при попытке запустить их в клиенте App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="6928e-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="6928e-212">Откройте старый пакет с помощью секвенсора App-V 4,5 с пакетом обновления 1 (SP1) или секвенсор App-V 4,6, а затем создайте новый MSI-пакет.</span><span class="sxs-lookup"><span data-stu-id="6928e-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="6928e-213">Созданные и сохраненные отчеты 4.2 будут перезаписаны, когда сервер будет обновлен до версии 4.5.</span><span class="sxs-lookup"><span data-stu-id="6928e-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="6928e-214">Если вы хотите сохранить эти отчеты, необходимо сохранить резервную копию файла SftMMC. msc, расположенную в папке консоли управления SoftGrid на сервере, и использовать эту копию для замены нового SftMMC. msc, установленного во время обновления.</span><span class="sxs-lookup"><span data-stu-id="6928e-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="6928e-215">Дополнительные сведения об обновлении предыдущей версии [можно найти в статье обновление до Microsoft Application Virtualization 4,5 (вопросы и ответы](https://go.microsoft.com/fwlink/?LinkId=120358) ) https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="6928e-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="6928e-216">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="6928e-216">Related topics</span></span>


[<span data-ttu-id="6928e-217">Планирование развертывания системы виртуализации приложений</span><span class="sxs-lookup"><span data-stu-id="6928e-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





