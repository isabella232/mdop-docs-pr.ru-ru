---
title: Вкладка "Шаблоны"
description: Вкладка "Шаблоны"
author: dansimp
ms.assetid: 5676e9f9-eb52-49e1-a55d-15c1059af368
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7469ee72eb23903ddec66152f8cc5d59861dfc9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820172"
---
# Вкладка "Шаблоны"


Вкладка " **шаблоны** "

-   Выводит список доступных шаблонов, которые можно использовать для создания новых объектов групповой политики (GPO).

-   Контекстное меню с командами для создания объекта групповой политики на основе выбранного шаблона, управления шаблонами и отображения отчетов для шаблонов.

-   Выводит список групп и пользователей, которые имеют разрешение на доступ к выбранному шаблону.

Поскольку шаблон не может быть изменен, шаблоны не имеют истории. Но, как и любая версия объекта групповой политики, параметры шаблона можно отобразить с помощью отчета о параметрах или по сравнению с другим GPO с отчетом о разнице.

**Примечание**  Шаблон — это нередактируемая статическая версия GPO, используемая в качестве отправной точки для создания новых редактируемых GPO.

 

При щелчке правой кнопкой мыши списка **объектов групповой политики** на этой вкладке отображается контекстное меню, в том числе один из указанных ниже вариантов.

## Элемент управления


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Команда</th>
<th align="left">Эффект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Новый управляемый объект групповой политики</strong></p></td>
<td align="left"><p>Создание нового объекта групповой политики на основе выбранного шаблона. В производственную среду предоставляется параметр для развертывания нового объекта групповой политики. Если у вас нет разрешения на создание объекта групповой политики, вам будет предложено отправить запрос. (Этот параметр отображается, если не выбран ни одного объекта групповой политики, если щелкнуть правой кнопкой мыши в области <strong> Список объектов групповой политики </strong> .)</p></td>
</tr>
</tbody>
</table>

 

## Отчеты


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Команда</th>
<th align="left">Эффект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Параметры</strong></p></td>
<td align="left"><p>Создание отчета на основе HTML или XML, в котором отображаются параметры выбранного объекта групповой политики.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Соответствия</strong></p></td>
<td align="left"><p>Создание отчета на основе HTML или XML для сравнения параметров в двух выбранных шаблонах GPO.</p></td>
</tr>
</tbody>
</table>

 

## Управление шаблонами


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Команда</th>
<th align="left">Эффект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Использовать по умолчанию</strong></p></td>
<td align="left"><p>Настройка выбранного шаблона в качестве используемого по умолчанию при создании нового объекта групповой политики.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Delete</strong></p></td>
<td align="left"><p>Переместить выбранный шаблон в <strong> корзину </strong> . Если у вас нет разрешения на удаление объекта групповой политики, вам будет предложено отправить запрос.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Rename</strong></p></td>
<td align="left"><p>Изменение имени выбранного шаблона.</p></td>
</tr>
</tbody>
</table>

 

## Прочее


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Команда</th>
<th align="left">Эффект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Обновить</strong></p></td>
<td align="left"><p>Обновите отображение консоли управления групповыми политиками, чтобы внести изменения. Некоторые изменения не видны до тех пор, пока не будет обновлено представление.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Help</strong></p></td>
<td align="left"><p>Вывести справку по расширенному управлению групповыми политиками.</p></td>
</tr>
</tbody>
</table>

 

### Дополнительные ссылки

-   [Вкладка "Содержимое"](contents-tab.md)

-   [Выполнение задач редактора](performing-editor-tasks.md)

-   [Выполнение задач рецензента](performing-reviewer-tasks.md)

 

 





