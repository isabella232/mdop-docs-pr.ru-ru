---
title: Предварительные требования App-V 5.1
description: Предварительные требования App-V 5.1
author: dansimp
ms.assetid: 1bfa03c1-a4ae-45ec-8a2b-b10c2b94bfb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a74d8f8d7148cdb6c32bcafa87f479d24305af
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814741"
---
# Предварительные требования App-V 5.1


Перед установкой Microsoft Application Virtualization (App-V) 5,1 Убедитесь, что установлены все перечисленные ниже необходимые компоненты.

Список поддерживаемых операционных систем и требований к оборудованию для сервера App-V, секвенсора и клиента можно найти в разделе [Поддерживаемые конфигурации App-v 5,1](app-v-51-supported-configurations.md).

## Сводка программного обеспечения, предварительно установленного в каждой операционной системе.


В приведенной ниже таблице указано программное обеспечение, которое уже установлено для разных операционных систем.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Описание предварительной проверки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10;</p></td>
<td align="left"><p>Все необходимое программное обеспечение уже установлено.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Все необходимое программное обеспечение уже установлено.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если вы используете Windows 8, обновите операционную систему до Windows 8,1, прежде чем использовать App-V 5,1.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Уже установлено следующее программное обеспечение:</p>
<ul>
<li><p>Microsoft .NET Framework 4,5</p></li>
<li><p>Windows PowerShell 3,0</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для установки PowerShell 3,0 требуется перезагрузка.</p>
</div>
<div>

</div></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>Необходимое программное обеспечение еще не установлено. Для установки App-V необходимо установить ее.</p></td>
</tr>
</tbody>
</table>



## Необходимое программное обеспечение для App-V Server


Установите необходимое программное обеспечение для серверных компонентов App-V 5,1.

### Что нужно знать перед началом работы

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Учетная запись для установки сервера App-V</p></td>
<td align="left"><p>Для учетной записи, используемой для установки серверных компонентов App-V, должны быть установлены следующие компоненты:</p>
<ul>
<li><p>Права администратора на компьютере, на котором устанавливаются компоненты.</p></li>
<li><p>Возможность запроса доменных служб Active Directory.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Порт и брандмауэр</p></td>
<td align="left"><ul>
<li><p>Укажите порт, на котором будет размещен каждый из компонентов.</p></li>
<li><p>Добавьте соответствующие правила брандмауэра, разрешающие входящие запросы на указанные порты.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Веб-сайт распределенной разработки и управления версиями (WebDAV)</p></td>
<td align="left"><p>WebDAV автоматически отключается для службы управления.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Поддерживаемые сценарии развертывания</p></td>
<td align="left"><ul>
<li><p>Отдельное развертывание, в котором все компоненты развертываются на одном и том же сервере.</p></li>
<li><p>Распределенное развертывание.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Неподдерживаемые сценарии развертывания</p></td>
<td align="left"><ul>
<li><p>Установка параллельных экземпляров нескольких серверных версий App-V на одном и том же сервере.</p></li>
<li><p>Установка серверных компонентов App-V на компьютере, на котором запущены серверные ядра или контроллер домена.</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Необходимое программное обеспечение для сервера управления

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Необходимые условия и необходимые параметры</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Поддерживаемая версия SQL Server</p></td>
<td align="left"><p>Поддерживаемые версии можно найти в разделе <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> Поддерживаемые конфигурации App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p></td>
<td align="left"><p>Для установки PowerShell 3,0 требуется перезагрузка.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Скачивание и установка <a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)"> KB2533623</a></p></td>
<td align="left"><p>Применимо только к Windows 7.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64 — битовая регистрация ASP.NET</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Роль веб-сервера Windows Server</p></td>
<td align="left"><p>Эту роль необходимо добавить в серверную операционную систему, которая поддерживается сервером управления.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Средства управления веб-сервером (IIS)</p></td>
<td align="left"><p>Выберите пункт <strong> сценарии и инструменты управления IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Службы ролей веб-сервера</p></td>
<td align="left"><p><strong>Основные возможности HTTP:</strong></p>
<ul>
<li><p>Статическое содержимое</p></li>
<li><p>Документ по умолчанию</p></li>
</ul>
<p><strong>Разработка приложений.</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Расширяемость .NET</p></li>
<li><p>Расширения ISAPI</p></li>
<li><p>Фильтры ISAPI</p></li>
</ul>
<p><strong>Разрешения</strong></p>
<ul>
<li><p>Проверка подлинности Windows</p></li>
<li><p>Фильтрация запросов</p></li>
</ul>
<p><strong>Средства управления.</strong></p>
<ul>
<li><p>Консоль управления IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Расположение для установки по умолчанию</p></td>
<td align="left"><p>Сервер Application Virtualization для%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Расположение базы данных управления</p></td>
<td align="left"><p>Имя базы данных SQL Server, имя экземпляра базы данных SQL Server и имя базы данных.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Разрешения консоли управления и базы данных управления</p></td>
<td align="left"><p>Пользователь или группа, которые могут получить доступ к консоли управления и базе данных после завершения развертывания. Только эти пользователи или группы получат доступ к консоли управления и базе данных, если только дополнительные администраторы не добавлены с помощью консоли управления.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя веб-сайта службы управления</p></td>
<td align="left"><p>Имя веб-сайта консоли управления.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Привязка порта службы управления</p></td>
<td align="left"><p>Уникальный номер порта для службы управления. Этот порт не может использоваться другим процессом на компьютере.</p></td>
</tr>
</tbody>
</table>



