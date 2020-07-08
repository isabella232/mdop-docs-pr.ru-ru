---
title: PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)
description: PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815812"
---
# PUBLISH PACKAGE (ОПУБЛИКОВАТЬ ПАКЕТ)


Публикует содержимое всего пакета.

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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

 

**Важно!**  Пакет уже должен быть добавлен в клиент виртуализации приложений, а требуется файл манифеста.

Чтобы использовать **глобальный** параметр, команда "опубликовать пакет" должна быть запущена как локальный администратор; в противном случае требуются только разрешения **ManageTypes** и **PublishShortcut** .

Публикация без **глобального** параметра предоставляет пользователю доступ к приложениям в пакете и публикует типы файлов и ярлыки, указанные в манифесте, в профиль пользователя.

Публикация с **глобальным** параметром добавляет типы файлов и ярлыки, указанные в манифесте, в профиль "все пользователи".

Если пакет не является глобальным перед вызовом и используется **глобальный** параметр, пакет становится глобальным и доступен всем пользователям.

 

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





