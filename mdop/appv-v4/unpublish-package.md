---
title: UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)
description: UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815132"
---
# UNPUBLISH PACKAGE (ОТМЕНИТЬ ПУБЛИКАЦИЮ ПАКЕТА)


Позволяет удалить сочетания клавиш и типы файлов для всего пакета.

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>Имя пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CLEAR</p></td>
<td align="left"><p>Если параметр указан, параметры пользователя также будут удалены. (Дополнительные сведения можно найти в разделе важное примечание ниже в этой статье.)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GLOBAL</p></td>
<td align="left"><p>Если он указан, пакет будет отменен для всех пользователей на этом компьютере.</p></td>
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

 

**Важно!**  Прежде чем можно будет выполнить команду **отмены публикации пакета** , пакет должен быть уже добавлен в клиент Application Virtualization.

Чтобы использовать **глобальную**программу, **отменить публикацию** , необходимо запустить ее от имени локального администратора. в противном случае требуется только разрешение **ClearApp** .

С помощью команды отменить **публикацию** в **глобальном шаблоне** удаляются все глобальные типы файлов и сочетания клавиш для пакета. **Очистка** неприменима.

Использование команды " **отменить публикацию** " без **глобального** удаления сочетаний клавиш и типов файлов для пакета и, если задано значение **clear** , приводит к удалению пользовательских настроек и остановке фоновой загрузки в контексте пользователя.

**Пакет отмены публикации** работает в приложениях с тем же именем пакета или GUID, который использовался в качестве идентификатора источника для **добавления**, **изменения**и **публикации пакета**.

Команда отменить **публикацию** всегда очищает все параметры пользователя, ярлыки и типы файлов независимо от использования переключателя/Clear.

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





