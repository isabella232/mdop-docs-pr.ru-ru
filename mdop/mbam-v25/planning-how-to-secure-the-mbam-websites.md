---
title: Планирование защиты веб-сайтов MBAM
description: Планирование защиты веб-сайтов MBAM
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825022"
---
# Планирование защиты веб-сайтов MBAM


В этой статье описаны следующие методы обеспечения безопасности администрирования и мониторинга Microsoft BitLocker (MBAM) 2,5 и веб-сайта мониторинга и самообслуживания.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Обязательный или необязательный?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Использование сертификатов для обеспечения безопасности веб-сайтов MBAM</p></td>
<td align="left"><p>Необязательно, но настоятельно рекомендуется</p></td>
</tr>
<tr class="even">
<td align="left"><p>Регистрация имен участников-служб (SPN) для учетной записи пула приложений</p></td>
<td align="left"><p>Обязательный</p></td>
</tr>
</tbody>
</table>



Дополнительные сведения о том, как защитить развертывание MBAM, можно найти в статьях [вопросы безопасности в MBAM 2,5](mbam-25-security-considerations.md).

## Использование сертификатов для обеспечения безопасности веб-сайтов MBAM


Мы рекомендуем использовать сертификат для обеспечения взаимодействия между абонентами:

-   Клиент MBAM и веб-службы

-   Браузер и веб-сайт администрирования и мониторинга и веб-сайты портала самообслуживания

