---
title: Настройка веб-приложений MBAM 2.5
description: Настройка веб-приложений MBAM 2.5
author: dansimp
ms.assetid: 909bf2d3-028c-4ac1-9247-171532a1eeae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0336d24f51167a00c8565ccd081f4bc5dfb2c4cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824499"
---
# Настройка веб-приложений MBAM 2.5


В этой статье объясняется, как настроить веб-приложения Microsoft BitLocker Administration и Monitoring (MBAM) 2,5 для рекомендованной [высокоуровневой архитектуры для MBAM 2,5](high-level-architecture-for-mbam-25.md) с помощью одного из указанных ниже способов.

-   Командлет Windows PowerShell

-   Мастер настройки сервера MBAM

Веб-приложения состоят из указанных ниже веб-служб и соответствующих им.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Веб-сайт</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Веб-сайт администрирования и мониторинга</p></td>
<td align="left"><p>Веб-сайт, на котором пользователи могут просматривать отчеты и помогать пользователям восстанавливать свои компьютеры после того, как они забывают PIN-код или пароль</p></td>
</tr>
<tr class="even">
<td align="left"><p>Портал самообслуживания</p></td>
<td align="left"><p>Веб-сайт, с которого конечные пользователи могут получить доступ к своим компьютерам независимо от того, забыли ли вы свой PIN-код или пароль</p></td>
</tr>
</tbody>
</table>



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
<td align="left"><p>Заполните необходимые условия на каждом сервере.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Убедитесь, что вы настроили службы SQL ServerReporting (SSRS) для использования протокола SSL (Secure Sockets Layer) перед настройкой веб-сайта администрирования и мониторинга. В противном случае функция "отчеты" будет использовать HTTP вместо HTTPS.</p>
</div>
<div>

</div></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Необходимые условия MBAM 2.5 Server для изолированной топологии и топологии интеграции диспетчера конфигураций</a></p></li>
<li><p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Требования к серверу MBAM 2,5, применимые только к топологии интеграции Configuration Manager </a> (если применимо)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Зарегистрируйте имена участников службы (SPN) для учетной записи пула приложений для веб-сайтов. Этот шаг необходимо выполнить только в том случае, если у вас нет прав администратора домена в доменных службах Active Directory (AD DS). Если у вас есть эти права в доменных СЛУЖБах Active Directory, MBAM создаст SPN.</p></td>
<td align="left"><p><a href="planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn" data-raw-source="[Planning How to Secure the MBAM Websites](planning-how-to-secure-the-mbam-websites.md#bkmk-regvirtualspn)">Планирование защиты веб-сайтов MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Установка программного обеспечения сервера MBAM на каждый сервер, на котором будет настроена функция сервера MBAM.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если вы планируете установить сайты на одном сервере и веб-службах на другом, вы сможете настроить их только с помощью <strong> </strong> командлета Windows PowerShell Enable-MbamWebApplication. Мастер настройки сервера MBAM не поддерживает настройку этих элементов на отдельных серверах.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Установка программного обеспечения MBAM 2.5 Server</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Если вы планируете использовать командлеты для настройки функций сервера MBAM, изучите необходимые условия для использования Windows PowerShell.</p></td>
<td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Настройка компонентов MBAM 2.5 Server с помощью Windows PowerShell</a></p></td>
</tr>
</tbody>
</table>



**Настройка веб-приложений с помощью Windows PowerShell**

1.  Прежде чем приступить к настройке, прочтите раздел [Настройка функций сервера MBAM 2,5 с помощью Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) , чтобы просмотреть предварительные требования для использования Windows PowerShell.

2.  Используйте командлет **Enable-MbamWebApplication** , чтобы настроить веб-приложения с помощью Windows PowerShell. Чтобы получить сведения об этом командлете, введите **Get-Help Enable-MbamWebApplication**.

**Настройка параметров для всех веб-приложений с помощью мастера**

1. На сервере, на котором вы хотите настроить веб-приложения, запустите мастер настройки сервера MBAM. Чтобы открыть мастер, вы можете выбрать **MBAM конфигурации сервера** в меню " **Пуск** ".

