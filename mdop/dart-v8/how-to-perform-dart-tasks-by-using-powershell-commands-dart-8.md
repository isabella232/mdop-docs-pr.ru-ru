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
# Выполнение задач DaRT с помощью команд PowerShell


Набор средств диагностики и восстановления Microsoft (DaRT) 8,0 содержит перечисленные ниже наборы командлетов Windows PowerShell. Администраторы могут использовать эти командлеты PowerShell для выполнения различных серверных задач DaRT 8,0 из командной строки, а не с помощью мастера DaRT Image Recovery.

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


[Администрирование DaRT 8.0 с помощью PowerShell](administering-dart-80-using-powershell-dart-8.md)

 

 





