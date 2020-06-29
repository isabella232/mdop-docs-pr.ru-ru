---
title: Настройка клиента для получения пакетов приложений
description: Настройка клиента для получения пакетов приложений
author: dansimp
ms.assetid: 891f2739-da7a-46da-b452-b8c0af075525
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5eeb0b977c6ecd44947d5d1c42d25d47b9e2530
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817829"
---
# <span data-ttu-id="7ebe9-103">Настройка клиента для получения пакетов приложений</span><span class="sxs-lookup"><span data-stu-id="7ebe9-103">How to Configure the Client for Application Package Retrieval</span></span>


<span data-ttu-id="7ebe9-104">Если клиент настроен на использование сервера управления Application Virtualization (App-V) в качестве сервера публикации, по умолчанию в следующем цикле обновления публикации клиент извлекает файлы дескриптора программного обеспечения (OSD) и манифеста пакета для каждого пакета, который пользователь уполномочен использовать.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-104">When the client is configured with an Application Virtualization (App-V) Management Server as its publishing server, by default at the next publishing refresh cycle, the client retrieves from the server the Open Software Descriptor (OSD) and package manifest files for each package that the user is authorized to use.</span></span> <span data-ttu-id="7ebe9-105">Клиент использует данные об источнике пакета, определенные в этих файлах, чтобы определить, где найти содержимое пакета, значки и сопоставления типов файлов.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-105">The client uses the package source information that is defined in these files to determine where to find the package content, icons, and file type associations.</span></span>

<span data-ttu-id="7ebe9-106">Если вы хотите, чтобы клиент получал содержимое пакета (SFT-файл) с локального серверного потокового или иного другого источника, такого как веб-сервер или файл на сервере, а не с сервера управления App-V, вы можете настроить значение раздела реестра ApplicationSourceRoot на компьютере таким образом, чтобы он указывал на локальную общую информацию о содержимом на другом сервере.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-106">If you want the client to obtain the package content (SFT file) from a local App-V Streaming Server or other alternate source such as a Web server or file server, instead of from the App-V Management Server, you can configure the ApplicationSourceRoot registry key value on the computer to point to the local content share on the other server.</span></span> <span data-ttu-id="7ebe9-107">Файл OSD по-прежнему определяет исходный исходный путь для содержимого пакета.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-107">The OSD file still defines the original source path for the package content.</span></span> <span data-ttu-id="7ebe9-108">Тем не менее, клиент использует значение параметра ApplicationSourceRoot вместо сервера и общего доступа, указанных в пути содержимого в OSD файле.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-108">However the client uses the value of the ApplicationSourceRoot setting in place of the server and share that are specified in the content path in the OSD file.</span></span> <span data-ttu-id="7ebe9-109">Это перенаправляет клиент для получения содержимого с другого сервера.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-109">This redirects the client to retrieve the content from the other server.</span></span>

<span data-ttu-id="7ebe9-110">Кроме того, вы можете настроить значения ключа реестра OSDSourceRoot и IconSourceRoot, если вы хотите переопределить эти параметры в файле манифеста пакета или пути, отправленные сервером публикации.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-110">You can also configure the OSDSourceRoot and IconSourceRoot registry key values if you want to override those settings in the package manifest file or in the paths sent by a publishing server.</span></span> <span data-ttu-id="7ebe9-111">OSDSourceRoot указывает местонахождение источника для извлечения файла OSD для пакета приложения во время публикации.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-111">The OSDSourceRoot specifies a source location for OSD file retrieval for an application package during publication.</span></span> <span data-ttu-id="7ebe9-112">IconSourceRoot указывает исходное расположение для получения значка для пакета приложения во время публикации.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-112">The IconSourceRoot specifies a source location for icon retrieval for an application package during publication.</span></span>

**<span data-ttu-id="7ebe9-113">Примечание.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-113">Note</span></span>**  
-   <span data-ttu-id="7ebe9-114">Параметры IconSourceRoot и OSDSourceRoot переопределяют значения в файле манифеста пакета, поэтому при попытке развернуть пакет с помощью метода файла установщика Windows (MSI) он также переопределит значения в файле манифеста пакета, который содержится в этом MSI-файле.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-114">The IconSourceRoot and OSDSourceRoot settings override the values in the package manifest file, so if you try to deploy a package by using the Windows Installer (.msi) file method, it will also override the values in the package manifest file that is contained within that .msi file.</span></span>

-   <span data-ttu-id="7ebe9-115">При выполнении операций публикации и передачи данных по HTTP (S) клиенты App-V 4,5 с пакетом обновления 1 (SP1) используют параметры прокси-сервера, настроенные в Internet Explorer на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-115">During both the publishing and HTTP(S) streaming operations,App-V 4.5 SP1 clients use the proxy server settings that are configured in Internet Explorer on the user’s computer.</span></span>



**<span data-ttu-id="7ebe9-116">Настройка значения раздела реестра ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7ebe9-116">To configure the ApplicationSourceRoot registry key value</span></span>**