Сведения о том, как запросить и установить сертификат, приведены в разделе [Настройка сертификатов Интернет-сервера](https://technet.microsoft.com/library/cc731977.aspx).

**Примечание.**  
Вы можете настроить веб-сайты и веб-службы на разных серверах только в том случае, если вы используете Windows PowerShell. Если вы используете мастер настройки сервера MBAM для настройки сайтов, необходимо настроить веб-сайты и веб-службы на одном и том же сервере.



Для обеспечения безопасности связи между веб-службами и базами данных мы также рекомендуем принудительно использовать шифрование в SQL Server. Сведения о защите всех подключений к SQL Server, в том числе о связи между веб-службами и SQL Server, можно найти в разделе [вопросы безопасности в MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).

## Регистрация SPN для учетной записи пула приложений


Чтобы разрешить серверам MBAM возможность проверки подлинности связи на веб-сайте администрирования и мониторинга и на портале самообслуживания, необходимо зарегистрировать имя участника-службы (SPN) для имени узла в учетной записи домена, которую вы используете для работы с этим пулом приложений.

В этой статье приведены инструкции по регистрации SPN для следующих типов имен узлов.

-   Полное доменное имя

-   Имя NetBIOS

-   Виртуальное имя

### Перед созданием SPN для начальной установки MBAM

Прежде чем приступить к созданию SPN, ознакомьтесь со сведениями в приведенной ниже таблице.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача или элемент</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Создание учетной записи службы в доменных службах Active Directory (AD DS).</p></td>
<td align="left"><p>Учетная запись службы — это учетная запись пользователя, созданная в доменных СЛУЖБах Active Directory для обеспечения безопасности веб-сайтов MBAM. Веб-сайты MBAM выполняются в пуле приложений, удостоверением которого является имя учетной записи службы. Затем SPN регистрируются в учетной записи пула приложений.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Для всех веб-серверов необходимо использовать одну и ту же учетную запись пула приложений.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Убедитесь в том, что учетной записи группы IIS-IUSR или учетной записи пула приложений предоставлены необходимые права.</p></td>
<td align="left"><p>Чтобы проверить это, выполните указанные ниже действия.</p>
<ol>
<li><p>Откройте <strong> Редактор локальной политики безопасности </strong> и разверните <strong> узел Локальные политики </strong> .</p></li>
<li><p>Выберите <strong> узел Назначение прав пользователей </strong> и дважды щелкните <strong> олицетворение клиента после проверки подлинности и войдите в систему в </strong> <strong> качестве параметров групповой политики для пакетного задания </strong> в области справа.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>Если вы настроили веб-сайты MBAM с помощью учетной записи администратора домена, MBAM создаст SPN.</p></td>
<td align="left"><p>Если вы настроили веб-сайты MBAM с помощью учетной записи администратора домена, выполните действия, описанные в этой статье, чтобы зарегистрировать SPN вручную для типа имени узла, которое вы используете.</p></td>
</tr>
</tbody>
</table>



### Регистрация SPN при использовании полного доменного имени узла

Если вы используете полное доменное имя узла при настройке MBAM, вам нужно зарегистрировать только одно SPN, как показано в следующем примере.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Что вам нужно сделать?</th>
<th align="left">Примеры и дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Зарегистрируйте имя SPN для полного доменного имени.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>Полное имя узла — <strong> mybitlockerrecovery.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройка ограниченного делегирования для SPN, регистрируемого для учетной записи пула приложений.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Настройка ограниченного делегирования</a></p>
<p>Это требование применимо только к MBAM 2,5; Это не обязательно в MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### Регистрация SPN при использовании имени узла NetBIOS

Если вы используете имя узла NetBIOS при настройке MBAM, зарегистрируйте одно SPN для имени NetBIOS и другое имя SPN для полного доменного имени, как показано в следующих примерах.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Что вам нужно сделать?</th>
<th align="left">Примеры и дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Зарегистрируйте имя участника-службы для имени узла NetBIOS.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>Имя узла NetBIOS — <strong> nbname01 </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Зарегистрируйте имя SPN для полного доменного имени.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>Полное доменное имя — <strong> nbname01.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Настройте ограниченное делегирование для имен участников, которые регистрируются для учетной записи пула приложений.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Настройка ограниченного делегирования</a></p>
<p>Это требование применимо только к MBAM 2,5; Это не обязательно в MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>Регистрация SPN при использовании имени виртуального узла

Если вы настроили MBAM с помощью имени виртуального узла, которое является полным доменным именем, зарегистрируйте только одно SPN для имени виртуального узла. Если настраиваемое имя виртуального узла не является полным доменным именем, необходимо создать второе SPN, которое указывает полное доменное имя, как описано в приведенных ниже примерах.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Что вам нужно сделать?</th>
<th align="left">Примеры и дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Если имя виртуального узла является полным доменным именем, как показано в этом примере, зарегистрируйте только одно SPN.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>В примере именем виртуального узла является <strong> mbamvirtual.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Зарегистрируйте это дополнительное SPN, если имя виртуального узла не является полным доменным именем.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>В примере именем виртуального узла является <strong> mbamvirtual </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Зарегистрируйте это дополнительное SPN, если имя виртуального узла не является полным доменным именем.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>В примере именем виртуального узла является <strong> mbamvirtual.contoso.com </strong> , а учетная запись домена, используемая для пула веб-приложений, — <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>На сервере доменных имен (DNS) создайте запись "A Record" для имени пользовательского узла и укажите его веб-серверу или подсистеме балансировки нагрузки.</p></td>
<td align="left"><p>Ознакомьтесь с разделом "Настройка DNS HOST A Records" для <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> настройки записей узлов DNS </a> .</p>
<p>Мы рекомендуем использовать записи вместо CNAME. Если вы используете CNAME для указания на адрес домена, необходимо также зарегистрировать SPN для имени веб-сервера в учетной записи пула приложений.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Настройте ограниченное делегирование для имен участников, которые регистрируются для учетной записи пула приложений.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Настройка ограниченного делегирования</a></p>
<p>Это требование применимо только к MBAM 2,5; Это не обязательно в MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>Регистрация SPN при обновлении предыдущей версии MBAM

Выполните действия, описанные в этом разделе, только в том случае, если вы хотите:

-   Переход с предыдущей версии MBAM.

-   Запустите веб-сайты в MBAM 2,5 в сбалансированной или распределенной конфигурации, и вы работаете в конфигурации, которая не сбалансирована в нагрузки.

Если вы уже зарегистрировали SPN в учетной записи компьютера, а не в учетной записи пула приложений, MBAM использует существующие SPN, и вы не сможете настроить веб-сайты в балансировке нагрузки или распределенной конфигурации.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Что вам нужно сделать?</th>
<th align="left">Примеры и дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Создайте учетную запись пула приложений в доменных службах Active Directory (AD DS).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Удалите установленные веб-сайты и веб-службы.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">Удаление компонентов или программного обеспечения MBAM Server</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Удалите SPN из учетной записи компьютера.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Зарегистрируйте SPN в учетной записи пула приложений.</p></td>
<td align="left"><p>Следуйте указаниям для <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> регистрации SPN при использовании имени виртуального узла </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Перенастройте веб-приложения и веб-службы.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Настройка веб-приложений MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Выполните одно из указанных ниже действий в зависимости от того, какой метод вы используете для настройки.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Способ</th>
<th align="left">Подробности</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Мастер настройки сервера MBAM</strong></p></td>
<td align="left"><p>Введите учетную запись пула приложений в <strong> поле Учетная запись домена пула приложений веб-службы </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Командлет Windows PowerShell</p></td>
<td align="left"><p>Введите учетную запись в <code>WebServiceApplicationPoolCredential</code> параметре.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>Важно.</strong><br/><p>Имя узла, которое вы ввели, должно совпадать с именем виртуального узла, для которого создаются SPN. Кроме того, в веб-ферме имена узлов и учетные данные пула приложений должны быть одинаковыми на каждом сервере, который вы настраиваете.</p>
</div>
<div>

</div>
<p>Когда MBAM настраивает веб-приложения, он попытается зарегистрировать SPN, но это может сделать только если у вас есть права администратора домена на сервере, на котором выполняется установка MBAM. Если у вас нет этих прав, вы можете завершить настройку, но вам придется задать имена участников службы до или после настройки MBAM.</p></td>
</tr>
</tbody>
</table>

## Обязательные параметры фильтрации запросов

 "Разрешить неуказанные расширения имен файлов" требуется, чтобы приложение работало надлежащим образом.  Это можно найти в разделе Фильтрация запросов на администрирование и мониторинг Microsoft BitLocker — > > изменить параметры компонента.


## Статьи по теме


[Подготовка среды для развертывания MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Необходимые условия для развертывания MBAM 2.5](mbam-25-deployment-prerequisites.md)





## У вас есть предложение MBAM?
- Здесь вы можете добавить предложения и проголосовать [здесь](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Для MBAM проблемы используйте [MBAM Форум TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



