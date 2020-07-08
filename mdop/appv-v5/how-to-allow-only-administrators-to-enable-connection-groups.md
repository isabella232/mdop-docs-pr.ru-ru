---
title: Настройка включения групп соединений только для администраторов
description: Настройка включения групп соединений только для администраторов
author: dansimp
ms.assetid: 60e62426-624f-4f26-851e-41cd78520883
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 53461d5c93bf246210c7427c95a8bbe8acca9cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814461"
---
# Настройка включения групп соединений только для администраторов


Вы можете настроить клиент App-V таким образом, чтобы только администраторы (не конечные пользователи) могли включать или отключать группы подключения. В более ранних версиях приложения App-V вы не смогли предотвратить выполнение этих задач конечными пользователями.

**Примечание** 
 **Эта функция поддерживается начиная с версии App-V 5,0 SP3.**

 

Используйте один из следующих методов, чтобы разрешить или запретить только администраторам включать или отключать группы подключения.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Действия</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Параметр групповой политики</p></td>
<td align="left"><p>Включите параметр групповой политики "требуется публикация от имени администратора", который находится в следующем узле объекта групповой политики:</p>
<p><strong>Политики конфигурации &gt; компьютера &gt; Административные шаблоны &gt; , &gt; Публикация System App-V &gt;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Командлет PowerShell</p></td>
<td align="left"><p>Запустите <strong> командлет Set-AppvClientConfiguration </strong> с <strong> параметром – RequirePublishAsAdmin </strong> .</p>
<p>Значения параметров:</p>
<ul>
<li><p>0 – ложь</p></li>
<li><p>1 — истина</p></li>
</ul>
<p><strong>Пример: </strong> Set-AppvClientConfiguration – RequirePublishAsAdmin1</p></td>
</tr>
</tbody>
</table>

 

**У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Управление связывающими группами](managing-connection-groups.md)

 

 





