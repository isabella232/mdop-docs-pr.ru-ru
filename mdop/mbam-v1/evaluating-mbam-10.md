---
title: Оценка MBAM 1.0
description: Оценка MBAM 1.0
author: dansimp
ms.assetid: a1e2b674-eda9-4e1c-9b4c-e748470c71f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f09b06af52f5738fd50bfe727987b760d98552d9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825252"
---
# Оценка MBAM 1.0


Прежде чем развертывать администрирование и мониторинг Microsoft BitLocker (MBAM) в рабочей среде, вы должны оценить его в лабораторной среде. В этой статье описано, как настроить MBAM в среде единого сервера лаборатории для целей оценки.

Несмотря на то, что фактические этапы развертывания очень похожи на сценарий, описанный в статье [Установка и настройка MBAM на одном сервере](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md), в этом разделе содержатся дополнительные сведения о том, как настроить среду оценки MBAM в течение минимального периода времени.

## Настройка лабораторной среды


Даже если вы настроили нерабочий экземпляр MBAM для оценки в лабораторной среде, вы должны убедиться, что выполнены необходимые требования к развертыванию, требования к оборудованию и программному обеспечению. Дополнительные сведения можно найти в разделе [MBAM 1,0 требования к развертыванию](mbam-10-deployment-prerequisites.md) и [поддерживаемые конфигурации MBAM 1,0](mbam-10-supported-configurations.md). Кроме того, прежде чем приступить к развертыванию MBAMной пробной версии, вам также следует предварительно [подготовить среду для MBAM 1,0](preparing-your-environment-for-mbam-10.md) .

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
<td align="left"><p><a href="getting-started-with-mbam-10.md" data-raw-source="[Getting Started with MBAM 1.0](getting-started-with-mbam-10.md)">Начало работы с MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p></p>
<p>Подготовьте рабочую среду для установки MBAM. Для этого необходимо включить прозрачное шифрование данных (TDE) для экземпляров SQL Server, которые будут размещаться в MBAM базах данных. Чтобы включить TDE в лабораторной среде, вы можете создать SQL-файл для работы с главной базой данных, размещенной в экземпляре SQL Server, который MBAM будет использовать.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Следующий пример можно использовать для создания SQL-файла для лабораторной среды для быстрого включения TDE на экземпляре SQL Server, на котором будут размещаться базы данных MBAM. Эти команды сервера SQL Server будут включать TDE с помощью локального подписанного сертификата SQL Server. Убедитесь в том, что резервная копия сертификата TDE и связанного ключа шифрования заданы в примере локального пути резервного копирования для <em> C:\Backup </em> . Сертификат и ключ TDE необходимы при восстановлении базы данных или перемещении сертификата и ключа на другой сервер, на котором TDE шифрование на месте.</p>
</div>
<div>

