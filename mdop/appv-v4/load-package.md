---
title: LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)
description: LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816239"
---
# LOAD PACKAGE (ЗАГРУЗИТЬ ПАКЕТ)


Загружает заданный пакет в кэш файловой системы.

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Имя загружаемого пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/SFTPATH &lt; SFT — PathName&gt;</p></td>
<td align="left"><p>Указывает путь к SFT – файлу для загрузки.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Если задано, в поле "вывод" заносится указанное имя пути.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Если задано значение, выводится в окне консоли в активном состоянии (по умолчанию).</p></td>
</tr>
<tr class="odd">
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

 

**Примечание**  Если не указано ни одного SFTPATH, клиент загрузит пакет, используя путь, который он использует, на основании файла OSD, значения раздела реестра ApplicationSourceRoot или параметра OverrideURL.

Команда **загрузить пакет** выполняет синхронную загрузку и не будет завершена до полной загрузки пакета или до тех пор, пока не встретится условие ошибки.

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