**Важно.**  
На веб-сайте, на котором открывается консоль управления Веба, должен быть включен JavaScript.



### Необходимое программное обеспечение для базы данных сервера управления

База данных управления является обязательной только в том случае, если вы используете сервер App-V 5,1 Management Server.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Необходимые условия и необходимые параметры</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Расположение для установки по умолчанию</p></td>
<td align="left"><p>Сервер Application Virtualization для%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="even">
<td align="left"><p>Настраиваемое имя экземпляра SQL Server (если применимо)</p></td>
<td align="left"><p>Формат для использования: <strong> instanceName</strong></p>
<p>Этот формат основывается на предположении, что установка находится на локальном компьютере.</p>
<p>Если задать имя в формате <strong> SVR\INSTANCE </strong> , установка завершится сбоем.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя настраиваемой базы данных (если применимо)</p></td>
<td align="left"><p>Уникальное имя базы данных.</p>
<p>По умолчанию: AppVManagement</p></td>
</tr>
<tr class="even">
<td align="left"><p>Расположение сервера управления</p></td>
<td align="left"><p>Учетная запись компьютера, на которой развернут сервер управления.</p>
<p>Формат для использования: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Администратор установки сервера управления</p></td>
<td align="left"><p>Учетная запись, используемая для установки сервера управления.</p>
<p>Формат для использования: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Агент служб Microsoft SQL Server</p></td>
<td align="left"><p>Настройка компьютера базы данных управления для автоматического запуска службы агента Microsoft SQL Server. Инструкции можно найти <a href="https://technet.microsoft.com/magazine/gg313742.aspx" data-raw-source="[Configure SQL Server Agent to Restart Services Automatically](https://technet.microsoft.com/magazine/gg313742.aspx)"> в разделе Настройка агента SQL Server для автоматического перезапуска служб </a> .</p></td>
</tr>
</tbody>
</table>



