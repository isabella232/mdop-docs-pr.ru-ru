---
title: Настройка работы ярлыков и сопоставлений типов файлов
description: Настройка работы ярлыков и сопоставлений типов файлов
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817912"
---
# <span data-ttu-id="77006-103">Настройка работы ярлыков и сопоставлений типов файлов</span><span class="sxs-lookup"><span data-stu-id="77006-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="77006-104">Ярлык и Политика публикации сопоставления типов файлов (FTA) определяются и контролируются XML-файлом публикации, который отправляется клиентам на сервере публикации во время операции обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="77006-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="77006-105">Когда клиент получает эти данные, он добавляет любые новые опубликованные данные о таких приложениях, как значки и FTAs.</span><span class="sxs-lookup"><span data-stu-id="77006-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="77006-106">Затем удаляются все устаревшие данные публикации.</span><span class="sxs-lookup"><span data-stu-id="77006-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="77006-107">В приложении App-V версии 4,6 определено два значения ключа реестра, позволяющие администраторам управлять этим поведением.</span><span class="sxs-lookup"><span data-stu-id="77006-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="77006-108">По умолчанию сочетания клавиш, создаваемые локально с помощью клиентской консоли, теперь сохраняются.</span><span class="sxs-lookup"><span data-stu-id="77006-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="77006-109">Изменение сочетания клавиш и поведения FTA</span><span class="sxs-lookup"><span data-stu-id="77006-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="77006-110">Для раздела реестра Configuration ("FileTypePolicy") и "ShortcutPolicy" (параметры клиента) заданы два новых значения реестра DWORD.</span><span class="sxs-lookup"><span data-stu-id="77006-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="77006-111">Эти значения реестра DWORD по умолчанию не отображаются, но их можно добавить вручную.</span><span class="sxs-lookup"><span data-stu-id="77006-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="77006-112">Раздел реестра "Конфигурация" находится на странице HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="77006-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="77006-113">В приведенной ниже таблице указаны четыре значения политики, которые применяются к обоим значениям раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="77006-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="77006-114">Ниже приведен список числовых значений для параметров реестра и поведение, применяемое к типам файлов или сочетаниям клавиш в операции обновления публикации.</span><span class="sxs-lookup"><span data-stu-id="77006-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="77006-115">Имя</span><span class="sxs-lookup"><span data-stu-id="77006-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-116">Тип</span><span class="sxs-lookup"><span data-stu-id="77006-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-117">Данные (примеры)</span><span class="sxs-lookup"><span data-stu-id="77006-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-118">Описание</span><span class="sxs-lookup"><span data-stu-id="77006-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="77006-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="77006-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="77006-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-121">По умолчанию = 0x2 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="77006-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-122">(0x0) — "ClientOnly" — Удаление существующих элементов из одного источника сведений о публикации и сохранение только тех элементов, которые были добавлены локально</span><span class="sxs-lookup"><span data-stu-id="77006-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="77006-123">(0x1) — "ServerOnly" — Удаление устаревших элементов из одного и того же источника сведений о публикации и всех элементов, добавленных на локальном компьютере, и добавление новых элементов.</span><span class="sxs-lookup"><span data-stu-id="77006-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="77006-124">(0x2) — "ClientAndServer" — Удаление устаревших элементов из одного и того же источника данных публикации, сохранение элементов на локальном экране и добавление новых элементов (по умолчанию, если отсутствует для App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="77006-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="77006-125">(0x3) — "без изменений" — не изменять типы файлов и сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="77006-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="77006-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="77006-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="77006-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-128">По умолчанию = 0x2</span><span class="sxs-lookup"><span data-stu-id="77006-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="77006-129">(0x0) — "ClientOnly" — Удаление существующих элементов из одного источника сведений о публикации и сохранение только элементов, добавленных локально</span><span class="sxs-lookup"><span data-stu-id="77006-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="77006-130">(0x1) — "ServerOnly" — Удаление устаревших элементов из одного и того же источника сведений о публикации и всех элементов, добавленных на локальном компьютере, и добавление новых элементов</span><span class="sxs-lookup"><span data-stu-id="77006-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="77006-131">(0x2) — "ClientAndServer" — Удаление устаревших элементов из одного и того же источника сведений о публикации, сохранение элементов на локальном экране и добавление новых элементов (по умолчанию, если не отображается)</span><span class="sxs-lookup"><span data-stu-id="77006-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="77006-132">(0x3) — "без изменений" — не изменять типы файлов и сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="77006-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="77006-133">**Примечание**  Текстовые значения ссылаются на значения для атрибутов XML в XML-файле публикации.</span><span class="sxs-lookup"><span data-stu-id="77006-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="77006-134">Вы можете настроить эти значения вручную, если вы реализовали пользовательское решение для публикации по HTTP.</span><span class="sxs-lookup"><span data-stu-id="77006-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





