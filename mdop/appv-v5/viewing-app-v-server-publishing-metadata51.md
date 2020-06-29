---
title: Просмотр метаданных публикации сервера App-V
description: Просмотр метаданных публикации сервера App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813232"
---
# Просмотр метаданных публикации сервера App-V


Используйте эту процедуру для просмотра метаданных публикации, которые помогут вам устранить проблемы, связанные с публикацией. Для использования этой процедуры необходимо использовать сервер управления App-V.

В этой статье содержатся указанные ниже сведения.

-   [Требования к приложению App-V 5,1 для просмотра метаданных публикации](#bkmk-51-reqs-pub-meta)

-   [Синтаксис, используемый для просмотра метаданных публикации](#bkmk-syntax-view-pub-meta)

-   [Значения запроса для операционной системы и версии клиента](#bkmk-values-query-pub-meta)

-   [Определение метаданных публикации](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a>Требования к приложению App-V 5,1 для просмотра метаданных публикации


В приложении App-V 5,1 необходимо указать следующие значения в адресе при запросе метаданных на сервере публикации App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Значение</th>
<th align="left">Дополнительные сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Если вы пропускаете <strong> </strong> параметр ClientVersion из запроса, метаданные не включают возможности, которые были новыми в App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>ClientOS</strong></p></td>
<td align="left"><p>Это значение нужно указывать только в том случае, если в качестве последовательности пакетов выбраны определенные клиентские операционные системы. Если вы выбрали вариант по умолчанию (все операционные системы), не указывайте это значение в запросе.</p>
<p>Если вы пропускаете <strong> </strong> параметр ClientOS из запроса, только пакеты, упорядоченные для поддержки любой операционной системы, отображаются в метаданных.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>Синтаксис запроса для просмотра метаданных публикации


В таблице ниже приведены примеры синтаксиса и запроса.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия App-V</th>
<th align="left">Синтаксис запроса</th>
<th align="left">Описание параметров</th>
<th align="left">Пример.</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 с пакетом обновления 3 (SP3) и App-V 5,1</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;PubServer&gt;</p></td>
<td align="left"><p>Имя сервера публикаций App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Порт публикации #&gt;</p></td>
<td align="left"><p>Порт для сервера публикаций App-V, определенного при настройке сервера публикаций.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClientVersion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>Версия клиента App-V. Ниже приведена таблица с правильным значением, которое необходимо использовать.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ClientOS = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>Операционная система компьютера, на котором запущен клиент App-V. Ниже приведена таблица с правильным значением, которое необходимо использовать.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>Чтобы получить имя сервера публикаций и номер порта (http:// &lt; PubServer &gt; : &lt; Publish Port # &gt; ) из клиента App-V, просмотрите конфигурацию URL-адреса <strong> </strong> командлета PowerShell Get-AppvPublishingServer.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>В примере:</p>
<ul>
<li><p>Служба публикации размещается на сервере Windows Server 2012 R2 под названием "pubsvr01".</p></li>
<li><p>Клиент Windows — это Windows 8,1 с 64-разр.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 – App-V 5,0 SP2</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>Примечание.</strong><br/><p><strong>ClientVersion </strong> и <strong> ClientOS </strong> поддерживаются только в app-v 5,0 SP3 и App-v 5,1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Ознакомьтесь со сведениями о приложении App-V 5,0 SP3 и App-V 5,1.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>В примере сервер Windows Server 2012 R2 с именем "pubsvr01" содержит службы управления и публикации.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>Значения запроса для операционной системы и версии клиента


В запросе метаданных публикации введите значения строки, соответствующие клиентской операционной системе и версии, которые вы используете.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Архитектура</th>
<th align="left">Строковое значение операционной строки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10;</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsClient_10.0_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10;</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsClient_10.0_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 R2</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsClient_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsClient_6.1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>WindowsServer_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>32-разрядная</p></td>
<td align="left"><p>WindowsServer_6.1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>Определение метаданных публикации


Если пакеты публикуются на компьютере, на котором запущен клиент App-V, на этот компьютер посылаются метаданные, указывающие, какие пакеты и группы подключений публикуются. Клиент App-V делает два отдельных запроса для следующих данных:

-   Пакеты и группы соединений, которые являются уполномоченными для клиентского компьютера.

-   Пакеты и группы соединений, которые являются уполномоченными для текущего пользователя.

Сервер публикации обменивается данными с сервером управления, чтобы определить, какие пакеты и группы подключений доступны для инициатора запроса. Сервер публикаций необходимо зарегистрировать на сервере управления, чтобы создать метаданные.

Вы можете просматривать метаданные для каждого запроса в веб-браузере с помощью запроса, который находится в контексте определенного пользователя или компьютера.






## Статьи по теме


[Технический справочник для App-V 5.1](technical-reference-for-app-v-51.md)









