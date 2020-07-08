---
title: Контрольный список необходимых компонентов развертывания MBAM 1.0
description: Контрольный список необходимых компонентов развертывания MBAM 1.0
author: dansimp
ms.assetid: 7e00be23-36a0-4b0f-8663-3c4f2c71546d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 96725183af2cb4e3d86d3f42973452c598497773
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812536"
---
# Контрольный список необходимых компонентов развертывания MBAM 1.0


Этот контрольный список разработан для упрощения развертывания администрирования и мониторинга Microsoft BitLocker (MBAM).

**Примечание.**  
В этом контрольном списке описаны рекомендованные шаги и представлен высокоуровневый список элементов, которые следует принимать во время развертывания функций MBAM. Мы рекомендуем вам скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для удовлетворения конкретных потребностей.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Задача</th>
<th align="left">Ссылки</th>
<th align="left">Заметки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Заполните этап планирования для подготовки вычислительной среды для MBAM развертывания.</p></td>
<td align="left"><p><a href="mbam-10-planning-checklist.md" data-raw-source="[MBAM 1.0 Planning Checklist](mbam-10-planning-checklist.md)">Контрольный список планирования MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ознакомьтесь со сведениями о поддерживаемых конфигурациях MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Поддерживаемые конфигурации MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM в указанном ниже порядке.</p>
<ol>
<li><p>База данных восстановления и оборудования</p></li>
<li><p>База данных состояния соответствия требованиям</p></li>
<li><p>Аудит соответствия требованиям и отчеты</p></li>
<li><p>Сервер администрирования и мониторинга</p></li>
<li><p>Шаблон групповой политики MBAM</p></li>
</ol>
<div class="alert">
<strong>Примечание.</strong><br/><p>Следите за именами серверов, на которых установлены все компоненты. Эти данные будут использоваться во время установки.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-10-server-infrastructure.md" data-raw-source="[Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md)">Развертывание инфраструктуры сервера MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Добавьте группы безопасности доменных служб Active Directory, созданные на этапе планирования, в соответствующие локальные группы администраторов компонентов сервера MBAM на соответствующих серверах.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Планирование ролей администраторов MBAM 1,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Управление РОЛЯМИ администратора MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Создание и развертывание необходимых объектов групповой политики MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Развертывание объектов групповой политики MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Развертывание программного обеспечения клиента MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Развертывание клиента MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Развертывание MBAM 1.0](deploying-mbam-10.md)









