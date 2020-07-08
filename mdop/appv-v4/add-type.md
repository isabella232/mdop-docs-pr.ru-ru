---
title: ADD TYPE (ДОБАВИТЬ ТИП)
description: ADD TYPE (ДОБАВИТЬ ТИП)
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822382"
---
# ADD TYPE (ДОБАВИТЬ ТИП)


Добавляет указанную ассоциацию типов файлов.

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Расширение имени файла, которое будет сопоставлено указанному приложению.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Приложение/App&gt;</p></td>
<td align="left"><p>Имя и версия (необязательно) приложения.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/ICON &lt; Icon (путь)&gt;</p></td>
<td align="left"><p>Путь или URL-адрес файла значка.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Тип/Description — DESC&gt;</p></td>
<td align="left"><p>Удобное для пользователя имя типа файлов. По умолчанию — &quot; файл расширения.&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;Тип содержимого/Content-Type&gt;</p></td>
<td align="left"><p>Тип содержимого файла. По умолчанию &quot; — расширение Application/Softricity.&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Если он указан, пакет будет доступен для всех пользователей на этом компьютере.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PERCEIVED-TYPE &lt; распознанный тип&gt;</p></td>
<td align="left"><p>Воспринимаемый тип файла. Значение по умолчанию — Nothing.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Идентификатор ProgID/ProgID&gt;</p></td>
<td align="left"><p>Программный идентификатор для типа файла. По умолчанию — приложение virt. расширение. File.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/CONFIRMOPEN</p></td>
<td align="left"><p>Указывает, должны ли пользователи загружать файл этого типа получать запросы на открытие или сохранение файла. По умолчанию используется значение Да.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SHOWEXT</p></td>
<td align="left"><p>Указывает, должно ли расширение файла всегда отображаться, даже если пользователь запрашивает, чтобы все расширения были скрыты. По умолчанию — нет.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/NEWMENU</p></td>
<td align="left"><p>Указывает, следует ли добавить запись в меню "создать" <strong> оболочки </strong> . По умолчанию — нет.</p></td>
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

 

 





