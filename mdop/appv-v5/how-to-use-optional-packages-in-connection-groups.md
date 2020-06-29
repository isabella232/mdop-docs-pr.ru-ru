---
title: Использование дополнительных пакетов в группах соединений
description: Использование дополнительных пакетов в группах соединений
author: dansimp
ms.assetid: 4d08a81b-55e5-471a-91dc-9a684fb3c9a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 64a2c0758294bfa617d3d85f888cfce3a2c0d21e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813632"
---
# Использование дополнительных пакетов в группах соединений


Начиная с Microsoft Application Virtualization (App-V) 5,0 с пакетом обновления 3 (SP3), вы можете добавить дополнительные пакеты в группы соединений для упрощения управления группами подключений. В приведенной ниже таблице кратко описаны задачи, которые можно выполнить с помощью дополнительных пакетов, и приведены ссылки на инструкции для каждой задачи.

**Примечание** 
 **Необязательные пакеты поддерживаются только в App-V 5,0 SP3.**

 

Прежде чем использовать дополнительные пакеты, ознакомьтесь [с требованиями для использования необязательных пакетов в группах соединений](#bkmk-reqs-using-cg).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ссылка на инструкции</th>
<th align="left">Задача</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">Использование одной группы подключения с необязательными пакетами для нескольких пользователей, у которых есть разные пакеты.</a></p></td>
<td align="left"><p>Используйте одну группу подключения, чтобы сделать различные группы приложений и подключаемых модулей доступными для разных конечных пользователей.</p>
<p>Например, вы хотите распространить Microsoft Office для всех конечных пользователей, но распространите различные подключаемые модули для разных подмножества пользователей.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">Отменить публикацию или удалить дополнительный пакет или отменить публикацию дополнительного пакета, а затем повторно опубликовать его позже без изменения группы подключения</a></p></td>
<td align="left"><p>Отменить публикацию, удалить или повторно опубликовать необязательный пакет, не отключая, удаляя, изменяя, добавляйте и заново включайте группу соединения в клиенте App-V.</p>
<p>Кроме того, вы можете отменить публикацию дополнительного пакета и повторно опубликовать его позже, не отключая и не перепубликуя группу подключения.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>Использование одной группы подключения с необязательными пакетами для нескольких пользователей с разными пакетами.


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Описание задачи</th>
<th align="left">Выполнение задачи</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>С помощью App-V 5,0 SP3</strong></p>
<p>Вы можете добавлять в группы соединений дополнительные пакеты, что позволяет использовать различные сочетания приложений и подключаемые модули для разных конечных пользователей.</p>
<p><strong>Пример </strong> : вы хотите распространить приложение Microsoft Office для конечных пользователей, но включите определенный плагин для всего набора пользователей.</p>
<p>Для этого создайте группу подключений, которая включает пакет с Office, и другой пакет с подключаемыми модулями Office, а затем сделайте пакет подключаемым модулем необязательным.</p>
<p>Конечные пользователи, у которых нет прав на доступ к пакету для подключения к плагину, по-прежнему смогут запускать Office.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Действия</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер App-V Server — консоль управления</p></td>
<td align="left"><ol>
<li><p>На консоли управления выберите пакеты, <strong> </strong> чтобы открыть страницу пакеты.</p></li>
<li><p>Выберите <strong> группы подключений </strong> , чтобы отобразить библиотеку групп подключения.</p></li>
<li><p>Выберите нужную группу подключений в библиотеке групп соединений.</p></li>
<li><p>Нажмите кнопку <strong> изменить </strong> в области подключенные пакеты.</p></li>
<li><p><strong> </strong> Рядом с названием пакета выберите пункт необязательный.</p></li>
<li><p>Установите <strong> флажок Добавить пакет для доступа к группе </strong> . Этот обязательный этап добавляет в группу подключения данные, которые вы настроили ранее, когда вы назначили пакеты группам Active Directory.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Сервер App-V-командлетов PowerShell</p></td>
<td align="left"><p>Используйте следующий командлет и укажите <strong> параметр-Optional </strong> :</p>
<p><strong>Add-AppvServerConnectionGroupPackage</strong></p>
<p><strong>Максимальное</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>Пример.</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Клиент App-V на отдельном компьютере</p></td>
<td align="left"><ol>
<li><p>Создайте XML-документ группы подключения и задайте <strong> </strong> для атрибута "тег пакета <strong> </strong> <strong> " параметр "истина".</strong></p></li>
<li><p>Чтобы добавить и включить группу подключения, используйте следующие командлеты:</p>
<ul>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>Пример XML-документа группы подключения с дополнительными пакетами:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>В версиях, предшествующих App-V 5,0 с пакетом обновления 3 (SP3)</strong></p></td>
<td align="left"><p>Чтобы сделать определенные пользователи доступными для конкретных пользователей, вам пришлось создать большое количество групп соединений.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>Отменить публикацию или удалить дополнительный пакет или отменить публикацию дополнительного пакета, а затем повторно опубликовать его позже без изменения группы подключения


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Описание задачи</th>
<th align="left">Выполнение задачи</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>С помощью App-V 5,0 SP3</strong></p>
<p>Вы можете отменить публикацию, удалить или повторно опубликовать необязательный пакет, который находится в группе подключения, не отключая и не перезапуская группу соединения в клиенте App-V.</p>
<p>Кроме того, вы можете отменить публикацию дополнительного пакета и повторно опубликовать его позже, не отключая и не перепубликуя группу подключения.</p>
<p><strong>Пример </strong> : Если вы публикуете дополнительный пакет, содержащий надстройку Microsoft Office, и хотите удалить его, вы можете отменить публикацию пакета, не отключая группу подключения.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Метод</th>
<th align="left">Действия</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Сервер App-V Server — консоль управления</p></td>
<td align="left"><ul>
<li><p>Чтобы отменить публикацию пакета: на консоли управления выберите пункт выбрать <strong> </strong> страницу пакетов, щелкните правой кнопкой мыши пакет, который нужно отменить, и выберите команду <strong> отменить публикацию </strong> .</p></li>
<li><p>Чтобы удалить дополнительный пакет из группы подключения, <strong> </strong> выберите пакет, который вы хотите удалить, и щелкните стрелку вправо, чтобы удалить пакет из области групп подключений в нижней части экрана.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Клиент App-V на отдельном компьютере</p></td>
<td align="left"><p>Используйте следующие существующие командлеты:</p>
<ul>
<li><p>Отмена публикации — AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
</ul>
<p>Дополнительные сведения <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> можно найти в разделе Управление пакетами приложений App-V 5,0, запущенными на отдельном компьютере с помощью PowerShell </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>В версиях, предшествующих App-V 5,0 с пакетом обновления 3 (SP3)</strong></p></td>
<td align="left"><p>Вам пришлось:</p>
<ol>
<li><p>Удалите группу подключений с каждого клиентского компьютера App-V, на котором он был включен.</p></li>
<li><p>Отмена публикации пакета.</p></li>
<li><p>Удалите пакет из определения группы подключения.</p></li>
<li><p>Повторно опубликуйте группу подключения.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>Требования для использования необязательных пакетов в группах соединений


Прежде чем использовать дополнительные пакеты в группах соединений, ознакомьтесь с приведенными ниже требованиями.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Требование</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Группы соединения должны содержать по крайней мере один необязательный пакет.</p></td>
<td align="left"><ul>
<li><p>Убедитесь, что вы удовлетворены этим требованием, так как сервер App-V и командлет PowerShell не проверяют выполнение требования.</p></li>
<li><p>Если вы случайно создали группу подключений, которая не содержит по крайней мере один необязательный пакет, и пользователь попытается открыть упакованное приложение в этой группе, произойдет сбой группы подключения.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>Опубликованные пользователем группы подключения могут содержать пакеты, опубликованные глобально или для пользователей.</p></li>
<li><p>Глобальные опубликованные группы подключения должны содержать только глобально опубликованные пакеты.</p></li>
</ul></td>
<td align="left"><p>Глобальные опубликованные группы подключения должны содержать пакеты, которые публикуются глобально, чтобы обеспечить доступность пакетов при запуске виртуальной среды группы подключения.</p>
<p>При попытке добавления или включения глобальных опубликованных групп подключений, содержащих опубликованные пользователем пакеты, произойдет сбой группы подключения.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Перед публикацией группы подключения, содержащей эти пакеты, необходимо опубликовать все необязательные пакеты.</p></td>
<td align="left"><p>Виртуальная среда группы соединения не может быть запущена, если не указаны необязательные пакеты.</p>
<p>Клиент App-V не может добавить или включить группу соединения, если не были опубликованы какие-либо необязательные пакеты.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Прежде чем отменять публикацию глобально опубликованного пакета, убедитесь в том, что для групп подключения, которые имеют право для всех пользователей на этом компьютере, больше не требуется пакет.</p></td>
<td align="left"><p>Система не проверяет, является ли пакет частью группы подключения другого пользователя. После отмены публикации глобального пакета он будет недоступен каждому пользователю компьютера, поэтому убедитесь, что группы подключений пользователей больше не содержат пакет, или сделайте пакет необязательным.</p></td>
</tr>
</tbody>
</table>

 






## Статьи по теме


[Управление связывающими группами](managing-connection-groups.md)

 

 





