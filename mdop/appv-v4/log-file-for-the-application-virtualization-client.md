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
# Файл журнала для клиента Application Virtualization


В файле журнала для клиента Application Virtualization (App-V) захватывается подробная информация об условиях выполнения операций и ошибок. Его можно использовать при проверке функциональных возможностей и при устранении проблем.

При первом установке клиента App-V файл журнала создается по умолчанию в расположении, указанном в таблице ниже. Расположение файла журнала — это новая возможность для Application Virtualization (App-V) 4,5, но это расположение не будет изменяться, если клиент обновлен с более ранней версии.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя файла журнала</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>sftlog.txt</strong></p></td>
<td align="left"><p>Общие сведения об операциях и ошибках клиента App-V. Используйте этот журнал в качестве отправной точки для устранения ошибок в клиенте App-V.</p>
<p>Расположение файла журнала для настольного клиента или клиента служб удаленных рабочих столов (прежнее название — службы терминалов):</p>
<ul>
<li><p><em>Клиент Settings\All Users\Application Data\Microsoft\Application </em> : WindowsXP, Windows Server 2003</p></li>
<li><p><em>Клиент виртуализации C:\ProgramData\Microsoft\Application </em> : Windows Vista, Windows Server 2008</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Справка по клиенту Application Virtualization](application-virtualization-client-reference.md)

 

 





