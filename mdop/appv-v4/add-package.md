---
title: ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)
description: ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822399"
---
# ADD PACKAGE (ДОБАВИТЬ ПАКЕТ)


Добавляет запись пакета. Если пакет уже существует, эта команда обновит конфигурацию существующего пакета.

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Пакет: &lt; имя пакета&gt;</p></td>
<td align="left"><p>Имя пакета, отображаемое пользователем, и понятное.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Путь манифеста/manifest&gt;</p></td>
<td align="left"><p>Путь к файлу манифеста, в котором перечислены приложения, включенные в пакет, и все сведения о его публикации.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;URL-адрес/OVERRIDEURL&gt;</p></td>
<td align="left"><p>Расположение SFT-файла пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Фоновая загрузка выполняется после обновления публикации.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Фоновая загрузка выполняется, когда пользователь входит в систему.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Фоновая загрузка выполняется после того, как пользователь запустит приложение из пакета.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Целевой объект/AUTOLOADTARGET</p></td>
<td align="left"><p>Указывает, какие приложения из пакета будут выгружены.</p></td>
</tr>
<tr class="even">
<td align="left"><p>НИЧЕГО</p></td>
<td align="left"><p>Автозагрузка не будет выполнена, несмотря на наличие флагов/AUTOLOADONxxx.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ВЕСЬ</p></td>
<td align="left"><p>Если включен триггер autoload, все приложения в пакете будут загружены в кэш независимо от того, были ли они запущены ранее.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Если включен триггер autoload, пакет будет загружаться, если какое-либо приложение ранее было запущено пользователем.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Если он указан, пакет будет доступен для всех пользователей на этом компьютере.</p></td>
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

 

 





