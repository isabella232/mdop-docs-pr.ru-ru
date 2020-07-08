---
title: Настройка отчетов MBAM 2.5
description: Настройка отчетов MBAM 2.5
author: dansimp
ms.assetid: ec462879-0253-4d9c-83c7-a9bcad479725
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b372bd6bc38a3729aef43354ecf19b2619b7856
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826619"
---
# Настройка отчетов MBAM 2.5


В этой статье объясняется, как настроить функцию отчетов администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 с помощью:

-   Командлет Windows PowerShell

-   Мастер настройки сервера MBAM

Инструкции основываются на рекомендованной архитектуре на [высоком уровне архитектуры для MBAM 2,5](high-level-architecture-for-mbam-25.md).

**Прежде чем приступить к настройке, выполните указанные ниже действия.**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Шаг</th>
<th align="left">Где найти инструкции</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Изучите рекомендованную архитектуру для MBAM.</p></td>
<td align="left"><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Высокоуровневая архитектура для MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Проверка поддерживаемых конфигураций для MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Заполните необходимые условия на каждом сервере.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Требования к серверу MBAM 2,5, применимые только к топологии интеграции Configuration Manager </a> (если применимо)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы планируете настроить компонент MBAM Server.</p></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Если вы планируете использовать командлеты Windows PowerShell для настройки функций сервера MBAM, изучите необходимые условия для использования Windows PowerShell.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Настройка отчетов с помощью Windows PowerShell**

1.  Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.

2.  С помощью командлета Windows PowerShell **Enable-MbamReport** можно настроить отчеты. Чтобы получить сведения об этом командлете Windows PowerShell, введите **Get-Help Enable-MbamReport**.

**Настройка отчетов с помощью мастера**

1. На сервере, на котором вы хотите настроить отчеты, запустите мастер **настройки сервера MBAM** . Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".

2. Нажмите кнопку **Добавить новые функции**, выберите пункт **отчеты**, а затем нажмите кнопку **Далее**. Мастер проверяет, выполнены ли все необходимые условия для отчетов.

3. Чтобы продолжить, нажмите **Далее**.

4. Введите значения полей в мастере, используя следующие описания:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Поле</th>
   <th align="left">Описание</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Экземпляр служб SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>Экземпляр служб SQL Server Reporting Services, в котором будут настраиваться отчеты.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Группа домена "роль отчета"</strong></p></td>
   <td align="left"><p>Имя группы "Пользователи домена", у участников которой есть права на доступ к отчетам на сервере администрирования и мониторинга.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Имя сервера SQL Server</strong></p></td>
   <td align="left"><p>Имя сервера, на котором настроена база данных соответствия и аудита.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Экземпляр базы данных SQL Server</strong></p></td>
   <td align="left"><p>Имя экземпляра SQL Server (например, <em> MSSQLServer </em> ), на котором настроена база данных соответствия и аудита.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Чтобы включить входящий трафик для порта сервера отчетов, необходимо добавить на компьютере с отчетом исключение для входящего трафика (порт по умолчанию — 80).</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Имя базы данных</strong></p></td>
   <td align="left"><p>Имя базы данных соответствия требованиям и аудита. По умолчанию имя базы данных имеет <strong> состояние соответствия MBAM </strong> , но вы можете изменить его при настройке базы данных "соответствие" и "Аудит".</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Если вы обновляете предыдущую версию MBAM, вы должны использовать имя базы данных, совпадающее с именем, используемым в предыдущем развертывании.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Учетная запись домена базы данных соответствия требованиям и аудита</strong></p></td>
   <td align="left"><p>Учетная запись пользователя домена и пароль для доступа к базе данных соответствия требованиям и аудита.</p>
   <p>Если значение, введенное в <strong> поле пользователя или группы домена "доступ только для чтения" </strong> на <strong> странице "Настройка баз данных" </strong> , является пользователем, необходимо указать это же значение в этом поле.</p>
   <p>Если значение, введенное в <strong> поле пользователя или группы домена "доступ только для чтения" </strong> на <strong> странице "Настройка баз данных" </strong> , является группой, значение, введенное в этом поле, должно быть членом этой группы.</p>
   <p>Настройка пароля для этой учетной записи бессрочна. Учетная запись пользователя должна иметь доступ ко всем данным, доступным группе "Пользователи отчетов MBAM".</p></td>
   </tr>
   </tbody>
   </table>



5. Когда вы закончите ввод, нажмите кнопку **Далее**.

   Мастер проверяет, выполнены ли все необходимые условия для функции "отчеты".

6. Чтобы продолжить, нажмите **Далее**.

7. На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.

   **Примечание.**  
   Чтобы создать сценарий Windows PowerShell для записей, которые вы только что сделали, нажмите **экспортировать сценарий PowerShell**, а затем сохраните сценарий.



8. Нажмите кнопку **Добавить** , чтобы добавить отчеты на сервер, а затем нажмите кнопку **Закрыть**.



## Статьи по теме


[Журналы событий сервера](server-event-logs.md)

[Настройка компонентов сервера MBAM 2.5 Server](configuring-the-mbam-25-server-features.md)

[Настройка веб-приложений MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Проверка конфигурации компонентов MBAM 2.5 Server](validating-the-mbam-25-server-feature-configuration.md)


## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






