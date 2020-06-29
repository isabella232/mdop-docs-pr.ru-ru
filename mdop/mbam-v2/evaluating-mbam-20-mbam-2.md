---
title: Оценка MBAM 2.0
description: Оценка MBAM 2.0
author: dansimp
ms.assetid: bfc77eec-0fd7-4fec-9c78-6870afa87152
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b7be883f44f5f09a904f619972ae3e7c35261d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824739"
---
# Оценка MBAM 2.0


Прежде чем развертывать администрирование и мониторинг Microsoft BitLocker (MBAM) в рабочей среде, вы должны оценить ее в тестовой среде. Сведения в этом разделе можно использовать для настройки администрирования Microsoft BitLocker и наблюдения за изолированной топологией в односерверной тестовой среде только для целей оценки. Односерверная топология не рекомендуется для рабочих сред.

Инструкции по развертыванию MBAM в тестовой среде можно найти в разделе [Установка и настройка MBAM на одном сервере](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md).

## Настройка тестовой среды


Несмотря на то, что вы настраиваете нерабочий экземпляр MBAM для оценки в тестовой среде, вы должны убедиться, что выполнены необходимые условия и требования к оборудованию и программному обеспечению. Прежде чем приступить к установке, ознакомьтесь с [требованиями к развертыванию MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md), [MBAM 2,0 поддерживаемые конфигурации](mbam-20-supported-configurations-mbam-2.md)и [подготовки среды для MBAM 2,0](preparing-your-environment-for-mbam-20-mbam-2.md).

### Планирование развертывания MBAM Evaluation

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
<td align="left"><p>Ознакомьтесь со статьей Приступая к работе с MBAM, чтобы получить основные сведения о продукте перед началом планирования развертывания.</p></td>
<td align="left"><p><a href="getting-started-with-mbam-20-mbam-2.md" data-raw-source="[Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)">Начало работы с MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планируйте требования к развертыванию MBAM 2,0 и подготовьте свою рабочую среду.</p></td>
<td align="left"><p><a href="mbam-20-deployment-prerequisites-mbam-2.md" data-raw-source="[MBAM 2.0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md)">Необходимые условия для развертывания MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Спланируйте и настройте требования к групповой политике MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-group-policy-requirements-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md)">Планирование требований групповой политики MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планируйте и создавайте необходимые группы безопасности ActiveDirectoryDomainServices и планируйте требования к членству в локальной группе безопасности MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Планирование ролей администратора MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планирование развертывания компонентов сервера MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-server-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md)">Планирование развертывания сервера MBAM 2.0 Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планируйте развертывание клиента MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-client-deployment-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Client Deployment](planning-for-mbam-20-client-deployment-mbam-2.md)">Планирование развертывания клиента MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

### Выполнение развертывания MBAM Evaluation

После того как вы заполните необходимые настройки планирования и программного обеспечения для подготовки вычислительной среды к установке MBAM, вы можете начать развертывание MBAM Evaluation.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ознакомьтесь со сведениями о конфигурации MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</p></td>
<td align="left"><p><a href="mbam-20-supported-configurations-mbam-2.md" data-raw-source="[MBAM 2.0 Supported Configurations](mbam-20-supported-configurations-mbam-2.md)">Поддерживаемые конфигурации MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM на одном сервере для ознакомления с целью оценки.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-2.md)">Установка и настройка MBAM на одном сервере</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Добавляйте группы безопасности ActiveDirectoryDomainServices, созданные на этапе планирования, в соответствующие локальные группы MBAM на новом сервере MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-20-administrator-roles-mbam-2.md" data-raw-source="[Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md)">Планирование ролей администраторов MBAM 2,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-2.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md)"> Управление РОЛЯМИ администратора MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Создание и развертывание необходимых объектов групповой политики MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-20-group-policy-objects-mbam-2.md" data-raw-source="[Deploying MBAM 2.0 Group Policy Objects](deploying-mbam-20-group-policy-objects-mbam-2.md)">Развертывание объектов групповой политики MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Развертывание программного обеспечения клиента MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-20-client-mbam-2.md" data-raw-source="[Deploying the MBAM 2.0 Client](deploying-the-mbam-20-client-mbam-2.md)">Развертывание клиента MBAM 2.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Настройка компьютеров лаборатории для оценки MBAM


В этом разделе содержатся сведения, с помощью которых можно ускорить создание отчетов о состоянии клиента MBAM. Однако эти изменения следует использовать только для целей тестирования.

**Примечание**  В разделе сведения, приведенные в этой статье, описано, как изменить реестр Windows. Неправильное использование редактора реестра может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows. Корпорация Майкрософт не гарантирует, что проблемы, возникающие в результате неправильного использования редактора реестра, могут быть устранены. Ответственность за использование редактора реестра.

 

### Изменение параметров частоты отчетов о состоянии клиента MBAM

Значения частот для отчетов об пробуждении клиента MBAM и состоянии в 90 минут заданы с помощью групповой политики. Вы можете использовать реестр Windows, чтобы изменить эти частоты на более низкие значения на клиентских компьютерах MBAM, чтобы ускорить тестирование.

Чтобы изменить параметры частоты отчета о состоянии клиента MBAM, выполните указанные ниже действия.

1.  С помощью редактора реестра перейдите в **HKLM\\Software\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement**.

2.  Измените значения для **ClientWakeupFrequency** и **StatusReportingFrequency** на **1** в качестве минимального значения, поддерживаемого клиентом. Это изменение приводит к тому, что клиент MBAM сообщает каждую минуту.

3.  Перезапустите **службу клиента управления BitLocker**.

**Примечание**  Чтобы установить этот низкий значения, необходимо вручную настроить их в реестре.

 

### Изменение задержки запуска службы клиента MBAM

В дополнение к частотам вывода клиента на пробуждение и отчет о состоянии возникает случайная задержка до 90 минут, когда служба агента клиента MBAM запускается на клиентских компьютерах. Если вы не хотите использовать случайную задержку, создайте параметр **DWORD** для **NoStartupDelay** в разделе **HKLM\\Software\\Microsoft\\MBAM**, установите для него значение **1**, а затем перезапустите **службу клиента управления BitLocker**.

## Статьи по теме


[Начало работы с MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