2. Нажмите кнопку **Добавить новые функции**, выберите **Администрирование и мониторинг на веб-сайте администрирования** и **на портале самообслуживания**, а затем нажмите кнопку **Далее**. Мастер проверяет, выполнены ли все необходимые условия для веб-приложений.

3. Если проверка готовности к установке выполнена успешно, нажмите кнопку **Далее** , чтобы продолжить. В противном случае устраните недостающие необходимые компоненты и нажмите кнопку **проверить необходимые компоненты еще раз**.

4. Чтобы ввести значения полей в мастере, воспользуйтесь приведенными ниже описаниями.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><strong>Поле</strong></th>
   <th align="left">Описание</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Сертификат безопасности</strong></p></td>
   <td align="left"><p>Выберите ранее созданный сертификат, чтобы дополнительно зашифровать связь между веб-службами и сервером, на котором вы настраиваете веб-сайты. Если вы выберете параметр <strong> не использовать сертификат </strong> , ваш веб-канал может быть небезопасным.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Имя узла</strong></p></td>
   <td align="left"><p>Имя главного компьютера, на котором вы настраиваете веб-сайты.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Путь установки</strong></p></td>
   <td align="left"><p>Путь к папке, в которую устанавливаются веб-сайты.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Port</strong></p></td>
   <td align="left"><p>Номер порта, используемый для связи с веб-сайтом и службами.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Необходимо настроить исключение брандмауэра, чтобы разрешить связь через указанный порт.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Учетная запись домена и пароль для пула приложений веб-службы</strong></p></td>
   <td align="left"><p>Учетная запись пользователя домена и пароль для пула приложений веб-службы.</p>
   <p>Если вы ввели имя пользователя в поле " <strong> пользователь или группа домена доступа для чтения и записи" </strong> на <strong> странице "Настройка баз данных" </strong> , необходимо ввести это же значение в это поле.</p>
   <p>Если вы ввели имя группы в <strong> поле пользователя или группы домена "доступ для чтения и записи" </strong> на <strong> странице "Настройка баз данных" </strong> , то значение, введенное в этом поле, должно быть членом этой группы.</p>
   <p>Если вы не указали учетные данные, будет использоваться учетная запись, указанная для любого ранее включенного веб-приложения. Все веб-приложения должны использовать одни и те же учетные данные пула приложений. Если вы укажете разные учетные данные для разных веб-приложений, будет использоваться Последнее указанное значение.</p>
   <div class="alert">
   <strong>Важно.</strong><br/><p>Для повышения безопасности настройте учетную запись, указанную в учетных данных, с ограниченными правами пользователя. Кроме того, установите для пароля учетной записи значение бессрочной.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



5. Убедитесь в том, что встроенная учетная запись IIS \ _IUSRS или учетная запись пула приложений добавлена в средство **олицетворения клиента после проверки подлинности** и локальных параметров безопасности для **входа в качестве пакетного задания** .

   Чтобы убедиться в том, что он был добавлен к локальным параметрам безопасности, откройте **Редактор локальной политики безопасности**, разверните узел **Локальные политики** , щелкните узел **Назначение прав пользователя** и дважды щелкните команду **Олицетворять клиента после проверки подлинности** и войдите в систему **как правила пакетных заданий** в области справа.

**Настройка сведений о соединении для баз данных с помощью мастера**

1.  Используйте следующие описания полей для настройки сведений о соединении в мастере для базы данных соответствия требованиям и аудита.

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
    <td align="left"><p>Имя сервера, на котором настроена база данных соответствия и аудита.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Экземпляр базы данных SQL Server</strong></p></td>
    <td align="left"><p>Имя экземпляра SQL Server, на котором настроена конфигурация базы данных соответствия требованиям и аудита.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Имя базы данных</strong></p></td>
    <td align="left"><p>Имя базы данных соответствия требованиям и аудита.</p></td>
    </tr>
    </tbody>
    </table>



