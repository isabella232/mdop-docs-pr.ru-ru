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
# Выполнение задач DaRT с помощью команд PowerShell


Набор средств диагностики и восстановления Microsoft (DaRT) 10 содержит перечисленные ниже наборы командлетов Windows PowerShell. Администраторы могут использовать эти командлеты PowerShell для выполнения различных задач, описанных в статье "DaRT 10 Server", из командной строки, а не с помощью мастера DaRT Recovery Image.

## Управление DaRT с помощью команд PowerShell


Используйте командлеты PowerShell, описанные здесь, для управления DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Имя</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copy-DartImage</p></td>
<td align="left"><p>Поменяет ISO-образ на CD, DVD или USB-накопитель.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Export-DartImage</p></td>
<td align="left"><p>Разрешает преобразование исходного WIM-файла, содержащего изображение DaRT, в файл ISO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>New-DartConfiguration</p></td>
<td align="left"><p>Создает объект конфигурации DaRT, необходимый для применения набора инструментов DaRT к образу Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-DartImage</p></td>
<td align="left"><p>Применяет объект DartConfiguration к подключенному образу Windows. Сюда входит добавление всех файлов, конфигурации и зависимостей пакетов.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Администрирование DaRT 10 с помощью PowerShell](administering-dart-10-using-powershell.md)

 

 





