---
title: CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)
description: CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819379"
---
# CONFIGURE APP (НАСТРОИТЬ ПРИЛОЖЕНИЕ)


Позволяет пользователю изменить значок, связанный с приложением, но не обновляет значок для существующих ярлыков или сопоставлений типов файлов.

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>/ICON &lt; Icon (путь)&gt;</p></td>
<td align="left"><p>Путь или URL-адрес файла значка.</p></td>
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

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





