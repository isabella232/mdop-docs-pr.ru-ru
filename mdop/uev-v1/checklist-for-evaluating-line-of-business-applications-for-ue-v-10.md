---
title: Контрольный список для оценки бизнес-приложений для UE-V 1.0
description: Контрольный список для оценки бизнес-приложений для UE-V 1.0
author: dansimp
ms.assetid: 3bfaab30-59f7-4099-abb1-d248ce0086b8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 133bc5d195763b7281fd8d152e153231ac4c4d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826459"
---
# Контрольный список для оценки бизнес-приложений для UE-V 1.0


Для оценки того, какие бизнес-приложения должны быть включены в развертывание UE-V, учитывайте следующее:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Содержит ли приложение параметры, доступные пользователю для настройки?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Важно ли пользователю, что эти параметры перемещаются?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Параметры пользователя уже управляются решением политики управления приложениями или параметрами. UE-V применяет параметры приложения при запуске приложения и параметры Windows для событий входа, разблокировки и удаленного подключения. Если вы используете UE-V с другими решениями политики настройки, пользователи могут столкнуться с несогласованностью во всех перемещаемых параметрах.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Специфичны ли параметры приложения для компьютера? Настройки приложения и настройки, связанные с оборудованием или конкретными конфигурациями компьютера, не всегда перемещаются по сеансам и могут привести к плохому взаимодействию с приложением.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Параметры магазина приложений находятся в каталоге Program Files или в каталоге файлов, расположенном в <strong> каталоге Users </strong> \ [имя пользователя] \ <strong> AppData </strong>  \  <strong> LocalLow </strong> ? Данные приложения, которые хранятся в одном из этих расположений, обычно не должны перемещаться вместе с пользователем, так как эти данные являются специфическими для компьютера, или данные слишком велики для перемещения.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Сохраняет ли приложение все параметры в файле, которые содержат другие данные приложения, которые не должны перемещаться? UE-V синхронизирует файлы как единый блок. Если параметры хранятся в файлах, которые содержат данные приложения, отличные от параметров, то синхронизация этих дополнительных данных может привести к плохому взаимодействию с приложением.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Насколько велики файлы, содержащие параметры? Производительность синхронизации параметров может зависеть от больших файлов. Включение больших файлов может повлиять на производительность синхронизации параметров.</p></td>
</tr>
</tbody>
</table>

 

## Статьи по теме


[Планирование методов конфигурации UE-V](planning-for-ue-v-configuration-methods.md)

[Планирование UE-V 1.0](planning-for-ue-v-10.md)

 

 