2.  Используйте следующие описания полей для настройки сведений о подключении в мастере для базы данных восстановления.

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
    <td align="left"><p>Имя сервера, на котором настроена база данных восстановления.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Экземпляр базы данных SQL Server</strong></p></td>
    <td align="left"><p>Имя экземпляра SQL Server, на котором настроена база данных восстановления.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Имя базы данных</strong></p></td>
    <td align="left"><p>Имя базы данных восстановления.</p></td>
    </tr>
    </tbody>
    </table>



**Настройка веб-приложений с помощью мастера**

1. Используйте следующие описания для ввода значений полей в мастере, чтобы настроить веб-сайт администрирования и мониторинга.

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
   <td align="left"><p><strong>Группа домена "Расширенная роль в справочной службе"</strong></p></td>
   <td align="left"><p>Группа пользователей домена, у которой есть доступ ко всем областям на веб-сайте администрирования и наблюдения за исключением области "отчеты".</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Группа домена "роль в справочной службе"</strong></p></td>
   <td align="left"><p>Группа пользователей домена, у которых есть доступ к <strong> </strong> <strong> разделу Управление областями восстановления доверенных платформенных устройств и дисков на </strong> веб-сайте администрирования и мониторинга.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Использование интеграции System Center Configuration Manager</strong></p></td>
   <td align="left"><p>Установите этот флажок, если вы настраиваете MBAM с помощью топологии интеграции Configuration Manager. При установке этого флажка все отчеты, кроме отчета об аудите восстановления, отображаются в диспетчере конфигураций, а не на веб-сайте администрирования и наблюдения.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Группа домена "роль отчета"</strong></p></td>
   <td align="left"><p>Группа пользователей домена, у участников которой есть доступ только для чтения к области "отчеты" на веб-сайте администрирования и мониторинга.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>URL-адрес служб SQL Server Reporting Services</strong></p></td>
   <td align="left"><p>URL-адрес сервера служб SSRS, на котором настроены отчеты MBAM.</p>
   <p>Примеры URL-адресов отчета:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Тип имени узла</th>
   <th align="left">Пример.</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Пример с полным доменным именем</p></td>
   <td align="left"><p><a href="https://MyReportServer.Contoso.com/ReportServer" data-raw-source="https://MyReportServer.Contoso.com/ReportServer">https://MyReportServer.Contoso.com/ReportServer</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Пример с именем настраиваемого узла</p></td>
   <td align="left"><p><a href="https://MyReportServer/ReportServer" data-raw-source="https://MyReportServer/ReportServer">https://MyReportServer/ReportServer</a></p></td>
   </tr>
   </tbody>
   </table>
   <p> </p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Виртуальный каталог</strong></p></td>
   <td align="left"><p>Виртуальный каталог на веб-сайте администрирования и мониторинга. Это имя соответствует физическому каталогу веб-сайта на сервере и добавляется к имени узла веб-сайта, например:</p>
   <p>HTTP (s):// &lt; <em> HostName </em> &gt; : &lt; <em> Port </em> &gt; /HelpDesk/</p>
   <p>Если вы не укажете виртуальный каталог, <strong> будет использоваться служба поддержки по стоимости </strong> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Группа домена роль миграции данных </strong> (необязательный)</p></td>
   <td align="left"><p>Группа пользователей домена, у которых есть доступ к данным о восстановлении через эту конечную точку, с помощью командлетов Write-MBAM * Information.</p></td>
   </tr>
   </tbody>
   </table>



