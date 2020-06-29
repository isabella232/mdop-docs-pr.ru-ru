---
title: Планирование развертывания App-V 5.1 с помощью системы электронного распространения программного обеспечения
description: Планирование развертывания App-V 5.1 с помощью системы электронного распространения программного обеспечения
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813400"
---
# Планирование развертывания App-V 5.1 с помощью системы электронного распространения программного обеспечения


Если вы используете электронную систему распространения программного обеспечения для развертывания пакетов App-V, ознакомьтесь с приведенными ниже замечаниями по планированию. Дополнительные сведения об использовании System Center Configuration Manager для развертывания App-V можно найти [в разделе Общие сведения об управлении приложениями в Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).

Ознакомьтесь со следующими параметрами требований к компонентам и архитектуре, которые применяются при использовании ESD для развертывания пакетов App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Требования к развертыванию или параметр</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер управления App-V, база данных управления и сервер публикаций не требуются.</p></td>
<td align="left"><p>Эти функции обрабатываются реализованным решением ESD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Вы можете развернуть сервер отчетов App-V и базу данных отчетов рядом друг с другом с помощью ESD.</p></td>
<td align="left"><p>Параллельное развертывание позволяет собирать данные и создавать отчеты.</p>
<p>Если вы включите клиент App-V для отправки сведений о отчете и не используете сервер отчетов App-V, данные отчетов хранятся в связанных XML-файлах.</p></td>
</tr>
</tbody>
</table>

 






## Статьи по теме


[Планирование развертывания App-V](planning-to-deploy-app-v51.md)

 

 





