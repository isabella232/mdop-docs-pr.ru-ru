---
title: Сценарии использования серверов с выходом в Интернет в сети периметра
description: Сценарии использования серверов с выходом в Интернет в сети периметра
author: dansimp
ms.assetid: 8a4da6e6-82c7-49e5-b9b1-1666cba02f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7415cf7a97edc646653df552723667bac8d25fdc
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910694"
---
# <a name="internet-facing-server-scenarios-for-perimeter-networks"></a>Сценарии использования серверов с выходом в Интернет в сети периметра


App-V 4.5 поддерживает сценарии серверов с подключением к Интернету, в которых пользователи, не подключенные к корпоративной сети или отключенные от сети, по-прежнему могут использовать App-V. Как показано на следующем рисунке, поддерживается только использование безопасных протоколов в Интернете (RTSPS и HTTPS).

![схема позиционирования брандмауэра app-v.](images/appvfirewalls.gif)

Вы можете настроить решение с подключением к Интернету с помощью isA Server, в котором инфраструктура App-V находится во внутренней сети следующим образом:

-   Создайте правило веб-публикации для сервера IIS, на который размещены файлы ICO и OSD, а также необязательно пакеты для потоковой передачи, расположенные во внутренней сети. Подробные действия предоставляются по <https://go.microsoft.com/fwlink/?LinkId=151982> .

-   Создание правила публикации сервера для сервера веб-управления App-V (RTSPS). Подробные действия предоставляются по [https://go.microsoft.com/fwlink/?LinkId=151983&](https://go.microsoft.com/fwlink/?LinkId=151983) .

Как показано на следующем примере, если инфраструктура реализовала другие брандмауэры между клиентом и сервером ISA Server или между сервером ISA Server и внутренней сетью, необходимо создать правила брандмауэра RTSPS (TCP 322) и HTTPS (TCP 443) для поддержки потока трафика. Кроме того, если брандмауэры реализованы между сервером ISA Server и внутренней сетью, трафик по умолчанию, необходимый для участников домена, должен быть разрешен для туннеля через брандмауэр (DNS, LDAP, Kerberos, SMB/CIFS).

![схема сетевого брандмауэра периметра app-v.](images/appvperimeternetworkfirewall.gif)

Так как решения брандмауэра отличаются от среды к среде, в руководстве, предоставляемом в этом разделе, описывается трафик, необходимый для настройки среды App-V с подключением к Интернету в сети периметра. Эта информация также включает рекомендуемые внутренние сетевые серверы.

Поместите следующие серверы в сеть периметра:

-   Сервер управления App-V

-   IIS-сервер для публикации и потоковой передачи

**Примечание.**  
Лучше всего разместить сервер management Server и IIS на отдельных компьютерах.

 

Поместите следующие серверы во внутреннюю сеть:

-   Сервер контента

-   Хранилище данных (SQL Server)

-   Контроллер домена Active Directory

## <a name="traffic-requirements"></a>Требования к трафику


В следующих таблицах перечисляются требования к трафику для связи из Интернета и сети периметра и из сети периметра во внутреннюю сеть.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Требования к трафику из Интернета в сеть периметра</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>RTSPS (публикация пакетов обновления и потоковой передачи)</p></td>
<td align="left"><p>TCP 322 по умолчанию; это может быть изменено в сервере управления App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>HTTPS (публикация ICO и OSD-файлов и пакетов потоковой передачи)</p></td>
<td align="left"><p>TCP 443 по умолчанию; это может быть изменено в конфигурации IIS.</p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Требования к трафику от сети периметра до внутренней сети</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>SQL Server</p></td>
<td align="left"><p>TCP 1433 по умолчанию, но может быть настроен в SQL Server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>SMB/CIFS</p></td>
<td align="left"><p>Если каталог контента расположен удаленно от сервера управления (s) или IIS-сервера (рекомендуется).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Kerberos</p></td>
<td align="left"><p>TCP и UDP 88</p></td>
</tr>
<tr class="even">
<td align="left"><p>LDAP</p></td>
<td align="left"><p>TCP и UDP 389</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DNS</p></td>
<td align="left"><p>Для разрешения имен внутренних ресурсов (можно устранить с помощью файла хоста на сетевых серверах периметра)</p></td>
</tr>
</tbody>
</table>

 

 

 





