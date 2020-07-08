---
title: CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)
description: CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819349"
---
# CONFIGURE PACKAGE (НАСТРОИТЬ ПАКЕТ)


Позволяет пользователю изменить файл манифеста пакета, источник пакетов, типы триггеров загрузки или целевой объект загрузки для пакета.

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

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
<td align="left"><p>Путь или URL-адрес файла манифеста, в котором перечислены приложения, включенные в пакет, и все сведения о его публикации.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;URL-адрес/OVERRIDEURL&gt;</p></td>
<td align="left"><p>Расположение SFT-файла пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADNEVER</p></td>
<td align="left"><p>Фоновая загрузка выключена для пакета.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONREFRESH</p></td>
<td align="left"><p>Фоновая загрузка выполняется после обновления публикации.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/AUTOLOADONLOGIN</p></td>
<td align="left"><p>Фоновая загрузка выполняется, когда пользователь входит в систему.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/AUTOLOADONLAUNCH</p></td>
<td align="left"><p>Фоновая загрузка выполняется после того, как пользователь запустит приложение из пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Целевой объект/AUTOLOADTARGET&gt;</p></td>
<td align="left"><p>Указывает, какие приложения из пакета будут выгружены.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>НИЧЕГО</p></td>
<td align="left"><p>Ни один из автонагрузок не будет выполнен, несмотря на наличие флагов/AUTOLOADONxxx.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ВЕСЬ</p></td>
<td align="left"><p>Если включен триггер autoload, все приложения в пакете будут загружены в кэш независимо от того, были ли они запущены.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PREVUSED</p></td>
<td align="left"><p>Если включен триггер autoload, пакет будет загружаться, если какое-либо приложение ранее было запущено пользователем.</p></td>
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

 

Для версии 4.6 SP2 была добавлена следующая опция.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</p></td>
<td align="left"><p>Если задано значение "TRUE", для пакета создается параметр для одного пользователя или глобально, если указан флаг/GLOBAL.</p>
<p>Если для параметра установлено значение FALSE, значение реестра удаляется, а также переустанавливаются сопоставления типов файлов (FTA) для пакета.</p>
<p>Если не указано, происходит обычное поведение публикации по FTA и сочетаний клавиш. Если вы выполняете последующие операции обновления публикации в клиенте App-V 4,6 SP2, сочетания клавиш и FTAs для пакетов, для которых задан этот параметр реестра, не будут изменены, а сочетания клавиш и FTAs не будут регистрироваться при запуске системы или входе пользователя в систему, если не установить флажок.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Работает совместно с флагом/NO-UPDATE-FTA-SHORTCUT. Если присутствует флаг/GLOBAL, это означает, что для этого пакета будет создано значение реестра для всех пользователей. По умолчанию значение реестра создается только для этого пользователя.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





