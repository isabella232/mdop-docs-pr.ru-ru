---
title: ADD SERVER (ДОБАВИТЬ СЕРВЕР)
description: ADD SERVER (ДОБАВИТЬ СЕРВЕР)
author: dansimp
ms.assetid: 4be2ac2e-a410-4711-9f84-f305393c8fa7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e15a5943b40e14b2f9031bf8b3ddffa693e32dea
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819889"
---
# ADD SERVER (ДОБАВИТЬ СЕРВЕР)


Добавляет сервер публикаций.

`SFTMIME ADD SERVER:server-name /HOST hostname /TYPE {HTTP|RTSP}                 /PATH path [/PORT port] [/REFRESH {ON|OFF}] [/SECURE]                 [/LOG log-pathname | /CONSOLE | /GUI]`

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
<td align="left"><p>СЕРВЕР: &lt; имя сервера&gt;</p></td>
<td align="left"><p>Отображаемое имя сервера публикаций.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;HostName (имя узла)/Host&gt;</p></td>
<td align="left"><p>Имя узла или IP-адрес сервера публикаций.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/TYPE {HTTP | Протокол</p></td>
<td align="left"><p>Указывает, является ли сервер публикаций веб-сервером ( &quot; HTTP &quot; ) или сервером Application Virtualization ( &quot; RTSP &quot; ).</p></td>
</tr>
<tr class="even">
<td align="left"><p>/PORT &lt; порт&gt;</p></td>
<td align="left"><p>Порт, прослушиваемый сервером публикаций. По умолчанию используется 80 для обычных HTTP-серверов, 443 для HTTP-серверов, использующих повышенную безопасность, 554 для обычных серверов виртуализации приложений и 322 для серверов с повышенной безопасностью.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/PATH &lt; путь&gt;</p></td>
<td align="left"><p>Часть пути URL-адреса, используемая в запросе на публикацию. Если для параметра TYPE задано значение RTSP, путь является необязательным и по умолчанию используется &quot; / &quot; .</p></td>
</tr>
<tr class="even">
<td align="left"><p>/REFRESH</p></td>
<td align="left"><p>Если установлено значение ON, сведения о публикации будут обновляться, когда пользователь входит в систему. По умолчанию: вкл.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/SECURE</p></td>
<td align="left"><p>Если указано, это означает, что для сервера публикаций должно быть установлено подключение с повышенной безопасностью.</p></td>
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

 

 