</div>
<pre class="syntax" space="preserve"><code>USE master;
GO
CREATE MASTER KEY ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;;
GO
CREATE CERTIFICATE tdeCert WITH SUBJECT = &#39;TDE Certificate&#39;;
GO
BACKUP CERTIFICATE tdeCert TO FILE = &#39;C:\Backup\TDECertificate.cer&#39;
   WITH PRIVATE KEY (
         FILE = &#39;C:\Backup\TDECertificateKey.pvk&#39;,
         ENCRYPTION BY PASSWORD = &#39;P@55w0rd&#39;);
GO</code></pre></td>
<td align="left"><p><a href="mbam-10-deployment-prerequisites.md" data-raw-source="[MBAM 1.0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md)">Необходимые компоненты развертывания MBAM 1.0</a></p>
<p><a href="https://go.microsoft.com/fwlink/?LinkId=269703" data-raw-source="[Database Encryption in SQL Server 2008 Enterprise Edition](https://go.microsoft.com/fwlink/?LinkId=269703)">Шифрование баз данных в SQL Server 2008 Enterprise Edition</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Спланируйте и настройте требования к групповой политике MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-group-policy-requirements.md" data-raw-source="[Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md)">Планирование требований групповой политики MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планируйте и создавайте необходимые группы безопасности доменных служб Active Directory и планируйте требования к членству в локальной группе безопасности MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Планирование ролей администратора MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планирование развертывания компонентов сервера MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-server-deployment.md" data-raw-source="[Planning for MBAM 1.0 Server Deployment](planning-for-mbam-10-server-deployment.md)">Планирование развертывания сервера MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Планирование развертывания клиента MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-client-deployment.md" data-raw-source="[Planning for MBAM 1.0 Client Deployment](planning-for-mbam-10-client-deployment.md)">Планирование развертывания клиента MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### Выполнение развертывания MBAM Evaluation

После того как вы завершите необходимые установки планирования и программного обеспечения, чтобы подготовить рабочую среду к установке MBAM, вы можете начать развертывание MBAM Evaluation.

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
<td align="left"><p>Ознакомьтесь со сведениями о поддерживаемых конфигурациях MBAM, чтобы убедиться, что выбранные клиентские и серверные компьютеры поддерживаются для установки компонента MBAM.</p></td>
<td align="left"><p><a href="mbam-10-supported-configurations.md" data-raw-source="[MBAM 1.0 Supported Configurations](mbam-10-supported-configurations.md)">Поддерживаемые конфигурации MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Запустите программу установки MBAM, чтобы развернуть компоненты сервера MBAM на одном сервере для ознакомления с целью оценки.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md" data-raw-source="[How to Install and Configure MBAM on a Single Server](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)">Установка и настройка MBAM на одном сервере</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Добавьте группы безопасности доменных служб Active Directory, созданные на этапе планирования, в соответствующие локальные группы MBAM локального сервера для нового сервера MBAM.</p></td>
<td align="left"><p><a href="planning-for-mbam-10-administrator-roles.md" data-raw-source="[Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md)">Планирование ролей администраторов MBAM 1,0 </a> и <a href="how-to-manage-mbam-administrator-roles-mbam-1.md" data-raw-source="[How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md)"> Управление РОЛЯМИ администратора MBAM</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Создание и развертывание необходимых объектов групповой политики MBAM.</p></td>
<td align="left"><p><a href="deploying-mbam-10-group-policy-objects.md" data-raw-source="[Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md)">Развертывание объектов групповой политики MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Развертывание программного обеспечения клиента MBAM.</p></td>
<td align="left"><p><a href="deploying-the-mbam-10-client.md" data-raw-source="[Deploying the MBAM 1.0 Client](deploying-the-mbam-10-client.md)">Развертывание клиента MBAM 1.0</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Настройка компьютеров лаборатории для оценки MBAM


Вы можете изменить параметры частоты в отчетах о состоянии клиента MBAM с помощью редактора реестра. Однако эти изменения следует использовать только для целей тестирования.

**Warning**  
В этой статье описано, как изменить реестр Windows с помощью редактора реестра. Если изменить реестр Windows некорректно, это может привести к серьезным неполадкам, которые могут потребовать повторной установки Windows. Перед изменением реестра необходимо создать резервную копию файлов реестра (System. dat и User. dat). Корпорация Майкрософт не несет ответственности за то, что проблемы, которые могут возникнуть при изменении реестра, могут быть устранены. Изменение реестра на свой страх и риск.



### <a href="" id="modify-the-frequency-settings-on-mbam-client-status-reporting-"></a>Изменение параметров частоты для отчетов о состоянии клиента MBAM

Значения частот для отчетов об пробуждении клиента MBAM и состоянии не менее 90 минут, когда они настроены на использование групповой политики. Вы можете изменить эти частоты на клиентских компьютерах MBAM, изменив реестр Windows, чтобы уменьшить значения, что поможет ускорить тестирование. Чтобы изменить параметры частоты в отчетах о состоянии клиента MBAM, используйте редактор реестра для перехода к **HKLM\\Software\\Policies\\FVE\\MDOPBitLockerManagement**, измените значения для **ClientWakeupFrequency** и **StatusReportingFrequency** на **1** в качестве минимального поддерживаемого клиентом значения, а затем перезапустите службу клиента управления BitLocker. Когда вы сделаете это изменение, клиент MBAM сообщит каждую минуту. Значения этого параметра можно настроить только в том случае, если это было сделано вручную в реестре.

### <a href="" id="modify-the-startup-delay-on-mbam-client-service-"></a>Изменение задержки запуска службы клиента MBAM

В дополнение к частотам вывода клиента на пробуждение и отчет о состоянии возникает случайная задержка до 90 минут, когда служба агента клиента MBAM запускается на клиентских компьютерах. Если вы не хотите использовать случайную задержку, создайте параметр **DWORD** для **NoStartupDelay** в разделе **HKLM\\Software\\Microsoft\\MBAM**, установите для него значение **1**, а затем перезапустите службу клиента управления BitLocker.

## Статьи по теме


[Начало работы с MBAM 1.0](getting-started-with-mbam-10.md)









