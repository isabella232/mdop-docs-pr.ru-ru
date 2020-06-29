---
title: Файл журнала для клиента Application Virtualization
description: Файл журнала для клиента Application Virtualization
author: dansimp
ms.assetid: ac4b3e4a-a220-4c06-bd60-af7dc318b3a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 52908aa583d3d673b8a229df14e56f1c71633ef4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816229"
---
# <span data-ttu-id="8f7bc-103">Файл журнала для клиента Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8f7bc-103">Log File for the Application Virtualization Client</span></span>


<span data-ttu-id="8f7bc-104">В файле журнала для клиента Application Virtualization (App-V) захватывается подробная информация об условиях выполнения операций и ошибок.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-104">The log file for the Application Virtualization (App-V) Client captures detailed information about operations and error conditions.</span></span> <span data-ttu-id="8f7bc-105">Его можно использовать при проверке функциональных возможностей и при устранении проблем.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-105">You can use it when you are verifying functionality and when you are troubleshooting issues.</span></span>

<span data-ttu-id="8f7bc-106">При первом установке клиента App-V файл журнала создается по умолчанию в расположении, указанном в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-106">When the App-V Client is first installed, the log file is created by default in the location shown in the following table.</span></span> <span data-ttu-id="8f7bc-107">Расположение файла журнала — это новая возможность для Application Virtualization (App-V) 4,5, но это расположение не будет изменяться, если клиент обновлен с более ранней версии.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-107">The location of the log file is new for Application Virtualization (App-V) 4.5, although the location will not be changed if the client is upgraded from an earlier version.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8f7bc-108">Имя файла журнала</span><span class="sxs-lookup"><span data-stu-id="8f7bc-108">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="8f7bc-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8f7bc-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="8f7bc-110">sftlog.txt</span><span class="sxs-lookup"><span data-stu-id="8f7bc-110">sftlog.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="8f7bc-111">Общие сведения об операциях и ошибках клиента App-V.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-111">Provides general information about App-V Client operations and errors.</span></span> <span data-ttu-id="8f7bc-112">Используйте этот журнал в качестве отправной точки для устранения ошибок в клиенте App-V.</span><span class="sxs-lookup"><span data-stu-id="8f7bc-112">Use this log as a starting point for troubleshooting App-V Client errors.</span></span></p>
<p><span data-ttu-id="8f7bc-113">Расположение файла журнала для настольного клиента или клиента служб удаленных рабочих столов (прежнее название — службы терминалов):</span><span class="sxs-lookup"><span data-stu-id="8f7bc-113">Log file location for either the Desktop Client or the Client for Remote Desktop Services (formerly Terminal Services):</span></span></p>
<ul>
<li><p><em><span data-ttu-id="8f7bc-114">Клиент Settings\All Users\Application Data\Microsoft\Application </em> : WindowsXP, Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f7bc-114">C:\Documents and Settings\All Users\Application Data\Microsoft\Application Virtualization Client</em>: WindowsXP, Windows Server 2003</span></span></p></li>
<li><p><em><span data-ttu-id="8f7bc-115">Клиент виртуализации C:\ProgramData\Microsoft\Application </em> : Windows Vista, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f7bc-115">C:\ProgramData\Microsoft\Application Virtualization Client</em>: Windows Vista, Windows Server 2008</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8f7bc-116">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="8f7bc-116">Related topics</span></span>


[<span data-ttu-id="8f7bc-117">Справка по клиенту Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="8f7bc-117">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