-   <span data-ttu-id="7ebe9-117">Настройте ApplicationSourceRoot в следующем значении раздела реестра, указав либо путь UNC, либо URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-117">Configure the ApplicationSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="7ebe9-118">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7ebe9-118">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\ApplicationSourceRoot</span></span>

    <span data-ttu-id="7ebe9-119">Правильным форматом UNC-пути является **\\\\computername\\sharefolder\\\ [Folder \] \ [\ \ \]**, где **Папка** является необязательной.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-119">The correct format for the Universal Naming Convention (UNC) path is **\\\\computername\\sharefolder\\\[folder\]\[\\\]**, where **folder** is optional.</span></span> <span data-ttu-id="7ebe9-120">**ComputerName** может быть полным доменным именем (FQDN) или IP-адресом, а **sharefolder** — буквой диска.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-120">The **computername** can be a Fully Qualified Domain Name (FQDN) or an IP address, and **sharefolder** can be a drive letter.</span></span> <span data-ttu-id="7ebe9-121">Заменяется только часть **\\\\computername\\sharedfolder** или буква диска в пути OSD.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-121">Only the **\\\\computername\\sharedfolder** or drive letter portion of the OSD path is replaced.</span></span>

    <span data-ttu-id="7ebe9-122">Правильным форматом URL-пути является **протокол://ServerName: \ [Port \] \ [/path\] \ [/\]**, где **порт** и **путь** являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-122">The correct format for the URL path is **protocol://servername:\[port\]\[/path\]\[/\]**, where **port** and **path** are optional.</span></span> <span data-ttu-id="7ebe9-123">Если **порт** не указан, используется порт по умолчанию для протокола.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-123">If **port** is not specified, the default port for the protocol is used.</span></span> <span data-ttu-id="7ebe9-124">Заменяется только часть **Protocol://Server: Port** URL-адреса OSD.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-124">Only the **protocol://server:port** portion of the OSD URL is replaced.</span></span>

    **<span data-ttu-id="7ebe9-125">Важно.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-125">Important</span></span>**  
    <span data-ttu-id="7ebe9-126">Переменные среды не поддерживаются в определении ApplicationSourceRoot.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-126">Environment variables are not supported in the ApplicationSourceRoot definition.</span></span>



~~~
The following table lists examples of acceptable URL and UNC path formats.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ApplicationSourceRoot</th>
<th align="left">OSD File HREF Path</th>
<th align="left">Result</th>
<th align="left">Comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>https://mainserver:443/prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>https://mainserver:443/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322/prodapps</p></td>
<td align="left"><p>rtsp://%SFT_APPVSERVER%:554/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>rtsps://mainserver:322/prodapps/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="even">
<td align="left"><p>rtsps://mainserver:322</p></td>
<td align="left"><p>file://\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>rtsps://mainserver:322/productivity/office2k3.sft</p></td>
<td align="left"><p>‘\’ converted to ‘/’</p></td>
</tr>
<tr class="odd">
<td align="left"><p>\\uncserver\share</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="even">
<td align="left"><p>\\uncserver\share\prodapps</p></td>
<td align="left"><p>rtsp://appserver/productivity/office2k3.sft?customer=seq</p></td>
<td align="left"><p>\\uncserver\share\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p>‘/’ converted to ‘\’ and parameter dropped when converting to UNC path</p></td>
</tr>
<tr class="odd">
<td align="left"><p>M:</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>M:\prodapps</p></td>
<td align="left"><p>\\uncserver\share\productivity\office2k3.sft</p></td>
<td align="left"><p>M:\prodapps\productivity\office2k3.sft</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>
~~~



**<span data-ttu-id="7ebe9-127">Настройка значения OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7ebe9-127">To configure the OSDSourceRoot value</span></span>**

-   <span data-ttu-id="7ebe9-128">Настройте OSDSourceRoot в следующем значении раздела реестра, указав либо путь UNC, либо URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-128">Configure the OSDSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="7ebe9-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7ebe9-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\OSDSourceRoot</span></span>

    <span data-ttu-id="7ebe9-130">Допустимые форматы для OSDSourceRoot включают пути UNC и URL-адреса, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="7ebe9-130">Acceptable formats for the OSDSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="7ebe9-131">**\\\\computername\\sharefolder\\resource** или **\\\\computername\\content** или \*\* &lt; диск &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="7ebe9-131">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="7ebe9-132">**http://computername/productivity/**/**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="7ebe9-132">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

**<span data-ttu-id="7ebe9-133">Настройка значения IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7ebe9-133">To configure the IconSourceRoot value</span></span>**

-   <span data-ttu-id="7ebe9-134">Настройте IconSourceRoot в следующем значении раздела реестра, указав либо путь UNC, либо URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="7ebe9-134">Configure the IconSourceRoot in the following registry key value with either a UNC path or a URL:</span></span>

    <span data-ttu-id="7ebe9-135">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span><span class="sxs-lookup"><span data-stu-id="7ebe9-135">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\IconSourceRoot</span></span>

    <span data-ttu-id="7ebe9-136">Допустимые форматы для IconSourceRoot включают пути UNC и URL-адреса, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="7ebe9-136">Acceptable formats for the IconSourceRoot include UNC paths and URLs, as in the following example:</span></span>

    <span data-ttu-id="7ebe9-137">**\\\\computername\\sharefolder\\resource** или **\\\\computername\\content** или \*\* &lt; диск &gt; : \\foldername\*\*</span><span class="sxs-lookup"><span data-stu-id="7ebe9-137">**\\\\computername\\sharefolder\\resource** or **\\\\computername\\content** or **&lt;drive&gt;:\\foldername**</span></span>

    <span data-ttu-id="7ebe9-138">**http://computername/productivity/**/**https://computername/productivity/**</span><span class="sxs-lookup"><span data-stu-id="7ebe9-138">**http://computername/productivity/** or **https://computername/productivity/**</span></span>

## <span data-ttu-id="7ebe9-139">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="7ebe9-139">Related topics</span></span>


[<span data-ttu-id="7ebe9-140">Настройка параметров реестра клиента App-V с помощью командной строки</span><span class="sxs-lookup"><span data-stu-id="7ebe9-140">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)