### Необходимое программное обеспечение сервера публикаций

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Необходимые условия и необходимые параметры</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>64 — битовая регистрация ASP.NET</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Роль веб-сервера Windows Server</p></td>
<td align="left"><p>Эту роль необходимо добавить в серверную операционную систему, которая поддерживается сервером управления.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Средства управления веб-сервером (IIS)</p></td>
<td align="left"><p>Выберите пункт <strong> сценарии и инструменты управления IIS </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Службы ролей веб-сервера</p></td>
<td align="left"><p><strong>Основные возможности HTTP:</strong></p>
<ul>
<li><p>Статическое содержимое</p></li>
<li><p>Документ по умолчанию</p></li>
</ul>
<p><strong>Разработка приложений.</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Расширяемость .NET</p></li>
<li><p>Расширения ISAPI</p></li>
<li><p>Фильтры ISAPI</p></li>
</ul>
<p><strong>Разрешения</strong></p>
<ul>
<li><p>Проверка подлинности Windows</p></li>
<li><p>Фильтрация запросов</p></li>
</ul>
<p><strong>Средства управления.</strong></p>
<ul>
<li><p>Консоль управления IIS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Расположение для установки по умолчанию</p></td>
<td align="left"><p>Сервер Application Virtualization для%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="even">
<td align="left"><p>URL-адрес службы управления</p></td>
<td align="left"><p>URL-адрес службы управления App-V. Это порт, с которым обменивается данными сервер публикаций.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Архитектура установки</th>
<th align="left">Формат, используемый для URL-адреса</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер управления и сервер публикаций установлены на одном и том же сервере</p></td>
<td align="left"><p><a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Сервер управления и сервер публикаций установлены на разных серверах</p></td>
<td align="left"><p><a href="http://MyAppvServer.MyDomain.com" data-raw-source="http://MyAppvServer.MyDomain.com">http://MyAppvServer.MyDomain.com</a></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя веб-сайта службы публикации</p></td>
<td align="left"><p>Имя веб-сайта публикации.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Привязка порта службы публикации</p></td>
<td align="left"><p>Уникальный номер порта для службы публикации. Этот порт не может использоваться другим процессом на компьютере.</p></td>
</tr>
</tbody>
</table>



### Необходимое программное обеспечение сервера отчетов

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Необходимые условия и необходимые параметры</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Поддерживаемая версия SQL Server</p></td>
<td align="left"><p>Поддерживаемые версии можно найти в разделе <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> Поддерживаемые конфигурации App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>64 — битовая регистрация ASP.NET</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Роль веб-сервера Windows Server</p></td>
<td align="left"><p>Эту роль необходимо добавить в серверную операционную систему, которая поддерживается сервером управления.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Средства управления веб-сервером (IIS)</p></td>
<td align="left"><p>Выберите пункт <strong> сценарии и инструменты управления IIS </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Службы ролей веб-сервера</p></td>
<td align="left"><p>Для снижения риска нежелательных или вредоносных данных, отправляемых на сервер отчетов, необходимо ограничить доступ к веб-службе отчетов по корпоративной политике безопасности.</p>
<p><strong>Основные возможности HTTP:</strong></p>
<ul>
<li><p>Статическое содержимое</p></li>
<li><p>Документ по умолчанию</p></li>
</ul>
<p><strong>Разработка приложений.</strong></p>
<ul>
<li><p>ASP.NET</p></li>
<li><p>Расширяемость .NET</p></li>
<li><p>Расширения ISAPI</p></li>
<li><p>Фильтры ISAPI</p></li>
</ul>
<p><strong>Разрешения</strong></p>
<ul>
<li><p>Проверка подлинности Windows</p></li>
<li><p>Фильтрация запросов</p></li>
</ul>
<p><strong>Средства управления.</strong></p>
<ul>
<li><p>Консоль управления IIS</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Расположение для установки по умолчанию</p></td>
<td align="left"><p>Сервер Application Virtualization для%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя веб-сайта службы отчетов</p></td>
<td align="left"><p>Имя веб-сайта отчетов.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Привязка порта службы отчетов</p></td>
<td align="left"><p>Уникальный номер порта для службы отчетов. Этот порт не может использоваться другим процессом на компьютере.</p></td>
</tr>
</tbody>
</table>



### Предварительное программное обеспечение для базы данных отчетов

