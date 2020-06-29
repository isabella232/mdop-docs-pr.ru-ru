---
title: ADD SERVER (ДОБАВИТЬ СЕРВЕР)
description: ADD SERVER (ДОБАВИТЬ СЕРВЕР)
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819889"
---
# <span data-ttu-id="721d6-103">ADD SERVER (ДОБАВИТЬ СЕРВЕР)</span><span class="sxs-lookup"><span data-stu-id="721d6-103">ADD SERVER</span></span>


<span data-ttu-id="721d6-104">Добавляет сервер публикаций.</span><span class="sxs-lookup"><span data-stu-id="721d6-104">Adds a publishing server.</span></span>

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="721d6-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="721d6-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="721d6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="721d6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="721d6-107">СЕРВЕР: &lt; имя сервера&gt;</span><span class="sxs-lookup"><span data-stu-id="721d6-107">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-108">Отображаемое имя сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="721d6-108">The display name for the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="721d6-109">&lt;HostName (имя узла)/Host&gt;</span><span class="sxs-lookup"><span data-stu-id="721d6-109">/HOST &lt;hostname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-110">Имя узла или IP-адрес сервера публикаций.</span><span class="sxs-lookup"><span data-stu-id="721d6-110">The host name or IP address for the publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="721d6-111">/TYPE {HTTP | Протокол</span><span class="sxs-lookup"><span data-stu-id="721d6-111">/TYPE {HTTP|RTSP}</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-112">Указывает, является ли сервер публикаций веб-сервером ( &quot; HTTP &quot; ) или сервером Application Virtualization ( &quot; RTSP &quot; ).</span><span class="sxs-lookup"><span data-stu-id="721d6-112">Indicates whether the publishing server is a Web server (&quot;HTTP&quot;) or an Application Virtualization Server (&quot;RTSP&quot;).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="721d6-113">/PORT &lt; порт&gt;</span><span class="sxs-lookup"><span data-stu-id="721d6-113">/PORT &lt;port&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-114">Порт, прослушиваемый сервером публикаций.</span><span class="sxs-lookup"><span data-stu-id="721d6-114">The port on which the publishing server listens.</span></span> <span data-ttu-id="721d6-115">По умолчанию используется 80 для обычных HTTP-серверов, 443 для HTTP-серверов, использующих повышенную безопасность, 554 для обычных серверов виртуализации приложений и 322 для серверов с повышенной безопасностью.</span><span class="sxs-lookup"><span data-stu-id="721d6-115">Defaults to 80 for normal HTTP servers, 443 for HTTP servers using enhanced security, 554 for normal Application Virtualization Servers, and 322 for servers using enhanced security.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="721d6-116">/PATH &lt; путь&gt;</span><span class="sxs-lookup"><span data-stu-id="721d6-116">/PATH &lt;path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-117">Часть пути URL-адреса, используемая в запросе на публикацию.</span><span class="sxs-lookup"><span data-stu-id="721d6-117">The path portion of the URL used in a publishing request.</span></span> <span data-ttu-id="721d6-118">Если для параметра TYPE задано значение RTSP, путь является необязательным и по умолчанию используется &quot; / &quot; .</span><span class="sxs-lookup"><span data-stu-id="721d6-118">If the TYPE parameter is set to RTSP, the path is optional and defaults to &quot;/&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="721d6-119">/REFRESH</span><span class="sxs-lookup"><span data-stu-id="721d6-119">/REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-120">Если установлено значение ON, сведения о публикации будут обновляться, когда пользователь входит в систему.</span><span class="sxs-lookup"><span data-stu-id="721d6-120">If set to ON, publishing information will be refreshed when the user logs in.</span></span> <span data-ttu-id="721d6-121">По умолчанию: вкл.</span><span class="sxs-lookup"><span data-stu-id="721d6-121">Defaults to ON.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="721d6-122">/SECURE</span><span class="sxs-lookup"><span data-stu-id="721d6-122">/SECURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-123">Если указано, это означает, что для сервера публикаций должно быть установлено подключение с повышенной безопасностью.</span><span class="sxs-lookup"><span data-stu-id="721d6-123">If present, indicates that a connection with enhanced security should be established to the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="721d6-124">/LOG</span><span class="sxs-lookup"><span data-stu-id="721d6-124">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-125">Если задано, в поле "вывод" заносится указанное имя пути.</span><span class="sxs-lookup"><span data-stu-id="721d6-125">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="721d6-126">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="721d6-126">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-127">Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="721d6-127">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="721d6-128">/GUI</span><span class="sxs-lookup"><span data-stu-id="721d6-128">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-129">Если указан, выводится диалоговое окно "вывод".</span><span class="sxs-lookup"><span data-stu-id="721d6-129">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="721d6-130">Для версии 4.6 добавлен следующий параметр.</span><span class="sxs-lookup"><span data-stu-id="721d6-130">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="721d6-131">/LOGU</span><span class="sxs-lookup"><span data-stu-id="721d6-131">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="721d6-132">Если задано значение, выводится имя указанного пути в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="721d6-132">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="721d6-133">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="721d6-133">Related topics</span></span>


[<span data-ttu-id="721d6-134">Справочник по командам SFTMIME</span><span class="sxs-lookup"><span data-stu-id="721d6-134">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





