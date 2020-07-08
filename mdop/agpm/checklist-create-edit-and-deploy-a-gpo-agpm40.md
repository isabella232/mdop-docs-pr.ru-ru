---
title: Контрольный список для создания, изменения и развертывания объекта групповой политики
description: Контрольный список для создания, изменения и развертывания объекта групповой политики
author: dansimp
ms.assetid: 44631bed-16d2-4b5a-af70-17a73fb5f6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d8bea9109040aa81a20df62356ef1d307d5eac0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819102"
---
# Контрольный список: создание, редактирование и развертывание объекта групповой политики


В среде, в которой несколько пользователей изменяют объекты групповой политики (GPO) с помощью расширенного управления групповыми политиками (режимом MARS), администраторы РАСШИРЕНного доступа (полный доступ) делегируют разрешение на редакторы, утверждающие и рецензенты либо в виде групп, либо в качестве отдельных пользователей. Ниже приведен типичный процесс разработки объектов групповой политики для редактора и утверждающего.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Справочные материалы</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Редактор запрашивает создание нового объекта групповой политики или утверждающего создает новый объект групповой политики.</p></td>
<td align="left"><p><a href="request-the-creation-of-a-new-controlled-gpo-agpm40.md" data-raw-source="[Request the Creation of a New Controlled GPO](request-the-creation-of-a-new-controlled-gpo-agpm40.md)">Запрос на создание нового управляемого объекта групповой политики</a></p>
<p><a href="create-a-new-controlled-gpo-agpm40.md" data-raw-source="[Create a New Controlled GPO](create-a-new-controlled-gpo-agpm40.md)">Создание нового управляемого объекта групповой политики</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Утверждающее лицо утверждает создание объекта групповой политики, если оно было запрошено редактором.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Утверждение или отклонение ожидающего действия</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Редактор извлекает из архива копию объекта групповой политики, чтобы никто из них не мог изменить объект групповой политики. Редактор вносит изменения в объект групповой политики, а затем проверяет измененный объект GPO в архив.</p></td>
<td align="left"><p><a href="edit-a-gpo-offline-agpm40.md" data-raw-source="[Edit a GPO Offline](edit-a-gpo-offline-agpm40.md)">Изменение объекта групповой политики в автономном режиме</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>При разработке в тестовом лесе редактор экспортирует объект групповой политики в файл, передает файл в производственный лес и импортирует файл. Кроме того, редактор может связать GPO с подразделением, содержащим тестовые компьютеры и пользователей.</p></td>
<td align="left"><p><a href="using-a-test-environment.md" data-raw-source="[Using a Test Environment](using-a-test-environment.md)">Использование тестовой среды</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Редактор запрашивает развертывание объекта групповой политики в производственной среде домена.</p></td>
<td align="left"><p><a href="request-deployment-of-a-gpo-agpm40.md" data-raw-source="[Request Deployment of a GPO](request-deployment-of-a-gpo-agpm40.md)">Запрос на развертывание объекта групповой политики</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>С помощью рецензентов, например утверждающих или редакторов, можно проанализировать объект групповой политики.</p></td>
<td align="left"><p><a href="performing-reviewer-tasks-agpm40.md" data-raw-source="[Performing Reviewer Tasks](performing-reviewer-tasks-agpm40.md)">Выполнение задач рецензента</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Утверждающее лицо утверждает и развертывает объект групповой политики в рабочей среде домена или отвергает объект групповой политики.</p></td>
<td align="left"><p><a href="approve-or-reject-a-pending-action-agpm40.md" data-raw-source="[Approve or Reject a Pending Action](approve-or-reject-a-pending-action-agpm40.md)">Утверждение или отклонение ожидающего действия</a></p></td>
</tr>
</tbody>
</table>

 

### Дополнительные ссылки

[Средство расширенного управления групповыми политиками 4.0](advanced-group-policy-management-40.md)

 

 





