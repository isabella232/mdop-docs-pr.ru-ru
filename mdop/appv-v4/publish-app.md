---
title: PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)
description: PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815819"
---
# PUBLISH APP (ОПУБЛИКОВАТЬ ПРИЛОЖЕНИЕ)


Публикация ярлыка приложения в меню "Пуск", рабочем столе или другом указанном месте.

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Приложение: &lt; приложение&gt;</p></td>
<td align="left"><p>Имя и версия (необязательно) приложения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/DESKTOP</p></td>
<td align="left"><p>Публикация ярлыка на рабочем столе пользователя.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/START</p></td>
<td align="left"><p>Публикация ярлыка в папке приложения Application Virtualization в папке программы в меню "Пуск".</p></td>
</tr>
<tr class="even">
<td align="left"><p>/TARGET &lt; Target-Path&gt;</p></td>
<td align="left"><p>Абсолютный путь к папке, в которой нужно опубликовать ярлык.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/ICON &lt; Icon (путь)&gt;</p></td>
<td align="left"><p>Путь или URL-адрес файла значка.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Отображаемое имя/Display&gt;</p></td>
<td align="left"><p>Отображаемое имя ярлыка.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/ARGS &lt; Command-args&gt;</p></td>
<td align="left"><p>Параметры, передаваемые приложению.</p></td>
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

 

 





