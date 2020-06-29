---
title: CONFIGURE TYPE (НАСТРОИТЬ ТИП)
description: CONFIGURE TYPE (НАСТРОИТЬ ТИП)
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821939"
---
# CONFIGURE TYPE (НАСТРОИТЬ ТИП)


Позволяет пользователю изменять параметры сопоставления типов файлов.

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Тип: &lt; расширение файла&gt;</p></td>
<td align="left"><p>Расширение имени файла, которое нужно настроить.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Приложение/App&gt;</p></td>
<td align="left"><p>Имя и версия (необязательно) приложения, которым нужно сопоставить этот тип файлов. Не может быть указан с PROGID.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/ICON &lt; Icon (путь)&gt;</p></td>
<td align="left"><p>Путь или URL-адрес файла значка.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Тип/Description — DESC&gt;</p></td>
<td align="left"><p>Удобное для пользователя имя типа файлов.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Тип содержимого/Content-Type&gt;</p></td>
<td align="left"><p>Тип содержимого файла.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Если задано значение, это означает, что необходимо изменить связь, которая применяется ко всем пользователям, а не для конкретного пользователя.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; распознанный тип&gt;</p></td>
<td align="left"><p>Воспринимаемый тип файла.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Идентификатор ProgID/ProgID&gt;</p></td>
<td align="left"><p>Указывает, что расширение должно быть связано с другим типом файла. Предыдущий тип файлов не удаляется. Не может быть указан с помощью приложения, ЗНАЧКа, описания, CONFIRMOPEN или SHOWEXT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Указывает, должны ли пользователи загружать файл этого типа получать запросы на открытие или сохранение файла.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Указывает, должно ли расширение файла всегда отображаться, даже если пользователь запрашивает, чтобы все расширения были скрыты.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Указывает, следует ли добавить запись в меню "создать" <strong> оболочки </strong> .</p></td>
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

 

 





