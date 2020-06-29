---
title: Просмотр метаданных публикации сервера App-V
description: Просмотр метаданных публикации сервера App-V
author: dansimp
ms.assetid: 048dd42a-24d4-4cc4-81f6-7a919aadd9b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 304aa656de98a0c9d59f0a6166811ead911033ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813264"
---
# <span data-ttu-id="3bc92-103">Просмотр метаданных публикации сервера App-V</span><span class="sxs-lookup"><span data-stu-id="3bc92-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="3bc92-104">Используйте эту процедуру для просмотра метаданных публикации, которые помогут вам устранить проблемы, связанные с публикацией.</span><span class="sxs-lookup"><span data-stu-id="3bc92-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="3bc92-105">Для использования этой процедуры необходимо использовать сервер управления App-V.</span><span class="sxs-lookup"><span data-stu-id="3bc92-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="3bc92-106">В этой статье содержатся указанные ниже сведения.</span><span class="sxs-lookup"><span data-stu-id="3bc92-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="3bc92-107">Требования к App-V 5,0 SP3 для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="3bc92-107">App-V 5.0 SP3 requirements for viewing publishing metadata</span></span>](#bkmk-50sp3-reqs-pub-meta)

-   [<span data-ttu-id="3bc92-108">Синтаксис, используемый для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="3bc92-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="3bc92-109">Значения запроса для операционной системы и версии клиента</span><span class="sxs-lookup"><span data-stu-id="3bc92-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="3bc92-110">Определение метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="3bc92-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-50sp3-reqs-pub-meta"></a><span data-ttu-id="3bc92-111">Требования к App-V 5,0 SP3 для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="3bc92-111">App-V 5.0 SP3 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="3bc92-112">В приложении App-V 5,0 с пакетом обновления 3 (SP3) при выполнении запроса метаданных на сервере публикации App-V необходимо указать указанные ниже значения.</span><span class="sxs-lookup"><span data-stu-id="3bc92-112">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bc92-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3bc92-113">Value</span></span></th>
<th align="left"><span data-ttu-id="3bc92-114">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3bc92-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3bc92-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="3bc92-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bc92-116">Если вы пропускаете <strong> </strong> параметр ClientVersion из запроса, метаданные не включают новую функциональность App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3bc92-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="3bc92-117">ClientOS</span><span class="sxs-lookup"><span data-stu-id="3bc92-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3bc92-118">Это значение нужно указывать только в том случае, если в качестве последовательности пакетов выбраны определенные клиентские операционные системы.</span><span class="sxs-lookup"><span data-stu-id="3bc92-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="3bc92-119">Если вы выбрали вариант по умолчанию (все операционные системы), не указывайте это значение в запросе.</span><span class="sxs-lookup"><span data-stu-id="3bc92-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="3bc92-120">Если вы пропускаете <strong> </strong> параметр ClientOS из запроса, только пакеты, упорядоченные для поддержки любой операционной системы, отображаются в метаданных.</span><span class="sxs-lookup"><span data-stu-id="3bc92-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="3bc92-121">Синтаксис запроса для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="3bc92-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="3bc92-122">В таблице ниже приведены примеры синтаксиса и запроса.</span><span class="sxs-lookup"><span data-stu-id="3bc92-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bc92-123">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="3bc92-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="3bc92-124">Синтаксис запроса</span><span class="sxs-lookup"><span data-stu-id="3bc92-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="3bc92-125">Описание параметров</span><span class="sxs-lookup"><span data-stu-id="3bc92-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="3bc92-126">Пример.</span><span class="sxs-lookup"><span data-stu-id="3bc92-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-127">App-V 5,0 с пакетом обновления 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="3bc92-127">App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bc92-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="3bc92-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="3bc92-129">Описание</span><span class="sxs-lookup"><span data-stu-id="3bc92-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="3bc92-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-131">Имя сервера публикаций App-V.</span><span class="sxs-lookup"><span data-stu-id="3bc92-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-132">&lt;Порт публикации #&gt;</span><span class="sxs-lookup"><span data-stu-id="3bc92-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-133">Порт для сервера публикаций App-V, определенного при настройке сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="3bc92-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="3bc92-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-135">Версия клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="3bc92-135">Version of the App-V client.</span></span> <span data-ttu-id="3bc92-136">Ниже приведена таблица с правильным значением, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="3bc92-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-137">ClientOS = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="3bc92-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-138">Операционная система компьютера, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="3bc92-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="3bc92-139">Ниже приведена таблица с правильным значением, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="3bc92-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="3bc92-140">Чтобы получить имя сервера публикаций и номер порта (http:// &lt; PubServer &gt; : &lt; Publish Port # &gt; ) из клиента App-V, просмотрите конфигурацию URL-адреса <strong> </strong> командлета PowerShell Get-AppvPublishingServer.</span><span class="sxs-lookup"><span data-stu-id="3bc92-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="3bc92-141">В примере:</span><span class="sxs-lookup"><span data-stu-id="3bc92-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="3bc92-142">Служба публикации размещается на сервере Windows Server 2012 R2 под названием "pubsvr01".</span><span class="sxs-lookup"><span data-stu-id="3bc92-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="3bc92-143">Клиент Windows — это Windows 8,1 с 64-разр.</span><span class="sxs-lookup"><span data-stu-id="3bc92-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-144">App-V 5,0 – App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="3bc92-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="3bc92-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="3bc92-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="3bc92-146">ClientVersion </strong> и <strong> ClientOS </strong> поддерживаются только в App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3bc92-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="3bc92-147">Ознакомьтесь со сведениями о приложении App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="3bc92-147">See the information for App-V 5.0 SP3.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="3bc92-148">В примере сервер Windows Server 2012 R2 с именем "pubsvr01" содержит службы управления и публикации.</span><span class="sxs-lookup"><span data-stu-id="3bc92-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="3bc92-149">Значения запроса для операционной системы и версии клиента</span><span class="sxs-lookup"><span data-stu-id="3bc92-149">Query values for client operating system and version</span></span>


<span data-ttu-id="3bc92-150">В запросе метаданных публикации введите значения строки, соответствующие клиентской операционной системе и версии, которые вы используете.</span><span class="sxs-lookup"><span data-stu-id="3bc92-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3bc92-151">Операционная система</span><span class="sxs-lookup"><span data-stu-id="3bc92-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="3bc92-152">Архитектура</span><span class="sxs-lookup"><span data-stu-id="3bc92-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="3bc92-153">Строковое значение операционной строки</span><span class="sxs-lookup"><span data-stu-id="3bc92-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-154">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3bc92-154">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-155">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-156">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="3bc92-156">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="3bc92-157">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-158">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-159">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="3bc92-159">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-160">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3bc92-160">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-161">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-162">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="3bc92-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-163">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3bc92-163">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-164">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-165">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="3bc92-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-166">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3bc92-166">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-167">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-168">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="3bc92-168">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-169">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="3bc92-169">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-170">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-171">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="3bc92-171">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bc92-172">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-173">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-174">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="3bc92-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3bc92-175">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-176">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-177">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="3bc92-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-178">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="3bc92-178">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-179">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-180">WindowsClient_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="3bc92-180">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-181">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="3bc92-181">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-182">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-183">WindowsClient_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="3bc92-183">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="3bc92-184">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="3bc92-184">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-185">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-186">WindowsServer_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="3bc92-186">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="3bc92-187">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="3bc92-187">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-188">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="3bc92-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="3bc92-189">WindowsServer_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="3bc92-189">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="3bc92-190">Определение метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="3bc92-190">Definition of publishing metadata</span></span>


<span data-ttu-id="3bc92-191">Если пакеты публикуются на компьютере, на котором запущен клиент App-V, на этот компьютер посылаются метаданные, указывающие, какие пакеты и группы подключений публикуются.</span><span class="sxs-lookup"><span data-stu-id="3bc92-191">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="3bc92-192">Клиент App-V делает два отдельных запроса для следующих данных:</span><span class="sxs-lookup"><span data-stu-id="3bc92-192">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="3bc92-193">Пакеты и группы соединений, которые являются уполномоченными для клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="3bc92-193">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="3bc92-194">Пакеты и группы соединений, которые являются уполномоченными для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="3bc92-194">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="3bc92-195">Сервер публикации обменивается данными с сервером управления, чтобы определить, какие пакеты и группы подключений доступны для инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="3bc92-195">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="3bc92-196">Сервер публикаций необходимо зарегистрировать на сервере управления, чтобы создать метаданные.</span><span class="sxs-lookup"><span data-stu-id="3bc92-196">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="3bc92-197">Вы можете просматривать метаданные для каждого запроса в веб-браузере с помощью запроса, который находится в контексте определенного пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="3bc92-197">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="3bc92-198">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="3bc92-198">Related topics</span></span>


[<span data-ttu-id="3bc92-199">Технический справочник по App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="3bc92-199">Technical Reference for App-V 5.0</span></span>](technical-reference-for-app-v-50.md)









