---
title: Планирование высокой доступности MBAM 2.5
description: Планирование высокой доступности MBAM 2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826942"
---
# Планирование высокой доступности MBAM 2.5


Администрирование и мониторинг Microsoft BitLocker (MBAM) может обеспечивать высокий уровень доступности с помощью одной или нескольких из описанных ниже технологий, описанных в следующих разделах.

-   [Группы доступности SQL Server AlwaysOn](#bkmk-alwayson)

-   [Кластеризация Microsoft SQL Server](#bkmk-sql-clustering)

-   [Балансировка сетевой нагрузки IIS](#bkmk-load-balance)

-   [Зеркальное отображение базы данных в SQL Server](#bkmk-db-mirroring)

-   [Резервное копирование баз данных MBAM с помощью службы теневого копирования томов (VSS)](#bkmk-vss)

Сведения о том, как развернуть MBAM в конфигурации высокой доступности, можно найти в следующих разделах.

## <a href="" id="bkmk-alwayson"></a>Поддержка групп доступности SQL Server AlwaysOn


MBAM позволяет настраивать группы доступности баз данных и управлять ими в Microsoft SQL Server. Группа доступности для MBAM поддерживает отказоустойчивую среду, в которой база данных соответствия и аудита и база данных восстановления не переносятся вместе, а не отдельно.

Группа доступности поддерживает набор баз данных для чтения и записи и один из четырех наборов соответствующих баз данных-получателей. Кроме того, дополнительные базы данных можно сделать доступными для разрешения только на чтение, некоторых операций резервного копирования или для обоих параметров.

Сведения о настройке групп доступности можно найти в разделе [группы доступности AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).

## <a href="" id="bkmk-sql-clustering"></a>Кластеризация Microsoft SQL Server


Базу данных проверки соответствия требованиям к MBAM 2,5 и базу данных для восстановления на компьютерах, на которых запущены кластеры SQL Server, можно выполнить.

## <a href="" id="bkmk-load-balance"></a>Балансировка сетевой нагрузки IIS


С помощью средства балансировки нагрузки сети можно настроить высокодоступную среду для компьютеров, на которых работает веб-сайт администрирования и мониторинга (также называемый службой поддержки), портал самообслуживания и веб-службы, которые развертываются с помощью служб IIS.

### Предварительные условия

Перед настройкой балансировки нагрузки убедитесь, что выполнены следующие требования:

-   Должна быть доступна подсистема балансировки нагрузки. Вы можете использовать балансировщик нагрузки из Microsoft или другой компании. Дополнительные сведения о технологии Microsoft балансировки нагрузки можно найти в разделе [Создание веб-фермы с помощью серверов IIS](https://go.microsoft.com/fwlink/?LinkId=393326).

-   По крайней мере два сервера работают под управлением служб IIS и удовлетворены всеми необходимыми компонентами MBAM для поддержки своих веб-функций, в том числе ASP.NET MVC 4.

-   Базы данных и отчеты MBAM запущены на сервере.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> Специфичные для MBAM изменения, необходимые для обеспечения балансировки нагрузки

Выполните указанные ниже действия.

1.  Зарегистрируйте имя субъекта-службы (SPN) для имени виртуального узла под учетной записью домена, которую вы используете для пулов приложений. Например, если имя виртуального узла — mbamvirtual.contoso.com, а учетная запись домена, используемая для пулов веб-приложений, — contoso\\mbamapppooluser, следующая команда регистрирует SPN соответствующим образом.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  Настройте следующие веб-функции MBAM:

    -   На каждом сервере, на котором будут размещаться веб-компоненты MBAM, используйте одну и ту же учетную запись домена для учетных данных администратора пула приложений.

    -   Укажите имя узла, соответствующее имени виртуального узла (DNS-имени) кластера балансировки нагрузки. Например, при установке MBAM на сервере под названием "NLB1" и именем виртуального узла **mbamvirtual.contoso.com**убедитесь в том, что имя узла, указанное в командлете Windows PowerShell, **mbamvirtual.contoso.com**.

3.  Если вы настраиваете веб-сайты в веб-ферме с помощью подсистемы балансировки нагрузки, необходимо настроить веб-сайты на использование одного ключа компьютера.

    Дополнительные сведения можно найти в следующих разделах [элемента machineKey (схема параметров ASP.NET)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx).

    -   Описание ключа компьютера

    -   Рекомендации по развертыванию веб-фермы

    Инструкции по созданию ключа для автоматического создания см. в разделе [Создание ключа компьютера (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).

Сведения о балансировке нагрузки также применимы к кластерам балансировки сетевой нагрузки (NLB) для IIS в Windows Server 2012 или Windows Server2008R2. Функция балансировки нагрузки сети для служб IIS в Windows Server 2012 обычно такая же, как и в Windows Server2008R2. Однако некоторые сведения о задачах в Windows Server 2012 отличаются. Сведения о новых способах выполнения задач можно найти [в разделе типичные задачи управления и Навигация в Windows server 2012 R2 Preview и Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).

## <a href="" id="bkmk-db-mirroring"></a>Зеркальное отображение базы данных в SQL Server


MBAM поддерживает использование зеркального отображения SQL Server, в котором база данных соответствия требованиям и аудита и база данных восстановления зеркально отражаются с помощью двух экземпляров SQL Server для каждой базы данных. Перед реализацией зеркального отображения следует учитывать, что зеркальное отображение выполняется постепенно, в пользу групп доступности, рассмотренных ранее в этом разделе.

Для реализации зеркального отображения для MBAM необходимо указать соответствующие строки подключения для конфигурации зеркальной базы данных с помощью командлета Windows PowerShell **Enable-MbamWebApplication** . Дополнительные сведения о командлетах Windows PowerShell MBAM 2,5 можно найти в разделе [Настройка серверных функций MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

### Примеры реализации зеркального отображения SQL Server с помощью Windows PowerShell

В следующих примерах показано, как вы можете реализовать зеркальное отображение SQL Server с помощью командлетов Windows PowerShell.

**Пример 1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**Пример 2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### Дополнительные сведения о зеркальном отображении SQL Server

Ниже приведены ссылки на дополнительные сведения о настройке зеркального отображения SQL Server.

-   [Инструкции: Подготовка зеркальной базы данных для зеркального отображения (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Создание сеанса зеркального отображения базы данных с использованием проверки подлинности Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>Резервное копирование баз данных MBAM с помощью службы теневого копирования томов (VSS)


MBAM предоставляет средство записи службы теневого копирования тома (VSS), которое называется администратором Microsoft BitLocker и разработчиком управления. Этот модуль записи VSS упрощает резервное копирование базы данных соответствия требованиям и аудита и базы данных восстановления.

Средство записи VSS регистрируется на каждом сервере, на котором вы включаете веб-приложение MBAM. Средство записи VSS MBAM зависит от модуля записи VSS SQL Server, которое зарегистрировано как часть установки Microsoft SQL Server. Любая технология резервного копирования, использующая средства записи VSS для выполнения резервного копирования, может найти модуль записи VSS MBAM.



## Статьи по теме


[Планирование развертывания MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




