---
title: DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)
description: DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821702"
---
# DELETE OBJ (УДАЛИТЬ ОБЪЕКТ)


Удаляет все записи приложения.

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Если указано, удаляются все приложения. По умолчанию удаляются только те приложения, к которым у текущего пользователя есть доступ.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Если задано, в поле "вывод" заносится указанное имя пути.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Если указан, выводится диалоговое окно "вывод".</p></td>
</tr>
</tbody>
</table>

 

Для версии 4.6 добавлен следующий параметр.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Если задано значение, выводится имя указанного пути в формате Юникод.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





