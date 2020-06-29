---
title: Параметры командной строки установщика клиента Application Virtualization
description: Параметры командной строки установщика клиента Application Virtualization
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819719"
---
# <span data-ttu-id="caeb3-103">Параметры командной строки установщика клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="caeb3-103">Application Virtualization Client Installer Command-Line Parameters</span></span>


<span data-ttu-id="caeb3-104">В следующей таблице перечислены все доступные параметры командной строки установщика клиента Microsoft Application Virtualization, их значения и краткое описание каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="caeb3-104">The following table lists all available Microsoft Application Virtualization Client installer command-line parameters, their values, and a brief description of each parameter.</span></span> <span data-ttu-id="caeb3-105">Параметры чувствительны к регистру и должны вводиться как прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="caeb3-105">Parameters are case-sensitive and must be entered as all-uppercase letters.</span></span> <span data-ttu-id="caeb3-106">Все значения параметров должны быть заключены в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="caeb3-106">All parameter values must be enclosed in double quotes.</span></span>

**<span data-ttu-id="caeb3-107">Примечание.</span><span class="sxs-lookup"><span data-stu-id="caeb3-107">Note</span></span>**  
-   <span data-ttu-id="caeb3-108">Для App-V версии 4,6 параметры командной строки нельзя использовать во время обновления клиента.</span><span class="sxs-lookup"><span data-stu-id="caeb3-108">For App-V version 4.6, command-line parameters cannot be used during a client upgrade.</span></span>

