---
title: Предварительные требования App-V 5.0
description: Предварительные требования App-V 5.0
author: dansimp
ms.assetid: 9756b571-c785-4ce6-a95c-d4e134e89429
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 176c9729d8c909325c6d6694e024938d9ce9df53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814813"
---
# Предварительные требования App-V 5.0

Прежде чем приступить к установке Microsoft Application Virtualization (App-V) 5,0, убедитесь, что для установки продукта выполнены необходимые условия. В этой статье приведены сведения, которые помогут вам успешно спланировать предварительную подготовку вычислительной среды перед развертыванием функций App-V 5,0.

> [!Important]
> **Предварительные требования, описанные в этой статье, применимы только к приложению App-V 5,0**. Дополнительные требования, применимые к пакетам обновления App-V 5,0, можно найти на веб-страницах ниже.

-   [Новые возможности в App-V 5.0 с пакетом обновления 1 (SP1)](whats-new-in-app-v-50-sp1.md)

-   [Сведения об App-V 5.0 с пакетом обновления 2 (SP2)](about-app-v-50-sp2.md)

-   [Необходимые условия для App-V 5.0 с пакетом обновления 3 (SP3)](app-v-50-sp3-prerequisites.md)

В следующей таблице перечислены предварительные сведения, относящиеся к определенным операционным системам.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционные системы</th>
<th align="left">Описание предварительной проверки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Запущенные компьютеры:</p>
<ul>
<li><p>Windows 8</p></li>
<li><p>Windows Server 2012</p></li>
</ul></td>
<td align="left"><p>Следующие предварительные требования уже установлены:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5 – вам не нужна платформа Microsoft .NET Framework 4</p></li>
<li><p>Windows PowerShell 3,0</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Запущенные компьютеры:</p>
<ul>
<li><p>Windows 7;</p></li>
<li><p>Windows Server 2008</p></li>
</ul></td>
<td align="left"><p>Вам может потребоваться загрузить следующую статью:</p>
<p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[Microsoft Security Advisory: Insecure library loading could allow remote code execution](https://support.microsoft.com/kb/2533623)">Рекомендации по безопасности Microsoft: Небезопасная загрузка библиотеки может привести к удаленному выполнению кода</a></p>
<p>Убедитесь, что для последующих КБ, которые заменяют этот вариант, и обратите внимание на то, что для некоторых КБ может потребоваться удаление предыдущих обновлений.</p></td>
</tr>
</tbody>
</table>

## Необходимые условия для установки App-V 5,0

> [!Note]  
> Следующие предварительные требования уже установлены на компьютерах под управлением Windows 8.

Каждая из функций App-V 5,0 имеет определенные предварительные требования, которые должны быть выполнены перед тем, как можно будет успешно установить компоненты App-V 5,0.

### Предварительные требования для клиента App-V 5,0

В следующей таблице перечислены требования к установке для клиента App-V 5,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Требования к программному обеспечению</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для установки PowerShell 3,0 требуется перезагрузка.</p>
</div>
<div>

</div></li>
<li><p>Скачивание и установка <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Важно.</strong><br/><p>Вы можете скачать и установить предыдущую статью в базе знаний. Однако она может быть заменена более поздней версией.</p>
</div>
<div>

</div></li>
<li><p>Установщик клиента (exe) обнаружит, нужно ли установить следующие необходимые компоненты, и будет выполнять указанные ниже действия.</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p>
<p>Этот предварительный компонент необходим только в том случае, если вы установили пакет исправлений 4 для Application Virtualization 5,0 SP2 или более поздней версии.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Распространяемый пакет Microsoft Visual C++ 2010</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Распространяемый пакет Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Необходимые условия для клиента служб удаленных рабочих столов App-V 5,0

> [!Note]  
> Следующие предварительные требования уже установлены на компьютерах под управлением Windows Server 2012.

В следующей таблице перечислены требования к установке для клиента служб удаленных рабочих столов App-V 5,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Требования к программному обеспечению</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft.NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft.NET Framework 4 (полный пакет)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для установки PowerShell 3,0 требуется перезагрузка.</p>
</div>
<div>

</div></li>
<li><p>Скачивание и установка <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Важно.</strong><br/><p>Вы можете скачать и установить предыдущую статью в базе знаний. Однако она может быть заменена более поздней версией.</p>
</div>
<div>

</div></li>
<li><p>Установщик клиента (exe) обнаружит, нужно ли установить следующие необходимые компоненты, и будет делать это соответствующим образом.</p>
<p></p>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p>
<p>Этот предварительный компонент необходим только в том случае, если вы установили пакет исправлений 4 для Application Virtualization 5,0 SP2 или более поздней версии.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=26999" data-raw-source="[The Microsoft Visual C++ 2010 Redistributable](https://www.microsoft.com/download/details.aspx?id=26999)">Распространяемый пакет Microsoft Visual C++ 2010</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=5638" data-raw-source="[Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://www.microsoft.com/download/details.aspx?id=5638)">Распространяемый пакет Microsoft Visual C++ 2005 SP1 (x86)</a></p></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

### Предварительные требования для секвенсора App-V 5,0

> [!Note]
> Следующие предварительные требования уже установлены на компьютерах под управлением Windows 8 и Windows Server 2012.

В следующей таблице перечислены требования к установке для приложения App-V 5,0 Sequencer. Если это возможно, компьютер, на котором работает секвенсор, должен иметь те же конфигурации оборудования и программного обеспечения, что и компьютеры, на которых будут запускаться виртуальные приложения.

> [!Note]  
> Если требования к системе для приложения, установленного локально, превышают требования секвенсора, необходимо соблюдать требования, предъявляемые к этому приложению. Кроме того, так как процесс упорядочения — это ресурсоемкие ресурсы, рекомендуется, чтобы компьютер, на котором работает секвенсор, работал с достаточной памятью, быстрым процессором и быстрым жестким диском. Дополнительные сведения см. в разделе [Поддерживаемые конфигурации App-V 5,0](app-v-50-supported-configurations.md).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Требования к программному обеспечению</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p>
<p>Этот предварительный компонент необходим только в том случае, если вы установили пакет исправлений 4 для Application Virtualization 5,0 SP2.</p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</a></p>
<p></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></li>
<li><p>Скачивание и установка <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p></li>
<li><p>Для компьютеров под управлением Microsoft Windows Server 2008 R2 SP1 Скачайте и установите <a href="https://go.microsoft.com/fwlink/?LinkId=286102" data-raw-source="[KB2533623](https://go.microsoft.com/fwlink/?LinkId=286102 )"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Важно.</strong><br/><p>Вы можете загрузить и установить одну из предыдущих статей базы знаний. Однако они могут быть заменены более поздней версией.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
</tbody>
</table>

### Предварительные требования для сервера App-V 5,0

> [!Note]
> Для компьютеров под управлением Windows Server 2012 уже установлены следующие предварительные требования:

-   Microsoft .NET Framework 4,5. Это позволит устранить требования Microsoft .NET Framework 4.

-   Windows PowerShell 3,0

-   Скачайте и установите [KB2533623](https://support.microsoft.com/kb/2533623) (https://support.microsoft.com/kb/2533623)

    > [!Important]
    > Вы по-прежнему можете скачать предыдущую версию KB. Однако она может быть заменена более поздней версией.

В следующей таблице перечислены требования к установке сервера App-V 5,0. У учетной записи, которую вы используете для установки серверных компонентов, должны быть права администратора на компьютере, на котором выполняется установка. Эта учетная запись должна также иметь возможность запросов к службам каталогов Active Directory. Перед установкой и настройкой серверов App-V 5,0 необходимо указать порт, в котором будет размещен каждый из компонентов. Кроме того, необходимо добавить соответствующие правила брандмауэра, разрешающие входящие запросы на указанные порты.

> [!Note]
> Служба управления распределенными разработками и версиями (WebDAV) автоматически отключается.

Сервер App-V 5,0 поддерживается для автономного развертывания, где все компоненты развертываются на одном и том же сервере и как распределенное развертывание. В зависимости от топологии, которую вы используете для развертывания сервера App-V 5,0, данные, которые вам понадобятся для каждого компонента, будут слегка изменены.

> [!Important]
> Установка сервера App-V 5,0 на компьютере, на котором запущены предыдущие версии или компоненты App-V, не поддерживается. Кроме того, установка серверных компонентов на компьютере, на котором запущены серверные ядра или контроллер домена, также не поддерживается.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Сервер управления</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</a></p></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для установки PowerShell 3,0 требуется перезагрузка.</p>
</div>
<div>

</div></li>
<li><p>Веб-сервер Windows с включенной ролью IIS и следующими возможностями: <strong> Основные возможности HTTP </strong> (статическое содержимое и документ по умолчанию), <strong> разработка приложений </strong> (ASP.NET, расширение среды .NET, расширения ISAPI и фильтры ISAPI), <strong> Безопасность </strong> (проверка подлинности Windows, Фильтрация запросов), <strong> средства управления </strong> (консоль управления IIS).</p></li>
<li><p>Скачивание и установка <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p>
<p></p>
<div class="alert">
<strong>Важно.</strong><br/><p>Вы по-прежнему можете скачать предыдущую версию KB. Однако она может быть заменена более поздней версией.</p>
</div>
<div>

</div></li>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=13523" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x64)](https://www.microsoft.com/download/details.aspx?id=13523)">Распространяемый пакет Microsoft Visual C++ 2010 с пакетом обновления 1 (64-разрядная версия)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Распространяемый пакет Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>64 — битовая регистрация ASP.NET</p></li>
</ul>
<p>Серверные компоненты App-V 5,0 являются зависимыми, но у них есть различные требования и параметры установки, которые необходимо развернуть. Используйте указанные ниже сведения, чтобы подготовить среду для работы с сервером управления App-V 5,0.</p>
<ul>
<li><p>Расположение установки: по умолчанию этот компонент будет установлен на <strong> сервер виртуализации приложений%ProgramFiles%\Microsoft </strong> .</p></li>
<li><p>Расположение базы данных управления App-V 5,0 — имя SQL Server, имя экземпляра SQL, имя базы данных.</p></li>
<li><p>Права доступа для консоли управления App-V 5,0 — это пользователь или группа, которым должен быть предоставлен доступ к консоли управления в конце развертывания. После развертывания пользователи будут иметь доступ к консоли управления, пока дополнительные администраторы не будут добавлены с помощью консоли управления.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Группы безопасности и отдельные пользователи не поддерживаются. Вы должны указать группу доменных служб Active Directory.</p>
</div>
<div>

</div></li>
<li><p>Имя веб-сайта службы управления App-V 5,0 — укажите имя веб-сайта или используйте имя по умолчанию.</p></li>
<li><p>Привязка порта службы управления App-V 5,0 — это уникальный номер порта, который не используется другим веб-сайтом на компьютере.</p></li>
<li><p>Поддержка Microsoft Silverlight – Microsoft Silverlight должна быть установлена до того, как будет доступна консоль управления. Хотя это не является требованием для развертывания, сервер должен поддерживать Microsoft Silverlight.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>База данных управления</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>База данных нужна только при использовании сервера управления App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Распространяемый пакет Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Серверные компоненты App-V 5,0 являются зависимыми, но у них есть различные требования и параметры установки, которые необходимо развернуть. Используйте следующие сведения для подготовки среды для работы с базой данных управления App-V 5,0.</p>
<ul>
<li><p>Расположение установки: по умолчанию этот компонент будет установлен на <strong> сервер Application Virtualization%ProgramFiles%\Microsoft </strong> .</p></li>
<li><p>Настраиваемое имя экземпляра SQL Server (если применимо) — формат должен быть <strong> instanceName </strong> , так как при установке предполагается, что он находится на локальном компьютере. Если задать имя в следующем формате, <strong> SVR\INSTANCE </strong> завершится сбоем.</p></li>
<li><p>Настраиваемое имя базы данных App-V 5,0 (если применимо) — необходимо указать уникальное имя базы данных. Значением по умолчанию для базы данных управления является <strong> AppVManagement </strong> .</p></li>
<li><p>Расположение сервера управления App-V 5,0 — задает учетную запись компьютера, на которой развернут сервер управления. Это значение должно быть задано в следующем формате <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>Администратор установки сервера управления App-V 5,0 — определяет учетную запись, которая будет использоваться для установки сервера управления App-V 5,0. Следует использовать следующий формат: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Агент служб Microsoft SQL Server — настройте компьютер с базой данных управления App-V 5,0 таким образом, чтобы служба агента Microsoft SQL Server автоматически перезагружалась. Дополнительные сведения см. <a href="https://go.microsoft.com/fwlink/?LinkId=273725" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://go.microsoft.com/fwlink/?LinkId=273725)"> в разделе Настройка агента SQL Server для автоматического перезапуска служб</a></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Сервер отчетов</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Распространяемый пакет Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><div class="alert">
<strong>Примечание.</strong><br/><p>Чтобы уменьшить риск нежелательных или вредоносных данных, отправляемых на сервер отчетов, необходимо ограничить доступ к веб-службе отчетов по корпоративной политике безопасности.</p>
</div>
<div>

</div>
<p>Веб-сервер Windows с ролью IIS со следующими возможностями: <strong> Общие функции HTTP </strong> (статическое содержимое и документ по умолчанию), <strong> разработка приложений </strong> (ASP.NET, расширение среды .NET, расширения ISAPI и фильтры ISAPI), <strong> Безопасность </strong> (проверка подлинности Windows, Фильтрация запросов <strong> </strong> <strong> </strong></p></li>
<li><p>64 — битовая регистрация ASP.NET</p></li>
<li><p>Расположение установки: по умолчанию этот компонент установлен на <strong> сервер Application Virtualization%ProgramFiles%\Microsoft </strong> .</p></li>
<li><p>Имя веб-сайта службы отчетов App-V 5,0 — определяет имя веб-сайта или имя, которое будет использоваться по умолчанию.</p></li>
<li><p>App-V 5,0 Привязка порта службы Reporting Service — это номер порта, который еще не используется другим веб-сайтом, работающим на компьютере.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>База данных отчетов</strong></p></td>
<td align="left"><p></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>База данных нужна только при использовании сервера отчетов App-V 5,0.</p>
</div>
<div>

</div>
<ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Распространяемый пакет Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
</ul>
<p>Серверные компоненты App-V 5,0 являются зависимыми, но у них есть различные требования и параметры установки, которые необходимо развернуть. Используйте следующие сведения, чтобы подготовить среду для запуска базы данных отчетов App-V 5,0.</p>
<ul>
<li><p>Расположение установки: по умолчанию этот компонент будет установлен на <strong> сервер Application Virtualization%ProgramFiles%\Microsoft </strong> .</p></li>
<li><p>Настраиваемое имя экземпляра SQL Server (если применимо) — формат должен быть <strong> instanceName </strong> , так как при установке предполагается, что он находится на локальном компьютере. Если задать имя в следующем формате, <strong> SVR\INSTANCE </strong> завершится сбоем.</p></li>
<li><p>Настраиваемое имя базы данных App-V 5,0 (если применимо) — необходимо указать уникальное имя базы данных. Значением по умолчанию для базы данных отчетов является <strong> AppVReporting </strong> .</p></li>
<li><p>Расположение сервера отчетов App-V 5,0 — указывает учетную запись компьютера, на которой развернут сервер отчетов. Это значение должно быть задано в следующем формате <strong> Domain\MachineAccount </strong> .</p></li>
<li><p>App-V 5,0 Reporting Server Installation Administrator — учетная запись, которая будет использоваться для установки сервера отчетов App-V 5,0. Следует использовать следующий формат: <strong> Domain\AdministratorLoginName </strong> .</p></li>
<li><p>Служба Microsoft SQL Server и служба агента Microsoft SQL Server — эти службы должны быть связаны с учетными записями пользователей, которые имеют доступ к службе запросов AD.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Сервер публикаций</strong></p></td>
<td align="left"><ul>
<li><p><a href="https://www.microsoft.com/download/details.aspx?id=17718" data-raw-source="[Microsoft .NET Framework 4 (Full Package)](https://www.microsoft.com/download/details.aspx?id=17718)">Microsoft .NET Framework 4 (полный пакет)</a></p></li>
<li><p><a href="https://go.microsoft.com/fwlink/?LinkId=267110" data-raw-source="[Microsoft Visual C++ 2010 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=267110)">Распространяемый пакет Microsoft Visual C++ 2010 SP1 (x86)</a></p></li>
<li><p>Веб-сервер Windows с ролью IIS со следующими возможностями: <strong> Общие функции HTTP </strong> (статическое содержимое и документ по умолчанию), <strong> разработка приложений </strong> (ASP.NET, расширение среды .NET, расширения ISAPI и фильтры ISAPI), <strong> Безопасность </strong> (проверка подлинности Windows, Фильтрация запросов <strong> </strong> <strong> </strong></p></li>
<li><p>64 — битовая регистрация ASP.NET</p></li>
</ul>
<p>Серверные компоненты App-V 5,0 являются зависимыми, но у них есть различные требования и параметры установки, которые необходимо развернуть. Используйте следующие сведения, чтобы подготовить среду для запуска сервера публикаций App-V 5,0.</p>
<ul>
<li><p>Расположение установки: по умолчанию этот компонент установлен на <strong> сервер Application Virtualization%ProgramFiles%\Microsoft </strong> .</p></li>
<li><p>URL-адрес службы управления App-V 5,0 — задает URL-адрес службы управления App-V 5,0. Это порт, с которым взаимодействует сервер публикаций, и он должен быть указан в следующем формате: <strong><a href="http://localhost:12345" data-raw-source="http://localhost:12345"> http://localhost:12345 </a></strong> .</p></li>
<li><p>Имя веб-сайта службы публикации App-V 5,0 — определяет имя веб-сайта или имя, которое будет использоваться по умолчанию.</p></li>
<li><p>Служба публикации для App-V 5,0 — это уникальный номер порта, который еще не используется другим веб-сайтом, работающим на компьютере.</p></li>
</ul></td>
</tr>
</tbody>
</table>

## Статьи по теме

[Планирование развертывания App-V](planning-to-deploy-app-v.md)

[Поддерживаемые конфигурации в App-V 5.0](app-v-50-supported-configurations.md)
