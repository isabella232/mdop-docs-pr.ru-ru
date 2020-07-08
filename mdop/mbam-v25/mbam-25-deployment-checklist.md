---
title: Контрольный список необходимых компонентов развертывания MBAM 2.5
description: Контрольный список необходимых компонентов развертывания MBAM 2.5
author: dansimp
ms.assetid: 2ba7de17-e3a4-4798-99e0-cd1dc28c5b76
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 11609b3d6d44d62b032e35005e5d967ca6d4e83b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822832"
---
# Контрольный список необходимых компонентов развертывания MBAM 2.5


Вы можете использовать этот контрольный список, чтобы помочь вам при развертывании Microsoft BitLocker и наблюдении (MBAM) с изолированной топологией.

**Примечание.**  
В этом контрольном списке описаны рекомендуемые шаги и высокоуровневый список элементов, которые следует принимать во время развертывания функций администрирования и мониторинга Microsoft BitLocker. Мы рекомендуем вам скопировать этот контрольный список в программу для работы с электронными таблицами и настроить ее для использования.



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
<td align="left"><p>Просматривайте и проверяйте все этапы планирования для подготовки среды к развертыванию MBAM.</p></td>
<td align="left"><p><a href="mbam-25-planning-checklist.md" data-raw-source="[MBAM 2.5 Planning Checklist](mbam-25-planning-checklist.md)">Контрольный список планирования MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Ознакомьтесь со сведениями о поддерживаемых конфигурациях, чтобы убедиться, что MBAM поддерживает выделенные клиентские и серверные компьютеры.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Установка программного обеспечения сервера MBAM.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Настройка функций сервера MBAM:</p>
<ul>
<li><p>База данных для проверки соответствия требованиям и базы данных восстановления</p></li>
<li><p>Отчеты</p></li>
<li><p>Веб-приложения</p></li>
<li><p>Топология интеграции Configuration Manager (требуется только в том случае, если вы работаете в MBAM с этой топологией)</p></li>
</ul>
<div class="alert">
<strong>Примечание.</strong><br/><p>Обратите внимание на имена серверов, на которых настраивается каждая функция. Эти сведения будут использоваться в ходе настройки.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="configuring-the-mbam-25-server-features.md" data-raw-source="[Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md)">Настройка компонентов сервера MBAM 2.5 Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Проверьте конфигурацию MBAM.</p></td>
<td align="left"><p><a href="validating-the-mbam-25-server-feature-configuration.md" data-raw-source="[Validating the MBAM 2.5 Server Feature Configuration](validating-the-mbam-25-server-feature-configuration.md)">Проверка конфигурации компонентов MBAM 2.5 Server</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Скопируйте шаблон групповой политики MBAM и измените параметры групповой политики.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Копирование шаблонов групповой политики MBAM 2,5 </a> и <a href="editing-the-mbam-25-group-policy-settings.md" data-raw-source="[Editing the MBAM 2.5 Group Policy Settings](editing-the-mbam-25-group-policy-settings.md)"> изменение параметров групповой политики MBAM 2,5</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Развертывание программного обеспечения клиента MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-25-client.md" data-raw-source="[Deploying the MBAM 2.5 Client](deploying-the-mbam-25-client.md)">Развертывание клиента MBAM 2.5</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>




## Статьи по теме


[Развертывание MBAM 2.5](deploying-mbam-25.md)




## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




