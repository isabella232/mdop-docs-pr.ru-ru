---
title: Функции вкладки "Содержимое"
description: Функции вкладки "Содержимое"
author: dansimp
ms.assetid: 725f025a-c30a-4d07-add1-4e0ed9a1a5fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f64aad16a3335d78641812121692f6d5f6436ee1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818909"
---
# Функции вкладки "Содержимое"


Каждая вспомогательная вкладка на вкладке " **содержимое** " состоит из двух разделов:**объектов групповой политики** и **групп и пользователей**.

## Раздел "объекты групповой политики"


Раздел " **объекты групповой политики** " отображает отфильтрованный список объектов групповой политики (GPO) и определяет указанные ниже атрибуты для каждого GPO.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Атрибут GPO</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Name</strong></p></td>
<td align="left"><p>Имя объекта групповой политики.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Состояние</strong></p></td>
<td align="left"><p>Состояние выбранного объекта групповой политики</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Кем изменено</strong></p></td>
<td align="left"><p>Редактор, который вернул или утверждающий, который развернул выбранный объект групповой политики.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Изменить дату</strong></p></td>
<td align="left"><p>Для управляемого объекта групповой политики: самая поздняя дата, когда она была возвращена после изменения или извлечения для изменения. Для неконтрольного объекта групповой политики — Дата последнего изменения.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Comment</strong></p></td>
<td align="left"><p>Примечание, введенное пользователем, который вернул или развернул объект групповой политики на момент его изменения. Полезен для выявления конкретных версий в случае необходимости возврата к предыдущей версии.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Версия компьютера</strong></p></td>
<td align="left"><p>Автоматически созданная версия части объекта групповой политики на компьютере.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Пользовательская версия</strong></p></td>
<td align="left"><p>Автоматически созданная версия части объекта групповой политики пользователя.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Состояние объекта групповой политики</strong></p></td>
<td align="left"><p>Конфигурацию компьютера и конфигурацию пользователя можно управлять отдельно. Состояние GPO показывает, какие части объекта групповой политики включены.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Фильтр WMI</strong></p></td>
<td align="left"><p>Отобразить все фильтры WMI, примененные к этому объекту групповой политики. Фильтры WMI управляются в <strong> папке "фильтры WMI" </strong> для домена в дереве консоли консоли управления групповыми политиками.</p></td>
</tr>
</tbody>
</table>

 

## Раздел групп и пользователей


При выборе объекта групповой политики в разделе **группы и пользователи** отображается список групп и пользователей, имеющих доступ к этому объекту групповой политики. Разрешенные разрешения и наследование отображаются для каждой группы или пользователя. Администратор РАСШИРЕНного доступа может настраивать разрешения с помощью стандартных ролей (редактор, утверждающий, рецензент и администратор РАСШИРЕНного доступа) или настроенного сочетания разрешений.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Кнопка</th>
<th align="left">Эффект</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Add</strong></p></td>
<td align="left"><p>Добавьте новую запись в дескриптор безопасности. Вы можете добавить пользователя или группу в службе каталогов Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Удалить</strong></p></td>
<td align="left"><p>Удаление выделенного элемента из списка управления доступом.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Свойства</strong></p></td>
<td align="left"><p>Отображение свойств выбранного объекта. На странице "Свойства" отображается один и тот же объект в окне " <strong> Пользователи и компьютеры Active Directory" </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Дополнительно</strong></p></td>
<td align="left"><p>Откройте <strong> Редактор списка управления доступом </strong> .</p></td>
</tr>
</tbody>
</table>

 

### Дополнительные рекомендации

-   Сведения о ролях и разрешениях, связанных с определенными задачами, можно найти в разделе [выполнение задач администратора расширенного администрирования](performing-agpm-administrator-tasks-agpm30ops.md), [выполнение задач редактора](performing-editor-tasks-agpm30ops.md), [выполнение задач утверждающего](performing-approver-tasks-agpm30ops.md)и [выполнение задач рецензента](performing-reviewer-tasks-agpm30ops.md).

### Дополнительные ссылки

-   [Вкладка "Содержимое"](contents-tab-agpm30ops.md)

 

 





