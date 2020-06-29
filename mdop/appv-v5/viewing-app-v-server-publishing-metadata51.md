---
title: Просмотр метаданных публикации сервера App-V
description: Просмотр метаданных публикации сервера App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813232"
---
# <span data-ttu-id="c5011-103">Просмотр метаданных публикации сервера App-V</span><span class="sxs-lookup"><span data-stu-id="c5011-103">Viewing App-V Server Publishing Metadata</span></span>


<span data-ttu-id="c5011-104">Используйте эту процедуру для просмотра метаданных публикации, которые помогут вам устранить проблемы, связанные с публикацией.</span><span class="sxs-lookup"><span data-stu-id="c5011-104">Use this procedure to view publishing metadata, which can help you resolve publishing-related issues.</span></span> <span data-ttu-id="c5011-105">Для использования этой процедуры необходимо использовать сервер управления App-V.</span><span class="sxs-lookup"><span data-stu-id="c5011-105">You must be using the App-V Management server to use this procedure.</span></span>

<span data-ttu-id="c5011-106">В этой статье содержатся указанные ниже сведения.</span><span class="sxs-lookup"><span data-stu-id="c5011-106">This article contains the following information:</span></span>

-   [<span data-ttu-id="c5011-107">Требования к приложению App-V 5,1 для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="c5011-107">App-V 5.1 requirements for viewing publishing metadata</span></span>](#bkmk-51-reqs-pub-meta)

-   [<span data-ttu-id="c5011-108">Синтаксис, используемый для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="c5011-108">Syntax to use for viewing publishing metadata</span></span>](#bkmk-syntax-view-pub-meta)

-   [<span data-ttu-id="c5011-109">Значения запроса для операционной системы и версии клиента</span><span class="sxs-lookup"><span data-stu-id="c5011-109">Query values for client operating system and version</span></span>](#bkmk-values-query-pub-meta)

-   [<span data-ttu-id="c5011-110">Определение метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="c5011-110">Definition of publishing metadata</span></span>](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a><span data-ttu-id="c5011-111">Требования к приложению App-V 5,1 для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="c5011-111">App-V 5.1 requirements for viewing publishing metadata</span></span>


<span data-ttu-id="c5011-112">В приложении App-V 5,1 необходимо указать следующие значения в адресе при запросе метаданных на сервере публикации App-V.</span><span class="sxs-lookup"><span data-stu-id="c5011-112">In App-V 5.1, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5011-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c5011-113">Value</span></span></th>
<th align="left"><span data-ttu-id="c5011-114">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="c5011-114">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c5011-115">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="c5011-115">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c5011-116">Если вы пропускаете <strong> </strong> параметр ClientVersion из запроса, метаданные не включают возможности, которые были новыми в App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="c5011-116">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the features that were new in App-V 5.0 SP3.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="c5011-117">ClientOS</span><span class="sxs-lookup"><span data-stu-id="c5011-117">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c5011-118">Это значение нужно указывать только в том случае, если в качестве последовательности пакетов выбраны определенные клиентские операционные системы.</span><span class="sxs-lookup"><span data-stu-id="c5011-118">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="c5011-119">Если вы выбрали вариант по умолчанию (все операционные системы), не указывайте это значение в запросе.</span><span class="sxs-lookup"><span data-stu-id="c5011-119">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="c5011-120">Если вы пропускаете <strong> </strong> параметр ClientOS из запроса, только пакеты, упорядоченные для поддержки любой операционной системы, отображаются в метаданных.</span><span class="sxs-lookup"><span data-stu-id="c5011-120">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a><span data-ttu-id="c5011-121">Синтаксис запроса для просмотра метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="c5011-121">Query syntax for viewing publishing metadata</span></span>


<span data-ttu-id="c5011-122">В таблице ниже приведены примеры синтаксиса и запроса.</span><span class="sxs-lookup"><span data-stu-id="c5011-122">The following table provides the syntax and query examples.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5011-123">Версия App-V</span><span class="sxs-lookup"><span data-stu-id="c5011-123">Version of App-V</span></span></th>
<th align="left"><span data-ttu-id="c5011-124">Синтаксис запроса</span><span class="sxs-lookup"><span data-stu-id="c5011-124">Query syntax</span></span></th>
<th align="left"><span data-ttu-id="c5011-125">Описание параметров</span><span class="sxs-lookup"><span data-stu-id="c5011-125">Parameter descriptions</span></span></th>
<th align="left"><span data-ttu-id="c5011-126">Пример.</span><span class="sxs-lookup"><span data-stu-id="c5011-126">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-127">App-V 5,0 с пакетом обновления 3 (SP3) и App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="c5011-127">App-V 5.0 SP3 and App-V 5.1</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5011-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="c5011-128">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c5011-129">Описание</span><span class="sxs-lookup"><span data-stu-id="c5011-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-130">&lt;PubServer&gt;</span><span class="sxs-lookup"><span data-stu-id="c5011-130">&lt;PubServer&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-131">Имя сервера публикаций App-V.</span><span class="sxs-lookup"><span data-stu-id="c5011-131">Name of the App-V Publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-132">&lt;Порт публикации #&gt;</span><span class="sxs-lookup"><span data-stu-id="c5011-132">&lt;Publishing Port#&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-133">Порт для сервера публикаций App-V, определенного при настройке сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="c5011-133">Port to the App-V Publishing server, which you defined when you configured the Publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-134">ClientVersion = &lt; AppvClientVersion&gt;</span><span class="sxs-lookup"><span data-stu-id="c5011-134">ClientVersion=&lt;AppvClientVersion&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-135">Версия клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="c5011-135">Version of the App-V client.</span></span> <span data-ttu-id="c5011-136">Ниже приведена таблица с правильным значением, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="c5011-136">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-137">ClientOS = &lt; OSStringValue&gt;</span><span class="sxs-lookup"><span data-stu-id="c5011-137">ClientOS=&lt;OSStringValue&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-138">Операционная система компьютера, на котором запущен клиент App-V.</span><span class="sxs-lookup"><span data-stu-id="c5011-138">Operating system of the computer that is running the App-V client.</span></span> <span data-ttu-id="c5011-139">Ниже приведена таблица с правильным значением, которое необходимо использовать.</span><span class="sxs-lookup"><span data-stu-id="c5011-139">Refer to the following table for the correct value to use.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p><span data-ttu-id="c5011-140">Чтобы получить имя сервера публикаций и номер порта (http:// &lt; PubServer &gt; : &lt; Publish Port # &gt; ) из клиента App-V, просмотрите конфигурацию URL-адреса <strong> </strong> командлета PowerShell Get-AppvPublishingServer.</span><span class="sxs-lookup"><span data-stu-id="c5011-140">To get the name of the Publishing server and the port number (http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;) from the App-V Client, look at the URL configuration of the <strong>Get-AppvPublishingServer</strong> PowerShell cmdlet.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p><span data-ttu-id="c5011-141">В примере:</span><span class="sxs-lookup"><span data-stu-id="c5011-141">In the example:</span></span></p>
<ul>
<li><p><span data-ttu-id="c5011-142">Служба публикации размещается на сервере Windows Server 2012 R2 под названием "pubsvr01".</span><span class="sxs-lookup"><span data-stu-id="c5011-142">A Windows Server 2012 R2 named “pubsvr01” hosts the Publishing service.</span></span></p></li>
<li><p><span data-ttu-id="c5011-143">Клиент Windows — это Windows 8,1 с 64-разр.</span><span class="sxs-lookup"><span data-stu-id="c5011-143">The Windows client is Windows 8.1 64-bit.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-144">App-V 5,0 – App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="c5011-144">App-V 5.0 through App-V 5.0 SP2</span></span></p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong><span data-ttu-id="c5011-145">Примечание.</span><span class="sxs-lookup"><span data-stu-id="c5011-145">Note</span></span></strong><br/><p><strong><span data-ttu-id="c5011-146">ClientVersion </strong> и <strong> ClientOS </strong> поддерживаются только в app-v 5,0 SP3 и App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="c5011-146">ClientVersion</strong> and <strong>ClientOS</strong> are supported only in App-V 5.0 SP3 and App-V 5.1.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c5011-147">Ознакомьтесь со сведениями о приложении App-V 5,0 SP3 и App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="c5011-147">See the information for App-V 5.0 SP3 and App-V 5.1.</span></span></p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p><span data-ttu-id="c5011-148">В примере сервер Windows Server 2012 R2 с именем "pubsvr01" содержит службы управления и публикации.</span><span class="sxs-lookup"><span data-stu-id="c5011-148">In the example, A Windows Server 2012 R2 named “pubsvr01” hosts the Management and Publishing services.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a><span data-ttu-id="c5011-149">Значения запроса для операционной системы и версии клиента</span><span class="sxs-lookup"><span data-stu-id="c5011-149">Query values for client operating system and version</span></span>


<span data-ttu-id="c5011-150">В запросе метаданных публикации введите значения строки, соответствующие клиентской операционной системе и версии, которые вы используете.</span><span class="sxs-lookup"><span data-stu-id="c5011-150">In your publishing metadata query, enter the string values that correspond to the client operating system and version that you’re using.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c5011-151">Операционная система</span><span class="sxs-lookup"><span data-stu-id="c5011-151">Operating system</span></span></th>
<th align="left"><span data-ttu-id="c5011-152">Архитектура</span><span class="sxs-lookup"><span data-stu-id="c5011-152">Architecture</span></span></th>
<th align="left"><span data-ttu-id="c5011-153">Строковое значение операционной строки</span><span class="sxs-lookup"><span data-stu-id="c5011-153">Operating string string value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-154">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="c5011-154">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-155">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-155">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-156">WindowsClient_10.0_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-156">WindowsClient_10.0_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-157">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="c5011-157">Windows 10</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-158">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-158">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-159">WindowsClient_10.0_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-159">WindowsClient_10.0_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c5011-160">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-161">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-161">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-162">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-162">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-163">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c5011-163">Windows 8.1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-164">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-164">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-165">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-165">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-166">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5011-166">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-167">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-167">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-168">WindowsClient_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-168">WindowsClient_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c5011-169">Windows 8</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-170">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-170">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-171">WindowsClient_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-171">WindowsClient_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c5011-172">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-173">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-173">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-174">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-174">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-175">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c5011-175">Windows Server 2012 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-176">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-176">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-177">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-177">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-178">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5011-178">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-179">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-179">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-180">WindowsServer_6.2_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-180">WindowsServer_6.2_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c5011-181">Windows Server 2012</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-182">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-182">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-183">WindowsServer_6.2_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-183">WindowsServer_6.2_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-184">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="c5011-184">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-185">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-185">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-186">WindowsClient_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-186">WindowsClient_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-187">Windows 7;</span><span class="sxs-lookup"><span data-stu-id="c5011-187">Windows 7</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-188">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-188">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-189">WindowsClient_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-189">WindowsClient_6.1_x86</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c5011-190">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="c5011-190">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-191">64-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-191">64-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-192">WindowsServer_6.1_x64</span><span class="sxs-lookup"><span data-stu-id="c5011-192">WindowsServer_6.1_x64</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c5011-193">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="c5011-193">Windows Server 2008 R2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-194">32-разрядная</span><span class="sxs-lookup"><span data-stu-id="c5011-194">32-bit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c5011-195">WindowsServer_6.1_x86</span><span class="sxs-lookup"><span data-stu-id="c5011-195">WindowsServer_6.1_x86</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a><span data-ttu-id="c5011-196">Определение метаданных публикации</span><span class="sxs-lookup"><span data-stu-id="c5011-196">Definition of publishing metadata</span></span>


<span data-ttu-id="c5011-197">Если пакеты публикуются на компьютере, на котором запущен клиент App-V, на этот компьютер посылаются метаданные, указывающие, какие пакеты и группы подключений публикуются.</span><span class="sxs-lookup"><span data-stu-id="c5011-197">When packages are published to a computer that is running the App-V client, metadata is sent to that computer indicating which packages and connection groups are being published.</span></span> <span data-ttu-id="c5011-198">Клиент App-V делает два отдельных запроса для следующих данных:</span><span class="sxs-lookup"><span data-stu-id="c5011-198">The App-V Client makes two separate requests for the following:</span></span>

-   <span data-ttu-id="c5011-199">Пакеты и группы соединений, которые являются уполномоченными для клиентского компьютера.</span><span class="sxs-lookup"><span data-stu-id="c5011-199">Packages and connection groups that are entitled to the client computer.</span></span>

-   <span data-ttu-id="c5011-200">Пакеты и группы соединений, которые являются уполномоченными для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c5011-200">Packages and connection groups that are entitled to the current user.</span></span>

<span data-ttu-id="c5011-201">Сервер публикации обменивается данными с сервером управления, чтобы определить, какие пакеты и группы подключений доступны для инициатора запроса.</span><span class="sxs-lookup"><span data-stu-id="c5011-201">The Publishing server communicates with the Management server to determine which packages and connection groups are available to the requester.</span></span> <span data-ttu-id="c5011-202">Сервер публикаций необходимо зарегистрировать на сервере управления, чтобы создать метаданные.</span><span class="sxs-lookup"><span data-stu-id="c5011-202">The Publishing server must be registered with the Management server in order for the metadata to be generated.</span></span>

<span data-ttu-id="c5011-203">Вы можете просматривать метаданные для каждого запроса в веб-браузере с помощью запроса, который находится в контексте определенного пользователя или компьютера.</span><span class="sxs-lookup"><span data-stu-id="c5011-203">You can view the metadata for each request in an Internet browser by using a query that is in the context of the specific user or computer.</span></span>






## <span data-ttu-id="c5011-204">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="c5011-204">Related topics</span></span>


[<span data-ttu-id="c5011-205">Технический справочник для App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="c5011-205">Technical Reference for App-V 5.1</span></span>](technical-reference-for-app-v-51.md)









