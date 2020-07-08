---
title: Файлы журнала программы Application Virtualization Sequencer
description: Файлы журнала программы Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816219"
---
# Файлы журнала программы Application Virtualization Sequencer


Файлы журнала для секвенсора Application Virtualization (App-V) содержат подробные сведения о последовательности приложений, и они могут быть полезны при проверке функциональности или при устранении проблем.

В таблице ниже приведены сведения о файлах журнала и их расположениях по умолчанию, которые создаются при использовании секвенсора.

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
<td align="left"><p><strong>sft-seq-log.txt</strong></p></td>
<td align="left"><p>Общие сведения о том, как поочередно приложит приложение. Используйте этот журнал в качестве отправной точки для устранения ошибок программы Sequencer.</p>
<p>Расположение файла журнала: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Значение маркера шаблона] Расположение файла журнала App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [значение маркера шаблона]</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>sftbt.txt</strong></p></td>
<td align="left"><p>Содержит сведения о задачах перезапуска компьютера, происходящих во время имитации перезапуска секвенсора.</p>
<p>Расположение файла журнала: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Значение маркера шаблона] Расположение файла журнала App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [значение маркера шаблона]</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>SftCallBack.txt</strong></p></td>
<td align="left"><p>Общие сведения о процессах, используемых при упорядочении.</p>
<p>Расположение файла журнала: <em> %WINDIR%\Microsoft Application Virtualization Sequencer\Logs</em></p>
<p>[Значение маркера шаблона] Расположение файла журнала App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [значение маркера шаблона]</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Справка по программе Application Virtualization Sequencer](application-virtualization-sequencer-reference.md)

 

 





