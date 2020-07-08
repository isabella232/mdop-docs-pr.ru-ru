---
title: Настройка баз данных MBAM 2.5
description: Настройка баз данных MBAM 2.5
author: dansimp
ms.assetid: 66e1c81b-f785-4398-9175-bb5f112c2a35
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c11cb58d8fd9266bd0322e4cf9aa96256b7fbb6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826622"
---
# Настройка баз данных MBAM 2.5


В этой статье объясняется, как настроить соответствие (MBAM) и базу данных аудита Microsoft BitLocker (в 2,5), а также базе данных.

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
<td align="left"><p>Установите серверное программное обеспечение MBAM на каждый сервер, на котором вы планируете настроить компонент MBAM Server.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Вы можете установить базы данных на удаленном компьютере SQL Server с помощью Windows PowerShell или пакета экспортированного приложения уровня данных (DAC). Дополнительные сведения о пакетах DAC можно найти в разделе <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> приложения уровня данных </a> .</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Если вы планируете использовать командлеты Windows PowerShell для настройки функций сервера MBAM, изучите необходимые условия для использования Windows PowerShell.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Настройка баз данных с помощью Windows PowerShell**

1.  Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.

2.  С помощью командлета Windows PowerShell **Enable-MbamDatabase** можно настроить базы данных. Чтобы получить сведения об этом командлете Windows PowerShell, введите **Get-Help Enable-MbamDatabase**.

**Настройка базы данных соответствия и аудита с помощью мастера**

1. На сервере, на котором вы хотите настроить базы данных, запустите мастер **настройки сервера MBAM** . Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".

2. Нажмите кнопку **Добавить новые функции**, выберите **соответствие и база данных для проверки соответствия и** **базы данных восстановления**, а затем нажмите кнопку **Далее**. Мастер проверяет, выполнены ли все необходимые условия для баз данных.

3. Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить. В противном случае устраните недостающие необходимые компоненты и нажмите кнопку **проверить необходимые компоненты еще раз**.

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
   <td align="left"><p><strong>Имя сервера SQL Server</strong></p></td>
   <td align="left"><p>Имя сервера, на котором настраивается база данных соответствия и аудита.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Для включения входящего трафика на порт Microsoft SQL Server необходимо добавить исключение на компьютере с базой данных соответствия требованиям и аудита. Номер порта по умолчанию — 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Экземпляр базы данных SQL Server</strong></p></td>
   <td align="left"><p>Имя экземпляра базы данных, в котором будут храниться данные о соответствии и аудите. Кроме того, необходимо указать, где будут храниться сведения о базе данных.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Имя базы данных</strong></p></td>
   <td align="left"><p>Имя базы данных, в которой будут храниться данные соответствия требованиям.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Если вы обновляете предыдущую версию MBAM, вы должны использовать то же имя базы данных, что и для прежнего развертывания.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Пользователь или группа доступа для чтения и записи</strong></p></td>
   <td align="left"><p>Пользователь или группа домена, у которых есть разрешение на чтение и запись в эту базу данных, чтобы разрешить веб-приложениям доступ к данным и отчетам в этой базе данных.</p>
   <p>Если вы введете в это поле пользователя, оно должно быть таким же, как значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> .</p>
   <p>Если в этом поле ввести группу, значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> должно быть членом группы, введенной в это поле.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Пользователь или группа домена "доступ только для чтения"</strong></p></td>
   <td align="left"><p>Имя пользователя или группы, которым будет предоставлено разрешение только на чтение для этой базы данных, чтобы разрешить этим отчетам получать доступ к данным о соответствии в этой базе данных.</p>
   <p>Если вы введете в это поле пользователя, он должен быть тем же пользователем, который указан в <strong> поле Учетная запись домена базы данных "соответствие требованиям" и "Аудит" </strong> на <strong> странице "Настройка отчетов" </strong> .</p>
   <p>Если вы ввели в это поле группу, значение, указанное в <strong> поле Учетная запись домена базы данных "соответствие требованиям и аудиту" </strong> на <strong> странице "Настройка отчетов", </strong> должно входить в группу, указанную в этом поле.</p></td>
   </tr>
   </tbody>
   </table>



5. Перейдите к следующему разделу, чтобы настроить базу данных восстановления.

**Настройка базы данных восстановления с помощью мастера**

1. Введите значения полей в мастере, используя следующие описания:

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
   <td align="left"><p><strong>Имя сервера SQL Server</strong></p></td>
   <td align="left"><p>Имя сервера, на котором вы настраиваете базу данных восстановления.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Необходимо добавить исключение на компьютере с базой данных восстановления, чтобы включить входящий трафик на порт Microsoft SQL Server. Номер порта по умолчанию — 1433.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Экземпляр базы данных SQL Server</strong></p></td>
   <td align="left"><p>Имя экземпляра базы данных, в котором будут храниться данные для восстановления. Кроме того, необходимо указать, где будут храниться сведения о базе данных.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Имя базы данных</strong></p></td>
   <td align="left"><p>Имя базы данных, в которой будут храниться данные для восстановления.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Если вы обновляете предыдущую версию MBAM, вы должны использовать то же имя базы данных, что и для прежнего развертывания.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Пользователь или группа доступа для чтения и записи</strong></p></td>
   <td align="left"><p>Пользователь или группа домена, у которых есть разрешение на чтение и запись в эту базу данных, чтобы разрешить веб-приложениям доступ к данным и отчетам в этой базе данных.</p>
   <p>Если вы введете в это поле пользователя, оно должно быть таким же, как значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> .</p>
   <p>Если в этом поле ввести группу, значение в <strong> поле Учетная запись домена пула приложений веб-службы </strong> на <strong> странице Настройка веб-приложений </strong> должно быть членом группы, введенной в это поле.</p></td>
   </tr>
   </tbody>
   </table>



2. Когда вы закончите ввод, нажмите кнопку **Далее**.

   Мастер проверяет, выполнены ли все необходимые условия для баз данных.

3. Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить. В противном случае устраните недостающие необходимые условия и нажмите кнопку **Далее** .

4. На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.

   **Примечание.**  
   Чтобы создать сценарий Windows PowerShell для записей, которые вы только что сделали, нажмите **экспортировать сценарий PowerShell**, а затем сохраните сценарий.



5. Нажмите кнопку **Добавить** , чтобы добавить базы данных MBAM на сервер, а затем нажмите кнопку **Закрыть**.



## Статьи по теме


[Журналы событий сервера](server-event-logs.md)

[Настройка компонентов сервера MBAM 2.5 Server](configuring-the-mbam-25-server-features.md)

[Настройка отчетов MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Настройка веб-приложений MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Проверка конфигурации компонентов MBAM 2.5 Server](validating-the-mbam-25-server-feature-configuration.md)



## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





