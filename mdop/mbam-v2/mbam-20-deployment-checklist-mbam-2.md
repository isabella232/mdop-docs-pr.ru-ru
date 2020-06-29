---
title: Контрольный список необходимых компонентов развертывания MBAM 2.0
description: Контрольный список необходимых компонентов развертывания MBAM 2.0
author: dansimp
ms.assetid: 7905d31d-f21c-4683-b9c4-95b815e08fab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d8d0ce1a3ff48d4bf2f84e61b4a578b170264a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826439"
---
# Контрольный список необходимых компонентов развертывания MBAM 2.0


Этот контрольный список поможет вам при развертывании Microsoft BitLocker и наблюдении (MBAM) с изолированной топологией.

**Примечание.**  
В этом контрольном списке описаны рекомендованные шаги и высокоуровневый список элементов, которые следует принимать во время развертывания функций администрирования и мониторинга Microsoft BitLocker. Рекомендуется скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.



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
<td align="left"><p><a href="mbam-20-planning-checklist-mbam-2.md" data-raw-source="[MBAM 2.0 Planning Checklist](mbam-20-planning-checklist-mbam-2.md)">Контрольный список планирования MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ознакомьтесь со сведениями о конфигурации, поддерживаемыми MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Поддерживаемые конфигурации MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM в указанном ниже порядке.</p>
<ol>
<li><p>База данных восстановления</p></li>
<li><p>База данных соответствия требованиям и аудита</p></li>
<li><p>Аудит соответствия требованиям и отчеты</p></li>
<li><p>Сервер самообслуживания</p></li>
<li><p>Сервер администрирования и мониторинга</p></li>
<li><p>Шаблон групповой политики MBAM</p></li>
</ol>
<div class="alert">
<strong>Примечание.</strong><br/><p>Следите за именами серверов, на которых установлены все компоненты. Эти сведения будут использоваться во время установки.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="deploying-the-mbam-20-server-infrastructure-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Server Infrastructure](deploying-the-mbam-20-server-infrastructure-mbam-2.md)">Развертывание инфраструктуры сервера MBAM 2.0 Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Добавьте группы безопасности доменных служб Active Directory, созданные на этапе планирования, в соответствующие локальные группы администраторов компонентов сервера MBAM на соответствующих серверах.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Планирование ролей администраторов MBAM 2,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Управление РОЛЯМИ администратора MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Создание и развертывание необходимых объектов групповой политики MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Развертывание объектов групповой политики MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Развертывание программного обеспечения клиента MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Развертывание клиента MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Развертывание MBAM 2.0](deploying-mbam-20-mbam-2.md)









