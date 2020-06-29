---
title: Выполнение задач DaRT с помощью команд PowerShell
description: Выполнение задач DaRT с помощью команд PowerShell
author: dansimp
ms.assetid: bc788b00-38c7-4f57-a832-916b68264d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f8ff87aa09555b93ca04a6ec7fa5dd4ba8504514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824302"
---
# <span data-ttu-id="f7174-103">Выполнение задач DaRT с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7174-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="f7174-104">Набор средств диагностики и восстановления Microsoft (DaRT) 8,0 содержит перечисленные ниже наборы командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7174-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="f7174-105">Администраторы могут использовать эти командлеты PowerShell для выполнения различных серверных задач DaRT 8,0 из командной строки, а не с помощью мастера DaRT Image Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7174-105">Administrators can use these PowerShell cmdlets to perform various DaRT 8.0 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="f7174-106">Управление DaRT с помощью команд PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7174-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="f7174-107">Используйте командлеты PowerShell, описанные здесь, для управления DaRT.</span><span class="sxs-lookup"><span data-stu-id="f7174-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7174-108">Имя</span><span class="sxs-lookup"><span data-stu-id="f7174-108">Name</span></span></th>
<th align="left"><span data-ttu-id="f7174-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f7174-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7174-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="f7174-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7174-111">Поменяет ISO-образ на CD, DVD или USB-накопитель.</span><span class="sxs-lookup"><span data-stu-id="f7174-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7174-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="f7174-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7174-113">Разрешает преобразование исходного WIM-файла, содержащего изображение DaRT, в файл ISO.</span><span class="sxs-lookup"><span data-stu-id="f7174-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7174-114">New-DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7174-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7174-115">Создает объект конфигурации DaRT, необходимый для применения набора инструментов DaRT к образу Windows.</span><span class="sxs-lookup"><span data-stu-id="f7174-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7174-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="f7174-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7174-117">Применяет объект DartConfiguration к подключенному образу Windows.</span><span class="sxs-lookup"><span data-stu-id="f7174-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="f7174-118">Сюда входит добавление всех файлов, конфигурации и зависимостей пакетов.</span><span class="sxs-lookup"><span data-stu-id="f7174-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f7174-119">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="f7174-119">Related topics</span></span>


[<span data-ttu-id="f7174-120">Администрирование DaRT 8.0 с помощью PowerShell</span><span class="sxs-lookup"><span data-stu-id="f7174-120">Administering DaRT 8.0 Using PowerShell</span></span>](administering-dart-80-using-powershell-dart-8.md)

 

 