-   <span data-ttu-id="caeb3-109">Параметры *SWICACHESIZE* и *MINFREESPACEMB* нельзя сочетать в командной строке.</span><span class="sxs-lookup"><span data-stu-id="caeb3-109">The *SWICACHESIZE* and *MINFREESPACEMB* parameters cannot be combined on the command line.</span></span> <span data-ttu-id="caeb3-110">Если используются оба аргумента, параметр *SWICACHESIZE* будет игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="caeb3-110">If both are used, the *SWICACHESIZE* parameter will be ignored.</span></span>



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="caeb3-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="caeb3-111">Parameter</span></span></th>
<th align="left"><span data-ttu-id="caeb3-112">Данные</span><span class="sxs-lookup"><span data-stu-id="caeb3-112">Values</span></span></th>
<th align="left"><span data-ttu-id="caeb3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="caeb3-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-114">ALLOWINDEPENDENTFILESTREAMING</span><span class="sxs-lookup"><span data-stu-id="caeb3-114">ALLOWINDEPENDENTFILESTREAMING</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-115">TRUE</span><span class="sxs-lookup"><span data-stu-id="caeb3-115">TRUE</span></span></p>
<p><span data-ttu-id="caeb3-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="caeb3-116">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-117">Указывает, будет ли включена потоковая передача из файла независимо от того, как был настроен клиент с <em> помощью </em> параметра APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="caeb3-117">Indicates whether streaming from file will be enabled regardless of how the client has been configured with the <em>APPLICATIONSOURCEROOT</em> parameter.</span></span> <span data-ttu-id="caeb3-118">Если задано значение FALSE, транспорт не включит потоковую передачу из файлов даже в том случае, если в качестве <em> параметра APPLICATIONSOURCEROOT в OSD </em> есть путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="caeb3-118">If set to FALSE, the transport will not enable streaming from files even if the OSD HREF or the <em>APPLICATIONSOURCEROOT</em> parameter contains a file path.</span></span></p>
<p><span data-ttu-id="caeb3-119">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="caeb3-119">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="caeb3-120">TRUE — приложение, развернутое вручную, может быть загружено с диска.</span><span class="sxs-lookup"><span data-stu-id="caeb3-120">TRUE—Manually deployed application may be loaded from disk.</span></span></p></li>
<li><p><span data-ttu-id="caeb3-121">FALSE — все приложения должны поступать из исходного потокового сервера.</span><span class="sxs-lookup"><span data-stu-id="caeb3-121">FALSE—All applications must come from source streaming server.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-122">APPLICATIONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="caeb3-122">APPLICATIONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-123"><em>URL-адрес RTSP:// </em> (для доставки динамического пакета)</span><span class="sxs-lookup"><span data-stu-id="caeb3-123">RTSP:// <em>URL</em> (for dynamic package delivery)</span></span></p>
<p><span data-ttu-id="caeb3-124"><em>URL-адрес file:// </em> или <em> UNC </em> (для загрузки из файла с пакетом доставки)</span><span class="sxs-lookup"><span data-stu-id="caeb3-124">File:// <em>URL</em> or <em>UNC</em> (for load from file package delivery)</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-125">Чтобы включить администратора или электронную систему распространения программного обеспечения, чтобы обеспечить выполнение загрузки приложения в соответствии с схемой управления топологией, можно переопределить базу кода OSD для элемента HREF приложения (исходное расположение).</span><span class="sxs-lookup"><span data-stu-id="caeb3-125">To enable an administrator or an electronic software distribution system to ensure that application loading is performed in compliance with the topology management scheme, allows an override of the OSD CODEBASE for the application HREF element (the source location).</span></span> <span data-ttu-id="caeb3-126">Если значение равно "", то есть значение по умолчанию, используются существующие параметры OSD файла.</span><span class="sxs-lookup"><span data-stu-id="caeb3-126">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="caeb3-127">URL-адрес состоит из нескольких частей.</span><span class="sxs-lookup"><span data-stu-id="caeb3-127">A URL has several parts:</span></span></p>
<p><span data-ttu-id="caeb3-128">&lt;протокол &gt; :// &lt; сервер &gt; : &lt; &gt; / &lt; путь к порту &gt; / &lt; ? &gt; &lt; #fragment запросов&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-128">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="caeb3-129">Путь в формате UNC состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="caeb3-129">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="caeb3-130">&amp;lt; имя_компьютера &gt; &amp; lt; общий доступ к папке &gt; &amp; lt; ресурс&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-130">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<p><span data-ttu-id="caeb3-131">Если <em> параметр APPLICATIONSOURCEROOT </em> указан на клиентском компьютере, клиент будет прерывать URL-адрес или путь UNC из файла OSD в составные части и заменять разделы OSD соответствующими <em> </em> разделами APPLICATIONSOURCEROOT.</span><span class="sxs-lookup"><span data-stu-id="caeb3-131">If the <em>APPLICATIONSOURCEROOT</em> parameter is specified on a client, the client will break the URL or UNC path from an OSD file into its constituent parts and replace the OSD sections with the corresponding <em>APPLICATIONSOURCEROOT</em> sections.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-132">Важно.</span><span class="sxs-lookup"><span data-stu-id="caeb3-132">Important</span></span></strong><br/><p><span data-ttu-id="caeb3-133">Убедитесь, что при использовании file://с путями в формате UNC используется правильный формат.</span><span class="sxs-lookup"><span data-stu-id="caeb3-133">Be sure to use the correct format when using file:// with a UNC path.</span></span> <span data-ttu-id="caeb3-134">Правильный формат: file:// &amp; lt; сервер &gt; &amp; lt; общий доступ &gt; .</span><span class="sxs-lookup"><span data-stu-id="caeb3-134">The correct format is file://&amp;lt;server&gt;&amp;lt;share&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-135">ICONSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="caeb3-135">ICONSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="caeb3-136">UNC</span><span class="sxs-lookup"><span data-stu-id="caeb3-136">UNC</span></span></em></p>
<p><span data-ttu-id="caeb3-137">URL <em> -адрес http:// </em> или <em> url-адрес https://</span><span class="sxs-lookup"><span data-stu-id="caeb3-137">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-138">Позволяет администратору указать исходное расположение для получения значка для серийного пакета приложения во время публикации.</span><span class="sxs-lookup"><span data-stu-id="caeb3-138">Enables an administrator to specify a source location for icon retrieval for a sequenced application package during publication.</span></span> <span data-ttu-id="caeb3-139">Корни источника значков поддерживают пути в формате UNC и URL-адреса (HTTP или HTTPS).</span><span class="sxs-lookup"><span data-stu-id="caeb3-139">Icon source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="caeb3-140">Если значение равно "", то есть значение по умолчанию, используются существующие параметры OSD файла.</span><span class="sxs-lookup"><span data-stu-id="caeb3-140">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="caeb3-141">URL-адрес состоит из нескольких частей.</span><span class="sxs-lookup"><span data-stu-id="caeb3-141">A URL has several parts:</span></span></p>
<p><span data-ttu-id="caeb3-142">&lt;протокол &gt; :// &lt; сервер &gt; : &lt; &gt; / &lt; путь к порту &gt; / &lt; ? &gt; &lt; #fragment запросов&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-142">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="caeb3-143">Путь в формате UNC состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="caeb3-143">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="caeb3-144">&amp;lt; имя_компьютера &gt; &amp; lt; общий доступ к папке &gt; &amp; lt; ресурс&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-144">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-145">Важно.</span><span class="sxs-lookup"><span data-stu-id="caeb3-145">Important</span></span></strong><br/><p><span data-ttu-id="caeb3-146">При использовании UNC-пути следует использовать правильный формат.</span><span class="sxs-lookup"><span data-stu-id="caeb3-146">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="caeb3-147">Допустимые форматы: &amp; lt; сервер &gt; &amp; lt; общий доступ &gt; или &lt; буква диска &gt; : &amp; lt; папка &gt; .</span><span class="sxs-lookup"><span data-stu-id="caeb3-147">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-148">OSDSOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="caeb3-148">OSDSOURCEROOT</span></span></em></p></td>
<td align="left"><p><em><span data-ttu-id="caeb3-149">UNC</span><span class="sxs-lookup"><span data-stu-id="caeb3-149">UNC</span></span></em></p>
<p><span data-ttu-id="caeb3-150">URL <em> -адрес http:// </em> или <em> url-адрес https://</span><span class="sxs-lookup"><span data-stu-id="caeb3-150">HTTP://<em>URL</em> or HTTPS://<em>URL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-151">Позволяет администратору указать расположение источника для получения файла OSD для пакета приложения во время публикации.</span><span class="sxs-lookup"><span data-stu-id="caeb3-151">Enables an administrator to specify a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="caeb3-152">Корни источника OSD поддерживают пути UNC и URL-адреса (HTTP или HTTPS).</span><span class="sxs-lookup"><span data-stu-id="caeb3-152">OSD source roots support UNC paths and URLs (HTTP or HTTPS).</span></span> <span data-ttu-id="caeb3-153">Если значение равно "", то есть значение по умолчанию, используются существующие параметры OSD файла.</span><span class="sxs-lookup"><span data-stu-id="caeb3-153">If the value is “”, which is the default value, the existing OSD file settings are used.</span></span></p>
<p><span data-ttu-id="caeb3-154">URL-адрес состоит из нескольких частей.</span><span class="sxs-lookup"><span data-stu-id="caeb3-154">A URL has several parts:</span></span></p>
<p><span data-ttu-id="caeb3-155">&lt;протокол &gt; :// &lt; сервер &gt; : &lt; &gt; / &lt; путь к порту &gt; / &lt; ? &gt; &lt; #fragment запросов&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-155">&lt;protocol&gt;://&lt;server&gt;:&lt;port&gt;/&lt;path&gt;/&lt;?query&gt;&lt;#fragment&gt;</span></span></p>
<p><span data-ttu-id="caeb3-156">Путь в формате UNC состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="caeb3-156">A UNC path has three parts:</span></span></p>
<p><span data-ttu-id="caeb3-157">&amp;lt; имя_компьютера &gt; &amp; lt; общий доступ к папке &gt; &amp; lt; ресурс&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-157">&amp;lt;computername&gt;&amp;lt;share folder&gt;&amp;lt;resource&gt;</span></span></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-158">Важно.</span><span class="sxs-lookup"><span data-stu-id="caeb3-158">Important</span></span></strong><br/><p><span data-ttu-id="caeb3-159">При использовании UNC-пути следует использовать правильный формат.</span><span class="sxs-lookup"><span data-stu-id="caeb3-159">Be sure to use the correct format when using a UNC path.</span></span> <span data-ttu-id="caeb3-160">Допустимые форматы: &amp; lt; сервер &gt; &amp; lt; общий доступ &gt; или &lt; буква диска &gt; : &amp; lt; папка &gt; .</span><span class="sxs-lookup"><span data-stu-id="caeb3-160">Acceptable formats are &amp;lt;server&gt;&amp;lt;share&gt; or &lt;drive letter&gt;:&amp;lt;folder&gt;.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-161">AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="caeb3-161">AUTOLOADONLOGIN</span></span></em></p>
<p><em><span data-ttu-id="caeb3-162">AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="caeb3-162">AUTOLOADONLAUNCH</span></span></em></p>
<p><em><span data-ttu-id="caeb3-163">AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="caeb3-163">AUTOLOADONREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-164">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="caeb3-164">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-165">Триггеры AutoLoad, определяющие события, инициирующие автоматическую загрузку приложений.</span><span class="sxs-lookup"><span data-stu-id="caeb3-165">The AutoLoad triggers that define the events that initiate auto-loading of applications.</span></span> <span data-ttu-id="caeb3-166">AutoLoad неявно использует фоновую потоковую передачу для обеспечения полной загрузки приложения в кэш.</span><span class="sxs-lookup"><span data-stu-id="caeb3-166">AutoLoad implicitly uses background streaming to enable the application to be fully loaded into cache.</span></span></p>
<p><span data-ttu-id="caeb3-167">Основной блок функций будет загружаться как можно быстрее.</span><span class="sxs-lookup"><span data-stu-id="caeb3-167">The primary feature block will be loaded as quickly as possible.</span></span> <span data-ttu-id="caeb3-168">Оставшиеся блоки функций будут загружены в фоновом режиме, чтобы обеспечить приоритетные операции, такие как взаимодействие пользователей с приложениями, и обеспечить оптимальную производительность.</span><span class="sxs-lookup"><span data-stu-id="caeb3-168">Remaining feature blocks will be loaded in the background to enable foreground operations, such as user interaction with applications, to take priority and provide optimal performance.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-169">Примечание.</span><span class="sxs-lookup"><span data-stu-id="caeb3-169">Note</span></span></strong><br/><p><span data-ttu-id="caeb3-170"><em>Параметр AUTOLOADTARGET </em> определяет, какие приложения загружаются автоматически.</span><span class="sxs-lookup"><span data-stu-id="caeb3-170">The <em>AUTOLOADTARGET</em> parameter determines which applications are auto-loaded.</span></span> <span data-ttu-id="caeb3-171">По умолчанию используемые пакеты загружаются автоматически, если <em> </em> не задано значение AUTOLOADTARGET.</span><span class="sxs-lookup"><span data-stu-id="caeb3-171">By default, packages that have been used are auto-loaded unless <em>AUTOLOADTARGET</em> is set.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="caeb3-172">Каждый параметр влияет на поведение при загрузке, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="caeb3-172">Each parameter affects loading behavior as follows:</span></span></p>
<ul>
<li><p><em><span data-ttu-id="caeb3-173">AUTOLOADONLOGIN </em> — Загрузка начинается, когда пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="caeb3-173">AUTOLOADONLOGIN</em>—Loading starts when the user logs in.</span></span></p></li>
<li><p><em><span data-ttu-id="caeb3-174">AUTOLOADONLAUNCH </em> — Загрузка начинается, когда пользователь запускает приложение.</span><span class="sxs-lookup"><span data-stu-id="caeb3-174">AUTOLOADONLAUNCH</em>—Loading starts when the user starts an application.</span></span></p></li>
<li><p><em><span data-ttu-id="caeb3-175">AUTOLOADONREFRESH </em> — Загрузка начинается, когда выполняется обновление публикации.</span><span class="sxs-lookup"><span data-stu-id="caeb3-175">AUTOLOADONREFRESH</em>—Loading starts when a publishing refresh occurs.</span></span></p></li>
</ul>
<p><span data-ttu-id="caeb3-176">Три значения могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="caeb3-176">The three values can be combined.</span></span> <span data-ttu-id="caeb3-177">В следующем примере триггеры AutoLoad включены как при входе пользователя, так и при обновлении публикации.</span><span class="sxs-lookup"><span data-stu-id="caeb3-177">In the following example, AutoLoad triggers are enabled both at user login and when publishing refresh occurs:</span></span></p>
<p><em><span data-ttu-id="caeb3-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="caeb3-178">AUTOLOADONLOGIN AUTOLOADONREFRESH</span></span></em></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-179">Примечание.</span><span class="sxs-lookup"><span data-stu-id="caeb3-179">Note</span></span></strong><br/><p><span data-ttu-id="caeb3-180">Если клиент настроил эти значения при первой установке, autoload не будет срабатывать до следующего выхода из системы и повторного входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="caeb3-180">If the client is configured with these values at first install, Autoload will not be triggered until the next time the user logs off and logs back on.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-181">AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="caeb3-181">AUTOLOADTARGET</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-182">НИЧЕГО</span><span class="sxs-lookup"><span data-stu-id="caeb3-182">NONE</span></span></p>
<p><span data-ttu-id="caeb3-183">ВЕСЬ</span><span class="sxs-lookup"><span data-stu-id="caeb3-183">ALL</span></span></p>
<p><span data-ttu-id="caeb3-184">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="caeb3-184">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-185">Указывает, что будет автоматически загружаться при возникновении любого определенного триггера AutoLoad.</span><span class="sxs-lookup"><span data-stu-id="caeb3-185">Indicates what will be auto-loaded when any given AutoLoad triggers occur.</span></span></p>
<p><span data-ttu-id="caeb3-186">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="caeb3-186">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="caeb3-187">NONE — без автоматической загрузки, независимо от того, какие триггеры могут быть заданы.</span><span class="sxs-lookup"><span data-stu-id="caeb3-187">NONE—No auto-loading, regardless of what triggers might be set.</span></span></p></li>
<li><p><span data-ttu-id="caeb3-188">ALL (если включен какой-либо триггер AutoLoad, все пакеты загружаются автоматически, независимо от того, были ли они запущены.</span><span class="sxs-lookup"><span data-stu-id="caeb3-188">ALL—If any AutoLoad trigger is enabled, all packages are automatically loaded, whether or not they have ever been launched.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-189">Примечание.</span><span class="sxs-lookup"><span data-stu-id="caeb3-189">Note</span></span></strong><br/><p><span data-ttu-id="caeb3-190">Этот параметр настраивается для отдельных пакетов с помощью <strong> команд "добавить пакет" </strong> и "Настройка пакета" SFTMIME <strong> </strong> .</span><span class="sxs-lookup"><span data-stu-id="caeb3-190">This setting is configured for individual packages by using the SFTMIME <strong>ADD PACKAGE</strong> and <strong>CONFIGURE PACKAGE</strong> commands.</span></span> <span data-ttu-id="caeb3-191">Дополнительные сведения об этих командах можно найти в разделе <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> Справочник по командам SFTMIME </a> .</span><span class="sxs-lookup"><span data-stu-id="caeb3-191">For more information about these commands, see <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)">SFTMIME Command Reference</a>.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="caeb3-192">PREVUSED — если включен какой-либо триггер AutoLoad, загрузите только те пакеты, в которых ранее использовалось хотя бы одно приложение в пакете (то есть, запущены или предварительно кэшированы).</span><span class="sxs-lookup"><span data-stu-id="caeb3-192">PREVUSED—If any AutoLoad trigger is enabled, load only the packages where at least one application in the package has been previously used (that is, launched or precached).</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="caeb3-193">Примечание.</span><span class="sxs-lookup"><span data-stu-id="caeb3-193">Note</span></span></strong><br/><p><span data-ttu-id="caeb3-194">При установке клиента App-V для использования кэша, доступного только для чтения (например, в качестве реализации сервера VDI), необходимо установить <em> </em> для параметра AUTOLOADTARGET значение None, чтобы клиент не мог обновить приложения в кэше только для чтения.</span><span class="sxs-lookup"><span data-stu-id="caeb3-194">When you install the App-V client to use a read-only cache, (for example, as a VDI server implementation), you must set the <em>AUTOLOADTARGET</em> parameter to NONE to prevent the client from trying to update applications in the read-only cache.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-195">DOTIMEOUTMINUTES</span><span class="sxs-lookup"><span data-stu-id="caeb3-195">DOTIMEOUTMINUTES</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-196">29600 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="caeb3-196">29600 (default)</span></span></p>
<p><span data-ttu-id="caeb3-197">1 – 1439998560 минут (диапазон)</span><span class="sxs-lookup"><span data-stu-id="caeb3-197">1–1439998560 minutes (range)</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-198">Показывает, сколько минут приложение может использоваться в отключенной операции.</span><span class="sxs-lookup"><span data-stu-id="caeb3-198">Indicates how many minutes an application may be used in disconnected operation.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-199">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="caeb3-199">INSTALLDIR</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-200">&lt;аппарат&gt;</span><span class="sxs-lookup"><span data-stu-id="caeb3-200">&lt;pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-201">Указывает каталог установки клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="caeb3-201">Specifies the installation directory of the App-V Client.</span></span></p>
<p><span data-ttu-id="caeb3-202">Пример: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization Client&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-202">Example: INSTALLDIR=&quot;C:\Program Files\Microsoft Application Virtualization Client&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-203">РЕЖИМ</span><span class="sxs-lookup"><span data-stu-id="caeb3-203">OPTIN</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-204">ЗАДАН</span><span class="sxs-lookup"><span data-stu-id="caeb3-204">“TRUE”</span></span></p>
<p><span data-ttu-id="caeb3-205">“”</span><span class="sxs-lookup"><span data-stu-id="caeb3-205">“”</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-206">Клиентские компоненты Microsoft Application Virtualization будут обновляться с помощью центра обновления Майкрософт, когда они доступны для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="caeb3-206">Microsoft Application Virtualization Client components will be upgradable through Microsoft Update when updates are made available to the general public.</span></span> <span data-ttu-id="caeb3-207">Для агента Центра обновления Майкрософт, установленного в операционных системах Windows, требуется явное согласие пользователя на использование службы.</span><span class="sxs-lookup"><span data-stu-id="caeb3-207">The Microsoft Update Agent installed on Windows operating systems requires a user to explicitly opt-in to use the service.</span></span> <span data-ttu-id="caeb3-208">Этот отказ требуется только один раз для всех приложений на устройстве.</span><span class="sxs-lookup"><span data-stu-id="caeb3-208">This opt-in is required only one time for all applications on the device.</span></span> <span data-ttu-id="caeb3-209">Если вы уже выбрали вариант "Microsoft Update", компоненты Microsoft Application Virtualization на устройстве будут автоматически использовать преимущества службы.</span><span class="sxs-lookup"><span data-stu-id="caeb3-209">If you have already opted into Microsoft Update, the Microsoft Application Virtualization components on the device will automatically take advantage of the service.</span></span></p>
<p><span data-ttu-id="caeb3-210">Для установки с помощью командной строки по умолчанию используется Microsoft Update (если только предыдущее приложение не включило на него) в соответствии с требованием, которое можно вручную внести в Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="caeb3-210">For command-line installation, use of Microsoft Update is by default opt-out (unless a previous application already enabled the device to be opted in) due to the requirement for manually opting into Microsoft Update.</span></span> <span data-ttu-id="caeb3-211">Таким образом, ожидание в установках должна быть явной для установки из командной строки.</span><span class="sxs-lookup"><span data-stu-id="caeb3-211">Therefore, opting in must be explicit for command-line installations.</span></span> <span data-ttu-id="caeb3-212">Установка для параметра "OptIn" <em> значения </em> true приводит к принудительному включению центра обновления Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="caeb3-212">Setting the command-line parameter <em>OPTIN</em> to TRUE forces the Microsoft Update opt-in to be set.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-213">REQUIREAUTHORIZATIONIFCACHED</span><span class="sxs-lookup"><span data-stu-id="caeb3-213">REQUIREAUTHORIZATIONIFCACHED</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-214">TRUE</span><span class="sxs-lookup"><span data-stu-id="caeb3-214">TRUE</span></span></p>
<p><span data-ttu-id="caeb3-215">FALSE</span><span class="sxs-lookup"><span data-stu-id="caeb3-215">FALSE</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-216">Указывает, требуется ли всегда проверка подлинности, независимо от того, какое приложение уже находится в кэше.</span><span class="sxs-lookup"><span data-stu-id="caeb3-216">Indicates whether authorization is always required, whether or not an application is already in cache.</span></span></p>
<p><span data-ttu-id="caeb3-217">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="caeb3-217">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="caeb3-218">TRUE — приложение всегда должно быть авторизовано при запуске.</span><span class="sxs-lookup"><span data-stu-id="caeb3-218">TRUE—Application always must be authorized at startup.</span></span> <span data-ttu-id="caeb3-219">Для потоковых приложений RTSP маркер авторизации пользователя отправляется на сервер для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="caeb3-219">For RTSP streamed applications, the user authorization token is sent to the server for authorization.</span></span> <span data-ttu-id="caeb3-220">Для файловых приложений списки ACL для файлов определяют, может ли пользователь получить доступ к приложению.</span><span class="sxs-lookup"><span data-stu-id="caeb3-220">For file-based applications, file ACLs dictate whether a user may access the application.</span></span></p></li>
<li><p><span data-ttu-id="caeb3-221">FALSE — всегда пытайтесь подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="caeb3-221">FALSE—Always try to connect to the server.</span></span> <span data-ttu-id="caeb3-222">Если не удается установить соединение с сервером, клиент по-прежнему позволяет пользователю запустить приложение, которое ранее было загружено в кэш.</span><span class="sxs-lookup"><span data-stu-id="caeb3-222">If a connection to the server cannot be established, the client still allows the user to launch an application that has previously been loaded into cache.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-223">SWICACHESIZE</span><span class="sxs-lookup"><span data-stu-id="caeb3-223">SWICACHESIZE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-224">Размер кэша в МЕГАБАЙТах</span><span class="sxs-lookup"><span data-stu-id="caeb3-224">Cache size in MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-225">Задает размер (в мегабайтах) кэша клиента.</span><span class="sxs-lookup"><span data-stu-id="caeb3-225">Specifies the size in megabytes of the client cache.</span></span> <span data-ttu-id="caeb3-226">Размер по умолчанию составляет 4096 МБ и максимальный размер составляет 1 048 576 МБ (1 ТБ).</span><span class="sxs-lookup"><span data-stu-id="caeb3-226">The default size is 4096 MB, and the maximum size is 1,048,576 MB (1 TB).</span></span> <span data-ttu-id="caeb3-227">Система проверяет наличие доступного места во время установки, но не резервирует пространство.</span><span class="sxs-lookup"><span data-stu-id="caeb3-227">The system checks for the available space at installation time, but the space is not reserved.</span></span></p>
<p><span data-ttu-id="caeb3-228">Пример: <strong> SWICACHESIZE = &quot; 1024&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-228">Example: <strong>SWICACHESIZE=&quot;1024&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-229">SWIPUBSVRDISPLAY</span><span class="sxs-lookup"><span data-stu-id="caeb3-229">SWIPUBSVRDISPLAY</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-230">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="caeb3-230">Display name</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-231">Указывает отображаемое имя сервера публикаций; требуется при <em> </em> использовании SWIPUBSVRHOST.</span><span class="sxs-lookup"><span data-stu-id="caeb3-231">Specifies the displayed name of the publishing server; required when <em>SWIPUBSVRHOST</em> is used.</span></span></p>
<p><span data-ttu-id="caeb3-232">Пример: <strong> SWIPUBSVRDISPLAY = &quot; производственная среда&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-232">Example: <strong>SWIPUBSVRDISPLAY=&quot;PRODUCTION ENVIRONMENT&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-233">SWIPUBSVRTYPE</span><span class="sxs-lookup"><span data-stu-id="caeb3-233">SWIPUBSVRTYPE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-234">[HTTP | Протокол</span><span class="sxs-lookup"><span data-stu-id="caeb3-234">[HTTP|RTSP]</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-235">Указывает тип сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="caeb3-235">Specifies the publishing server type.</span></span> <span data-ttu-id="caeb3-236">Тип сервера по умолчанию — сервер Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="caeb3-236">The default server type is Application Virtualization Server.</span></span> <span data-ttu-id="caeb3-237"><strong>Параметр/Secure </strong> не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="caeb3-237">The <strong>/secure</strong> switch is not case sensitive.</span></span></p>
<ul>
<li><p><span data-ttu-id="caeb3-238">HTTP (стандартный HTTP-сервер)</span><span class="sxs-lookup"><span data-stu-id="caeb3-238">HTTP—Standard HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="caeb3-239">HTTP- <strong> /Secure </strong> — Улучшенная безопасность HTTP-сервер</span><span class="sxs-lookup"><span data-stu-id="caeb3-239">HTTP <strong>/secure</strong>—Enhanced Security HTTP Server</span></span></p></li>
<li><p><span data-ttu-id="caeb3-240">RTSP (сервер Application Virtualization Server)</span><span class="sxs-lookup"><span data-stu-id="caeb3-240">RTSP—Application Virtualization Server</span></span></p></li>
<li><p><span data-ttu-id="caeb3-241">Протокол RTSP <strong> /Secure </strong> — сервер виртуализации приложений повышенной безопасности</span><span class="sxs-lookup"><span data-stu-id="caeb3-241">RTSP <strong>/secure</strong>—Enhanced Security Application Virtualization Server</span></span></p></li>
</ul>
<p><span data-ttu-id="caeb3-242">Пример: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-242">Example: <strong>SWIPUBSVRTYPE=&quot;HTTP /secure&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-243">SWIPUBSVRHOST</span><span class="sxs-lookup"><span data-stu-id="caeb3-243">SWIPUBSVRHOST</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-244">IP-адрес | имя узла</span><span class="sxs-lookup"><span data-stu-id="caeb3-244">IP address|host name</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-245">Указывает IP-адрес сервера виртуализации приложений или имени узла сервера, который разрешается в IP-адрес сервера&#39;s; требуется при <em> </em> использовании SWIPUBSVRDISPLAY.</span><span class="sxs-lookup"><span data-stu-id="caeb3-245">Specifies either the IP address of the Application Virtualization Server or a host name of the server that resolves into the server&#39;s IP address; required when <em>SWIPUBSVRDISPLAY</em> is used.</span></span></p>
<p><span data-ttu-id="caeb3-246">Пример: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-246">Example: <strong>SWIPUBSVRHOST=&quot;SERVER01&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-247">SWIPUBSVRPORT</span><span class="sxs-lookup"><span data-stu-id="caeb3-247">SWIPUBSVRPORT</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-248">Номер порта</span><span class="sxs-lookup"><span data-stu-id="caeb3-248">Port number</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-249">Задает логический порт, используемый этим сервером Application Virtualization для прослушивания запросов от клиента (по умолчанию = 554).</span><span class="sxs-lookup"><span data-stu-id="caeb3-249">Specifies the logical port that is used by this Application Virtualization Server to listen for requests from the client (default = 554).</span></span></p>
<ul>
<li><p><span data-ttu-id="caeb3-250">Стандартный HTTP-сервер — по умолчанию = 80.</span><span class="sxs-lookup"><span data-stu-id="caeb3-250">Standard HTTP server—Default = 80.</span></span></p></li>
<li><p><span data-ttu-id="caeb3-251">Сервер HTTP с улучшенной защитой: по умолчанию = 443.</span><span class="sxs-lookup"><span data-stu-id="caeb3-251">Enhanced Security HTTP Server—Default = 443.</span></span></p></li>
<li><p><span data-ttu-id="caeb3-252">Сервер Application Virtualization — значение по умолчанию = 554.</span><span class="sxs-lookup"><span data-stu-id="caeb3-252">Application Virtualization Server—Default = 554.</span></span></p></li>
<li><p><span data-ttu-id="caeb3-253">Сервер виртуализации приложений повышенной безопасности — по умолчанию = 322.</span><span class="sxs-lookup"><span data-stu-id="caeb3-253">Enhanced Security Application Virtualization Server—Default = 322.</span></span></p></li>
</ul>
<p><span data-ttu-id="caeb3-254">Пример: <strong> SWIPUBSVRPORT = &quot; 443&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-254">Example: <strong>SWIPUBSVRPORT=&quot;443&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-255">SWIPUBSVRPATH</span><span class="sxs-lookup"><span data-stu-id="caeb3-255">SWIPUBSVRPATH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-256">Имя пути</span><span class="sxs-lookup"><span data-stu-id="caeb3-256">Path name</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-257">Задает расположение на сервере публикации файла, в котором определяются сопоставления типов файлов (по умолчанию =/); требуется, если <em> </em> значение параметра SWIPUBSVRTYPE — HTTP.</span><span class="sxs-lookup"><span data-stu-id="caeb3-257">Specifies the location on the publishing server of the file that defines file type associations (default = /); required when the <em>SWIPUBSVRTYPE</em> parameter value is HTTP.</span></span></p>
<p><span data-ttu-id="caeb3-258">Пример: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-258">Example: <strong>SWIPUBSVRPATH=&quot;/AppVirt/appsntypes.xml&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-259">SWIPUBSVRREFRESH</span><span class="sxs-lookup"><span data-stu-id="caeb3-259">SWIPUBSVRREFRESH</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-260">[Вкл. | ВЫЙТИ</span><span class="sxs-lookup"><span data-stu-id="caeb3-260">[ON|OFF]</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-261">Указывает, будет ли клиент автоматически запрашивает сервер публикаций для сопоставлений типов файлов и приложений, когда пользователь входит на клиент (по умолчанию используется значение ON).</span><span class="sxs-lookup"><span data-stu-id="caeb3-261">Specifies whether the client automatically queries the publishing server for file type associations and applications when a user logs in to the client (default = ON).</span></span></p>
<p><span data-ttu-id="caeb3-262">Пример: <strong> SWIPUBSVRREFRESH = &quot; Off&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-262">Example: <strong>SWIPUBSVRREFRESH=&quot;off&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-263">SWIGLOBALDATA</span><span class="sxs-lookup"><span data-stu-id="caeb3-263">SWIGLOBALDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-264">Глобальный каталог данных</span><span class="sxs-lookup"><span data-stu-id="caeb3-264">Global data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-265">Указывает каталог, в котором будут храниться данные, не относящиеся к конкретным пользователям (по умолчанию — C:\Documents and Settings\All Users\Documents).</span><span class="sxs-lookup"><span data-stu-id="caeb3-265">Specifies the directory where data will be stored that is not specific to particular users (default = C:\Documents and Settings\All Users\Documents).</span></span></p>
<p><span data-ttu-id="caeb3-266">Пример: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-266">Example: <strong>SWIGLOBALDATA=&quot;D:\Microsoft Application Virtualization Client\Global&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-267">SWIUSERDATA</span><span class="sxs-lookup"><span data-stu-id="caeb3-267">SWIUSERDATA</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-268">Каталог данных пользователя</span><span class="sxs-lookup"><span data-stu-id="caeb3-268">User data directory</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-269">Указывает каталог, в котором будут храниться данные, специфичные для конкретных пользователей (по умолчанию =% APPDATA%).</span><span class="sxs-lookup"><span data-stu-id="caeb3-269">Specifies the directory where data will be stored that is specific to particular users (default = %APPDATA%).</span></span></p>
<p><span data-ttu-id="caeb3-270">Пример: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization (клиент)&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-270">Example: <strong>SWIUSERDATA=&quot;H:\Windows\Microsoft Application Virtualization Client&quot;</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-271">SWIFSDRIVE</span><span class="sxs-lookup"><span data-stu-id="caeb3-271">SWIFSDRIVE</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-272">Предпочтительная буква диска</span><span class="sxs-lookup"><span data-stu-id="caeb3-272">Preferred drive letter</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-273">Соответствует букве диска, выбранной для виртуального диска.</span><span class="sxs-lookup"><span data-stu-id="caeb3-273">Corresponds to the drive letter that you selected for the virtual drive.</span></span></p>
<p><span data-ttu-id="caeb3-274">Пример: <strong> SWIFSDRIVE = &quot; S&quot;</span><span class="sxs-lookup"><span data-stu-id="caeb3-274">Example: <strong>SWIFSDRIVE=&quot;S&quot;</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-275">SYSTEMEVENTLOGLEVEL</span><span class="sxs-lookup"><span data-stu-id="caeb3-275">SYSTEMEVENTLOGLEVEL</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-276">0 – 4</span><span class="sxs-lookup"><span data-stu-id="caeb3-276">0–4</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-277">Уровень ведения журнала, на котором сообщения журнала записываются в журнал событий NT.</span><span class="sxs-lookup"><span data-stu-id="caeb3-277">Indicates the logging level at which log messages are written to the NT event Log.</span></span> <span data-ttu-id="caeb3-278">Это значение указывает порог, который заносится в журнал, то есть все, что равно или меньше этого значения, заносится в журнал.</span><span class="sxs-lookup"><span data-stu-id="caeb3-278">The value indicates a threshold of what is logged—that is, everything equal to or less than that value is logged.</span></span> <span data-ttu-id="caeb3-279">Например, значение 0x3 (предупреждение) указывает на то, что в журнал записываются предупреждения (0x3), ошибки (0x2) и критические ошибки (0x1).</span><span class="sxs-lookup"><span data-stu-id="caeb3-279">For example, a value of 0x3 (Warning) indicates that Warnings (0x3), Errors (0x2), and Critical Errors (0x1) are logged.</span></span></p>
<p><span data-ttu-id="caeb3-280">Возможные значения:</span><span class="sxs-lookup"><span data-stu-id="caeb3-280">Possible values:</span></span></p>
<ul>
<li><p><span data-ttu-id="caeb3-281">0 = = нет</span><span class="sxs-lookup"><span data-stu-id="caeb3-281">0 == None</span></span></p></li>
<li><p><span data-ttu-id="caeb3-282">1 = = критическая</span><span class="sxs-lookup"><span data-stu-id="caeb3-282">1 == Critical</span></span></p></li>
<li><p><span data-ttu-id="caeb3-283">2 = = ошибка</span><span class="sxs-lookup"><span data-stu-id="caeb3-283">2 == Error</span></span></p></li>
<li><p><span data-ttu-id="caeb3-284">3 = = предупреждение</span><span class="sxs-lookup"><span data-stu-id="caeb3-284">3 == Warning</span></span></p></li>
<li><p><span data-ttu-id="caeb3-285">4 = = информация</span><span class="sxs-lookup"><span data-stu-id="caeb3-285">4 == Information</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em><span data-ttu-id="caeb3-286">MINFREESPACEMB</span><span class="sxs-lookup"><span data-stu-id="caeb3-286">MINFREESPACEMB</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-287">В МЕГАБАЙТах</span><span class="sxs-lookup"><span data-stu-id="caeb3-287">In MB</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-288">Задает объем свободного места (в мегабайтах), которое должно быть доступно на узле, прежде чем можно будет увеличивать размер кэша.</span><span class="sxs-lookup"><span data-stu-id="caeb3-288">Specifies the amount of free space (in megabytes) that must be available on the host before the cache size can increase.</span></span> <span data-ttu-id="caeb3-289">В следующем примере в клиенте настраивается наличие не менее 5 ГБ свободного места на диске, прежде чем можно будет увеличивать размер кэша.</span><span class="sxs-lookup"><span data-stu-id="caeb3-289">The following example would configure the client to ensure at least 5 GB of free space on the disk before allowing the size of the cache to increase.</span></span> <span data-ttu-id="caeb3-290">По умолчанию используется 5000 МБАЙТ свободного места на диске во время установки.</span><span class="sxs-lookup"><span data-stu-id="caeb3-290">The default is 5000 MB of free space available on disk at installation time.</span></span></p>
<p><span data-ttu-id="caeb3-291">Пример: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 ГБ)</span><span class="sxs-lookup"><span data-stu-id="caeb3-291">Example: <strong>MINFREESPACEMB =&quot;5000&quot; (5 GB)</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em><span data-ttu-id="caeb3-292">KEEPCURRENTSETTINGS</span><span class="sxs-lookup"><span data-stu-id="caeb3-292">KEEPCURRENTSETTINGS</span></span></em></p></td>
<td align="left"><p><span data-ttu-id="caeb3-293">[0 | 1]</span><span class="sxs-lookup"><span data-stu-id="caeb3-293">[0|1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="caeb3-294">Используется при применении параметров реестра перед развертыванием клиента (например, с помощью групповой политики).</span><span class="sxs-lookup"><span data-stu-id="caeb3-294">Used when you have applied registry settings prior to deploying a client—for example, by using Group Policy.</span></span> <span data-ttu-id="caeb3-295">При развертывании клиента установите для этого параметра значение 1, чтобы не перезаписывать параметры реестра.</span><span class="sxs-lookup"><span data-stu-id="caeb3-295">When a client is deployed, set this parameter to a value of 1 so that it will not overwrite the registry settings.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="caeb3-296">Важно.</span><span class="sxs-lookup"><span data-stu-id="caeb3-296">Important</span></span></strong><br/><p><span data-ttu-id="caeb3-297">Если задано значение 1, игнорируются следующие параметры командной строки установщика клиента:</span><span class="sxs-lookup"><span data-stu-id="caeb3-297">If set to a value of 1, the following client installer command-line parameters are ignored:</span></span></p>
<p><strong><span data-ttu-id="caeb3-298">SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , ICONSOURCEROOT, OSDSOURCEROOT, <strong> </strong> <strong> </strong> <strong> SYSTEMEVENTLOGLEVEL </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> , SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE и AUTOLOADTARGET.</span><span class="sxs-lookup"><span data-stu-id="caeb3-298">SWICACHESIZE</strong>, <strong>MINFREESPACEMB</strong>, <strong>ALLOWINDEPENDENTFILESTREAMING</strong>, <strong>APPLICATIONSOURCEROOT</strong>, <strong>ICONSOURCEROOT</strong>, <strong>OSDSOURCEROOT</strong>, <strong>SYSTEMEVENTLOGLEVEL</strong>, <strong>SWIGLOBALDATA</strong>, <strong>DOTIMEOUTMINUTES</strong>, <strong>SWIFSDRIVE</strong>, <strong>AUTOLOADTARGET</strong>, <strong>AUTOLOADTRIGGERS</strong>, and <strong>SWIUSERDATA</strong>.</span></span></p>
<p><span data-ttu-id="caeb3-299">Дополнительные сведения об установке этих значений после установки можно найти в разделе "Настройка параметров реестра клиента App-V с помощью командной строки" в руководстве по операциям Application Virtualization (App-V) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</span><span class="sxs-lookup"><span data-stu-id="caeb3-299">For further information about setting these values after installation, see “How to Configure the App-V Client Registry Settings by Using the Command Line” in the Application Virtualization (App-V) Operations Guide (<a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)">https://go.microsoft.com/fwlink/?LinkId=122939</a>).</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="caeb3-300">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="caeb3-300">Related topics</span></span>


[<span data-ttu-id="caeb3-301">Установка клиента Application Virtualization Client вручную</span><span class="sxs-lookup"><span data-stu-id="caeb3-301">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="caeb3-302">Обновление клиента Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="caeb3-302">How to Upgrade the Application Virtualization Client</span></span>](how-to-upgrade-the-application-virtualization-client.md)

[<span data-ttu-id="caeb3-303">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="caeb3-303">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)









