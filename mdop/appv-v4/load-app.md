---
title: LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)
description: LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816249"
---
# LOAD APP (ЗАГРУЗИТЬ ПРИЛОЖЕНИЕ)


Загружает указанное приложение и все другие приложения в пакете в кэш файловой системы.

**Примечание**  Команда **загрузить приложение** запускает процесс загрузки, а индикатор выполнения отображается в области уведомлений на рабочем столе. Команда выполняется сразу после запуска этого процесса, поэтому все ошибки загрузки отображаются в одном и том же месте. Если вы хотите запустить процесс загрузки из командной строки, не используя область уведомлений на рабочем столе, используйте команду **загрузить пакет** .

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

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
<td align="left"><p>Имя и версия (необязательно) загружаемого приложения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Если задано, в поле "вывод" заносится указанное имя пути.</p></td>
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

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





