---
title: О файле связывающей группы
description: О файле связывающей группы
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814928"
---
# О файле связывающей группы


**В этой статье:**

-   [Назначение и расположение файла в группе подключения](#bkmk-cg-purpose-loc)

-   [Структура XML-файла группы подключения](#bkmk-define-cg-5-0sp3)

-   [Настройка приоритета пакетов в группе подключения](#bkmk-config-pkg-priority-incg)

-   [Поддерживаемые конфигурации подключений виртуальных приложений](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>Назначение и расположение файла в группе подключения


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Назначение группы соединения</p></td>
<td align="left"><p>Группа подключений — это функция App-V, позволяющая группировать пакеты вместе, чтобы создать виртуальную среду, в которой приложения в этих пакетах могут взаимодействовать друг с другом.</p>
<p>Пример: вы хотите использовать подключаемые модули в Microsoft Office. Вы можете создать пакет, содержащий подключаемые модули, и создать другой пакет, содержащий Office, а затем добавить оба пакета в группу подключения, чтобы позволить Office использовать эти подключаемые модули.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Как работает файл группы подключения</p></td>
<td align="left"><p>При применении файла группы подключения App-V 5,1 пакеты, перечисленные в файле, будут объединяться во время выполнения в одну виртуальную среду. С помощью файла Microsoft Application Virtualization (App-V) 5,1 в группе Подключение можно настроить существующие группы соединения App-V 5,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Пример пути к файлу</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>Структура XML-файла группы подключения


**Содержание раздела**

-   [Параметры, определяющие группу соединения](#bkmk-params-define-cg)

-   [Параметры, определяющие пакеты в группе "соединение"](#bkmk-params-define-pkgs-incg)

-   [Пример XML-файла группы подключения для App-V](#bkmk-50sp3-exp-cg-xml)

-   [Приложение App-V 5,0 с помощью App-V 5,0 SP2 пример XML-файла группы подключения](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>Параметры, определяющие группу соединения

В приведенной ниже таблице описаны параметры XML-файла, в котором определена сама группа подключения, а не пакеты.

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
<td align="left"><p>Имя схемы</p></td>
<td align="left"><p>Имя схемы.</p>
<p><strong>Применимо, начиная с версии App-V 5,0 SP3 </strong> : Если вы хотите использовать новые функции "дополнительные пакеты" и "использовать любую версию", описанные в этой таблице, необходимо указать в XML-файле следующую схему:</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>Уникальный идентификатор GUID для этой группы подключения. Состояние группы подключения сопоставлено с этим идентификатором. Указывайте этот идентификатор только при создании группы подключения.</p>
<p>Вы можете создать новый идентификатор GUID, введя: <strong>[Guid]::NewGuid()</strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Идентификатор GUID версии для этой версии группы подключения.</p>
<p>При обновлении группы подключения (например, при добавлении или обновлении нового пакета) необходимо обновить GUID версии, чтобы он отражал новую версию.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>Отображаемое имя группы подключения.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Priority</p></td>
<td align="left"><p>Необязательное поле приоритета для группы подключения.</p>
<p><strong>0 </strong> - указывает высший приоритет.</p>
<p>Если требуется задать приоритет, но он не настроен, произойдет сбой пакета, так как не будет определена нужная группа подключения.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>Параметры, определяющие пакеты в группе "соединение"

В &lt; разделе Packages &gt; XML-файла группы подключения вы перечислите пакеты участников в группе подключение, указав уникальный идентификатор пакета и идентификатор версии каждого пакета, как описано в приведенной ниже таблице. Первый пакет в списке имеет наивысший приоритет.

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
<td align="left"><p>PackageId</p></td>
<td align="left"><p>Уникальный идентификатор GUID для этого пакета. Этот идентификатор GUID не меняется, когда публикуются более новые версии пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Уникальный идентификатор GUID для версии пакета.</p>
<p><strong>Применимо начиная с App-V 5,0 SP3 </strong> : Если вы задаете <strong> "*" </strong> для версии пакета, динамически вставляется идентификатор GUID последней доступной версии пакета.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Функция "переключатель"</p></td>
<td align="left"><p><strong>Применимо в App-V 5,0 SP3 </strong> : параметр, который позволяет сделать пакет необязательным в группе подключения. Допустимые значения:</p>
<ul>
<li><p><strong>"истина" </strong> — пакет является необязательным в группе "соединение"</p></li>
<li><p><strong>"ложь" </strong> — в группе "соединение" требуется пакет</p></li>
</ul>
<p>Узнайте <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> , как использовать дополнительные пакеты в группах соединений </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>Пример XML-файла группы подключения для App-V

Ниже приведен пример XML-файла группы подключения, в котором показаны примеры полей в предыдущих таблицах, а также выделены элементы, которые были введены в приложении App-V 5,0 с пакетом обновления 3 (SP3).

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>Приложение App-V 5,0 с помощью App-V 5,0 SP2 пример XML-файла группы подключения

Следующий пример XML-файла группы подключения применим к приложению App-V 5,0 с помощью App-v 5,0 SP2. В нем показаны примеры полей в предыдущей таблице, но исключены описанные выше изменения для App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>Настройка приоритета пакетов в группе подключения


Приоритет пакета настраивается с помощью порядка списка пакетов. Первый пакет в документе имеет наивысший приоритет. Последующие пакеты в списке имеют убывающий приоритет.

Приоритет пакета — это разрешение, которое может быть ненеизбежным конфликтом ресурсов при инициализации виртуальной среды. Например, если два пакета, открываемые в одной виртуальной среде, имеют одинаковый параметр Registry, то пакет с наивысшим приоритетом определяет значение, которое задается.

С помощью файла группы подключения можно настроить каждую группу подключений, выполнив указанные ниже действия.

-   Укажите приоритеты выполнения для групп подключения. Чтобы изменить приоритет с помощью консоли управления App-V, щелкните группу соединения и нажмите кнопку **изменить**.

    **Примечание**  Priority требуется только в том случае, если пакет связан с несколькими группами соединений.

     

-   Укажите приоритет пакета в группе подключение.

Поле «приоритет» является обязательным, если запущенное виртуальное приложение запускается из запроса собственного приложения, например проводник Microsoft Windows. Клиент App-V использует приоритет, чтобы определить, в какой группе подключения должна выполняться приложение. Такая ситуация возникает, если виртуальное приложение входит в состав нескольких групп подключения.

Если виртуальное приложение открыто с помощью другого виртуального приложения, будет использоваться виртуальная среда исходного виртуального приложения. В этом случае поле «приоритет» не используется.

**Пример.**

Виртуальное приложение Microsoft Outlook работает в виртуальной среде **XYZ**. Когда вы открываете прикрепленный документ Microsoft Word, в виртуальной среде **XYZ**открывается виртуализированная версия Microsoft Word, независимо от того, какие из виртуализированных групп подключений и приоритетов среды выполнения соответствует Microsoft Word.

## <a href="" id="bkmk-va-conn-configs"></a>Поддерживаемые конфигурации подключений виртуальных приложений


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Конфигурация</th>
<th align="left">Пример сценария</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Массив. EXE-файл и надстройка (DLL)</p></td>
<td align="left"><ul>
<li><p>Вы хотите распространить Microsoft Office для всех пользователей, но распространите плагин Microsoft Excel только на подмножество пользователей.</p></li>
<li><p>Включите группу подключения для соответствующих пользователей.</p></li>
<li><p>Обновляйте каждый пакет по отдельности по мере необходимости.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Массив. EXE-файл и приложение по промежуточного слоя</p></td>
<td align="left"><ul>
<li><p>Для работы приложения требуется приложение по промежуточного слоя или несколько приложений, которые зависят от одной и той же версии среды выполнения промежуточного слоя.</p></li>
<li><p>Все компьютеры, на которых требуется одно или несколько приложений, получают группы подключений с приложением и средой выполнения приложения по промежуточного слоя.</p></li>
<li><p>При необходимости вы можете объединить несколько приложений по промежуточного слоя в одну группу подключения.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Пример.</th>
<th align="left">Пример описания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Группа виртуальных подключений приложений для финансового подразделения</p></td>
<td align="left"><ul>
<li><p>Приложение по промежуточного слоя 1</p></li>
<li><p>Приложение по промежуточного слоя 2</p></li>
<li><p>Приложение по промежуточного слоя 3</p></li>
<li><p>Среда выполнения приложения по промежуточного слоя</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Группа подключений виртуальных приложений для отдела кадров</p></td>
<td align="left"><ul>
<li><p>Приложение по промежуточного слоя 5</p></li>
<li><p>Приложение по слоям 6</p></li>
<li><p>Среда выполнения приложения по промежуточного слоя</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Массив. EXE файл и exe</p></td>
<td align="left"><p>У вас есть приложение, которое использует другое приложение и хотите, чтобы пакеты были разделены для эффективности работы, ограничения лицензирования или развертывания временной шкалы.</p>
<p><strong>Пример.</strong></p>
<p>Если вы развертываете Microsoft Lync 2010, вы можете использовать три пакета:</p>
<ul>
<li><p>Microsoft Office2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>Вы можете управлять развертыванием с помощью следующих групп соединений:</p>
<ul>
<li><p>Microsoft Office2010 и Microsoft Communicator2007</p></li>
<li><p>Microsoft Office2010 и Microsoft Lync2010</p></li>
</ul>
<p>После завершения развертывания вы можете либо создать один новый пакет Microsoft Office2010 + Microsoft Lync2010, либо сохранить и сохранить его в виде отдельных пакетов и развернуть с помощью группы подключения.</p></td>
</tr>
</tbody>
</table>

 






## Статьи по теме


[Управление связывающими группами](managing-connection-groups51.md)

 

 