База данных отчетов требуется только в том случае, если вы используете сервер App-V 5,1 Reporting Server.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Необходимые условия и необходимые параметры</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Расположение для установки по умолчанию</p></td>
<td align="left"><p>Сервер Application Virtualization для%PROGRAMFILES%\Microsoft</p></td>
</tr>
<tr class="even">
<td align="left"><p>Настраиваемое имя экземпляра SQL Server (если применимо)</p></td>
<td align="left"><p>Формат для использования: <strong> instanceName</strong></p>
<p>Этот формат основывается на предположении, что установка находится на локальном компьютере.</p>
<p>Если задать имя в формате <strong> SVR\INSTANCE </strong> , установка завершится сбоем.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Имя настраиваемой базы данных (если применимо)</p></td>
<td align="left"><p>Уникальное имя базы данных.</p>
<p>По умолчанию: AppVReporting</p></td>
</tr>
<tr class="even">
<td align="left"><p>Расположение сервера отчетов</p></td>
<td align="left"><p>Учетная запись компьютера, на которой развернут сервер отчетов.</p>
<p>Формат для использования: Domain\MachineAccount</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Администратор установки сервера отчетов</p></td>
<td align="left"><p>Учетная запись, используемая для установки сервера отчетов.</p>
<p>Формат для использования: Domain\AdministratorLoginName</p></td>
</tr>
<tr class="even">
<td align="left"><p>Служба Microsoft SQL Server и агент служб Microsoft SQL Server</p></td>
<td align="left"><p>Настройте эти службы, чтобы они были связаны с учетными записями пользователей, которые имеют доступ к службе AD DS.</p></td>
</tr>
</tbody>
</table>



## Необходимое программное обеспечение клиента App-V


Установите следующее программное обеспечение, необходимое для клиента App-V.

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>Для установки PowerShell 3,0 требуется перезагрузка.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Применимо только к Windows 7: скачивание и установка KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Необходимое программное обеспечение клиента служб удаленных рабочих столов


Установите следующее программное обеспечение, необходимое для клиента служб удаленных рабочих столов App-V.

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>Для установки PowerShell 3,0 требуется перезагрузка.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Применимо только к Windows 7: скачивание и установка KB.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=40784" data-raw-source="[Visual C++ Redistributable Packages for Visual Studio 2013](https://www.microsoft.com/download/details.aspx?id=40784)">Распространяемые пакеты Visual C++ для Visual Studio 2013</a></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



## Программное обеспечение программы Sequencer


**Что необходимо знать перед установкой необходимых компонентов:**

-   Рекомендация: на компьютере, на котором работает секвенсор, должны быть те же конфигурации оборудования и программного обеспечения, что и на компьютерах, на которых будут запускаться виртуальные приложения.

-   Процесс упорядочения занимает много ресурсов, поэтому убедитесь, что на компьютере, на котором работает секвенсор, достаточно памяти, быстрого процессора и быстрого жесткого диска. Системные требования, предъявляемые локально установленными приложениями, не могут превышать возможности секвенсора. Дополнительные сведения можно найти в разделе [Поддерживаемые конфигурации App-V 5,1](app-v-51-supported-configurations.md).

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
<td align="left"><p><a href="https://www.microsoft.com//download/details.aspx?id=40773" data-raw-source="[Microsoft .NET Framework 4.5.1 (Web Installer)](https://www.microsoft.com//download/details.aspx?id=40773)">Microsoft .NET Framework 4.5.1 (веб-установщик)</a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="https://www.microsoft.com/download/details.aspx?id=34595" data-raw-source="[Windows PowerShell 3.0](https://www.microsoft.com/download/details.aspx?id=34595)">Windows PowerShell 3,0</a></p>
<p></p></td>
<td align="left"><p>Для установки PowerShell 3,0 требуется перезагрузка.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="https://support.microsoft.com/kb/2533623" data-raw-source="[KB2533623](https://support.microsoft.com/kb/2533623)">KB2533623</a></p></td>
<td align="left"><p>Применимо только к Windows 7: скачивание и установка KB.</p></td>
</tr>
</tbody>
</table>








## Статьи по теме


[Планирование использования App-V 5.1](planning-for-app-v-51.md)

[Поддерживаемые конфигурации в App-V 5.1](app-v-51-supported-configurations.md)









