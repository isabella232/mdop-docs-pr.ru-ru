---
title: Выполнение задач DaRT с помощью команд PowerShell
description: Выполнение задач DaRT с помощью команд PowerShell
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822599"
---
# <span data-ttu-id="e1dd6-103">Выполнение задач DaRT с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1dd6-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="e1dd6-104">Набор средств диагностики и восстановления Microsoft (DaRT) 10 содержит перечисленные ниже наборы командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 10 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="e1dd6-105">Администраторы могут использовать эти командлеты PowerShell для выполнения различных задач, описанных в статье "DaRT 10 Server", из командной строки, а не с помощью мастера DaRT Recovery Image.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-105">Administrators can use these PowerShell cmdlets to perform various DaRT 10 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="e1dd6-106">Управление DaRT с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1dd6-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="e1dd6-107">Используйте командлеты PowerShell, описанные здесь, для управления DaRT.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e1dd6-108">Имя</span><span class="sxs-lookup"><span data-stu-id="e1dd6-108">Name</span></span></th>
<th align="left"><span data-ttu-id="e1dd6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e1dd6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e1dd6-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="e1dd6-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1dd6-111">Поменяет ISO-образ на CD, DVD или USB-накопитель.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e1dd6-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="e1dd6-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1dd6-113">Разрешает преобразование исходного WIM-файла, содержащего изображение DaRT, в файл ISO.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e1dd6-114">New-DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1dd6-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1dd6-115">Создает объект конфигурации DaRT, необходимый для применения набора инструментов DaRT к образу Windows.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e1dd6-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="e1dd6-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="e1dd6-117">Применяет объект DartConfiguration к подключенному образу Windows.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="e1dd6-118">Сюда входит добавление всех файлов, конфигурации и зависимостей пакетов.</span><span class="sxs-lookup"><span data-stu-id="e1dd6-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e1dd6-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="e1dd6-119">Related topics</span></span>


[<span data-ttu-id="e1dd6-120">Администрирование DaRT 10 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1dd6-120">Administering DaRT 10 Using PowerShell</span></span>](administering-dart-10-using-powershell.md)

 

 