2. Для ввода значений полей в мастере для настройки портала самообслуживания используйте следующее описание.

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
   <td align="left"><p><strong>Виртуальный каталог</strong></p></td>
   <td align="left"><p>Виртуальный каталог веб-приложения. Это имя соответствует физическому каталогу веб-сайта на сервере и добавляется к имени узла веб-сайта, например:</p>
   <p>HTTP (s):// &lt; <em> HostName </em> &gt; : &lt; <em> Port </em> &gt; /Selfservice/</p>
   <p>Если вы не указали виртуальный каталог, <strong> будет использоваться значение Selfservice </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Название организации</p></td>
   <td align="left"><p>Укажите название компании для портала самообслуживания, например:</p>
   <p>Contoso IT</p>
   <p>Это название компании отображается для всех пользователей портала самообслуживания.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Текст URL-адреса службы поддержки</p></td>
   <td align="left"><p>Укажите текстовую инструкцию, которая направляет пользователей на веб-сайт службы поддержки Организации, например:</p>
   <p>Обращение в службу технической поддержки или ИТ-отдел</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>URL-адрес службы поддержки</p></td>
   <td align="left"><p>Укажите URL-адрес сайта технической поддержки своей организации, например:</p>
   <p>HTTP (s):// &lt; <em> companyHelpdeskURL</em>&gt;/</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Текстовый файл с примечанием</p></td>
   <td align="left"><p>Выберите файл, содержащий уведомление, которое должно отображаться для пользователей на начальной странице портала самообслуживания.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Не отображать текст уведомления для пользователей</p></td>
   <td align="left"><p>Установите этот флажок, чтобы указать, что текст уведомления не отображается для пользователей.</p></td>
   </tr>
   </tbody>
   </table>



3. Когда вы закончите ввод, нажмите кнопку **Далее**.

   Мастер проверяет, выполнены ли все необходимые условия для веб-приложений.

4. Чтобы продолжить, нажмите **Далее**.

5. На странице **сводки** ознакомьтесь с возможностями, которые будут добавлены.

   **Примечание.**  
   Чтобы создать сценарий Windows PowerShell для записей, которые вы создали, нажмите **экспортировать сценарий PowerShell** и сохранить сценарий.



6. Нажмите кнопку **Добавить** , чтобы добавить веб-приложения на сервер, а затем нажмите кнопку **Закрыть**.

   Чтобы настроить портал самообслуживания, добавив настраиваемый текст уведомления, название компании, ссылки на дополнительные сведения и т. д., ознакомьтесь с [Разстройкой портала самообслуживания для своей организации](customizing-the-self-service-portal-for-your-organization.md).

**Настройка портала самообслуживания, если клиентские компьютеры не могут получить доступ к сети CDN**

1.  Определите, используете ли вы Microsoft BitLocker администрирование и мониторинг (MBAM) 2,5 с пакетом обновления 1 (SP1). Если да, ничего делать не нужно. Настройка портала самообслуживания завершена.

    **Примечание.**  
    Администрирование и мониторинг Microsoft BitLocker (MBAM) 2,5 с пакетом обновления 1 (SP1) устанавливает файлы JavaScript в настройке, поэтому для настройки портала самообслуживания не требуется подключение к сети доставки содержимого Microsoft AJAX. Описанные ниже действия необходимы только в том случае, если вы используете версию администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5, предшествующую пакету обновления 1 (SP1).



2.  Определение того, есть ли у клиентских компьютеров доступ к сети доставки содержимого (CDN) Microsoft AJAX.

    Сеть CDN предоставляет порталу самообслуживания, доступ к которому требуется для определенных файлов JavaScript. Если вы не настраиваете портал самообслуживания, когда клиентские компьютеры не могут получить доступ к сети CDN, будет отображаться только название компании и учетная запись, под которой вошел конечный пользователь. Сообщение об ошибке не выводится.

3.  Выполните одно из следующих действий.

    -   Если клиентские компьютеры имеют доступ к сети CDN, ничего делать не нужно. Настройка портала самообслуживания завершена.

    -   Если клиентские компьютеры не имеют доступа к сети CDN, выполните действия, описанные в разделе [Настройка портала самообслуживания, когда клиентские компьютеры не могут получить доступ к Интернету для доставки содержимого](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).


## Статьи по теме


[Журналы событий сервера](server-event-logs.md)

[Настройка компонентов сервера MBAM 2.5 Server](configuring-the-mbam-25-server-features.md)

[Настройка портала самообслуживания при отсутствии у клиентских компьютеров доступа к сети доставки содержимого корпорации Майкрософт](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md)

[Настройка портала самообслуживания для организации](customizing-the-self-service-portal-for-your-organization.md)

[Проверка конфигурации компонентов MBAM 2.5 Server](validating-the-mbam-25-server-feature-configuration.md)



## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





