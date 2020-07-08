---
title: Настройка интеграции System Center Configuration Manager с MBAM 2.5
description: Настройка интеграции System Center Configuration Manager с MBAM 2.5
author: dansimp
ms.assetid: 2b8a4c13-1dad-41e8-89ac-6889c5f7e051
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c6fb0a0b06399baf1dc6493a40d17e76a51741f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812445"
---
# Настройка интеграции System Center Configuration Manager с MBAM 2.5


В этой статье объясняется, как настроить администрирование и мониторинг Microsoft BitLocker (MBAM), чтобы использовать топологию интеграции System Center Configuration Manager, которая интегрирует MBAM с Configuration Manager.

В этой статье объясняется, как настроить интеграцию Configuration Manager с помощью:

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
<td align="left"><p><a href="high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md" data-raw-source="[High-Level Architecture of MBAM 2.5 with Configuration Manager Integration Topology](high-level-architecture-of-mbam-25-with-configuration-manager-integration-topology.md)">Высокоуровневая архитектура MBAM 2.5 с топологией интеграции диспетчера конфигураций</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Проверка поддерживаемых конфигураций для MBAM.</p></td>
<td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Поддерживаемые конфигурации MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Заполните необходимые условия на каждом сервере.</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Необходимые условия MBAM 2.5 Server, которые применяются только к топологии интеграции диспетчера конфигураций</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Установка программного обеспечения сервера MBAM на каждый сервер, на котором будет настроена функция сервера MBAM.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для этой топологии необходимо установить консоль Configuration Manager на компьютере, на котором устанавливается программное обеспечение сервера MBAM.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Изучите предварительные требования для Windows PowerShell (применимо только в том случае, если вы собираетесь использовать командлеты Windows PowerShell для настройки MBAM).</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Настройка интеграции Configuration Manager с помощью Windows PowerShell**

1.  Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.

2.  С помощью командлета Windows PowerShell **Enable-MbamCMIntegration** можно настроить отчеты. Чтобы получить сведения об этом командлете, введите **Get-Help Enable-MbamCMIntegration**.

**Настройка интеграции System Center Configuration Manager с помощью мастера**

1.  На сервере, на котором вы хотите настроить функцию интеграции System Center Configuration Manager, запустите мастер настройки сервера MBAM. Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".

2.  Нажмите кнопку **Добавить новые функции**, выберите **Интеграция System Center Configuration Manager**и нажмите кнопку **Далее**.

    Мастер проверяет, выполнены ли все необходимые условия для интеграции Configuration Manager.

3.  Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить. В противном случае устраните недостающие необходимые компоненты и нажмите кнопку **проверить необходимые компоненты еще раз**.

4.  Чтобы ввести значения полей в мастере, воспользуйтесь приведенными ниже описаниями.

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
    <td align="left"><p><strong>Сервер служб SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Полное доменное имя (FQDN) сервера с ролью точки обслуживания отчетов. Это сервер, на который развертываются отчеты диспетчера конфигураций MBAM.</p>
    <p>Если вы не указали сервер, отчеты Configuration Manager будут развернуты на локальном сервере.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Экземпляр служб SQL Server Reporting Services</strong></p></td>
    <td align="left"><p>Имя экземпляра служб SQL Server Reporting Services (SSRS), в котором развертываются отчеты Configuration Manager.</p>
    <p>Если экземпляр не указан, отчеты Configuration Manager будут развернуты в имени экземпляра служб SSRS по умолчанию. Введенное значение игнорируется, если на сервере установлен System Center 2012 Configuration Manager.</p></td>
    </tr>
    </tbody>
    </table>



5.  На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.

    **Примечание.**  
    Чтобы создать сценарий Windows PowerShell для только что сделанных записей, нажмите **экспортировать сценарий PowerShell** и сохранить сценарий.



6.  Нажмите кнопку **Добавить** , чтобы добавить компонент интеграции Configuration Manager на сервер, а затем нажмите кнопку **Закрыть**.



## Статьи по теме


[Настройка компонентов сервера MBAM 2.5 Server](configuring-the-mbam-25-server-features.md)

[Проверка конфигурации компонентов MBAM 2.5 Server](validating-the-mbam-25-server-feature-configuration.md)


## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






