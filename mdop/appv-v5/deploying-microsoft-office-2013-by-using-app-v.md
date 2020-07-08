---
title: Развертывание Microsoft Office 2013 с помощью App-V
description: Развертывание Microsoft Office 2013 с помощью App-V
author: dansimp
ms.assetid: 02df5dc8-79e2-4c5c-8398-dbfb23344ab3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: c57227d531c61949f9160c27fc249db72dbc6523
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814632"
---
# Развертывание Microsoft Office 2013 с помощью App-V


В этой статье описано, как использовать Microsoft Application Virtualization 5,0 или более поздних версий для поставки Microsoft Office 2013 как виртуализованных приложений на компьютерах вашей организации. Сведения о том, как использовать App-V для отправки Office 2010, можно найти в разделе [развертывание Microsoft office 2010 с помощью App-V](deploying-microsoft-office-2010-by-using-app-v.md). Чтобы успешно развернуть Office 2013 с помощью App-V, вам необходимо ознакомиться с Office 2013 и PP-V.

Этот раздел включает в себя следующие разделы:

-   [Что нужно знать перед началом работы](#bkmk-before-you-start)

-   [Создание пакета Office 2013 для App-V с помощью средства развертывания Office](#bkmk-create-office-pkg)

-   [Публикация пакета Office для App-V 5,0](#bkmk-pub-pkg-office)

-   [Настройка пакетов приложений Office App-V и управление ими](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a>Что нужно знать перед началом работы


Перед развертыванием Office 2013 с помощью App-V ознакомьтесь со следующими сведениями о планировании.

### <a href="" id="bkmk-supp-vers-coexist"></a>Поддерживаемые версии Office и сосуществование Office

В следующей таблице приведены сведения о поддерживаемых версиях Office и о том, как работать с имеющимися версиями Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Сведения для проверки</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)">Планирование использования App-V с Office</a></p></td>
<td align="left"><ul>
<li><p>Поддерживаемые версии Office</p></li>
<li><p>Поддерживаемые типы развертывания (например, классическое приложение, инфраструктура личных виртуальных рабочих столов (VDI), в составе пула VDI)</p></li>
<li><p>Варианты лицензирования Office</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)">Планирование использования App-V с Office</a></p></td>
<td align="left"><p>Рекомендации по установке разных версий Office на одном компьютере</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a>Требования к пакетированию, публикации и развертыванию

Перед развертыванием Office с помощью App-V ознакомьтесь с приведенными ниже требованиями.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Требование</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Создание пакетов</p></td>
<td align="left"><ul>
<li><p>Все приложения Office, которые вы хотите развернуть для пользователей, должны находиться в одном пакете.</p></li>
<li><p>В App-V 5,0 и более поздних версиях для создания пакетов необходимо использовать средство развертывания Office. Нельзя использовать секвенсор.</p></li>
<li><p>Если вы развертываете Microsoft Visio 2013 и Microsoft Project 2013 вместе с Office, необходимо включить их в один пакет с Office. Дополнительные сведения можно найти в разделе <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> развертывание Visio 2013 и Project 2013 с Office </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Публикация</p></td>
<td align="left"><ul>
<li><p>Вы можете опубликовать только один пакет Office на каждом клиентском компьютере.</p></li>
<li><p>Необходимо опубликовать пакет Office глобально. Вы не можете опубликовать пользователя.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Развертывание любого из перечисленных ниже продуктов на общем компьютере, например с помощью служб удаленных рабочих столов:</p>
<ul>
<li><p>Приложения Microsoft 365 для предприятий</p></li>
<li><p>Visio Pro для Office 365</p></li>
<li><p>Project Pro для Office 365</p></li>
</ul></td>
<td align="left"><p>Необходимо включить <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> активацию на общем компьютере </a> .</p>
<p>Активация на общем компьютере не используется, если вы разрабатываете продукт корпоративного лицензирования, например:</p>
<ul>
<li><p>Office профессиональный плюс 2013</p></li>
<li><p>Visio профессиональный 2013</p></li>
<li><p>Project профессиональный 2013</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Исключение приложений Office из пакета

В приведенной ниже таблице описаны рекомендуемые методы для исключения конкретных приложений Office из пакета.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Используйте <strong> параметр ExcludeApp </strong> при создании пакета с помощью средства развертывания Office.</p></td>
<td align="left"><ul>
<li><p>Позволяет исключить из пакета определенные приложения Office, когда средство развертывания Office создаст пакет. Например, вы можете использовать этот параметр, чтобы создать пакет, содержащий только Microsoft Word.</p></li>
<li><p>Дополнительные сведения можно найти в разделе <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp element </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Изменение файла DeploymentConfig.xml</p></td>
<td align="left"><ul>
<li><p>Измените файл DeploymentConfig.xml после создания пакета. Этот файл содержит параметры пакета по умолчанию для всех пользователей на компьютере, на котором запущен клиент App-V.</p></li>
<li><p>Дополнительные сведения можно найти в разделе <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> Отключение приложений Office 2013 </a> .</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a>Создание пакета Office 2013 для App-V с помощью средства развертывания Office


Выполните описанные ниже действия, чтобы создать пакет Office 2013 для App-V 5,0 или более поздней версии.

**Важно.**  
В App-V 5,0 и более поздних версиях необходимо создать пакет с помощью средства развертывания Office. Нельзя использовать секвенсор для создания пакетов.


### Проверка готовности к использованию средства развертывания Office

На компьютере, на котором устанавливается средство развертывания Office, должны быть:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Предварительные</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Необходимое программное обеспечение</p></td>
<td align="left"><p>.NET Framework 4</p></td>
</tr>
<tr class="even">
<td align="left"><p>Поддерживаемые операционные системы</p></td>
<td align="left"><ul>
<li><p>64-разрядная версия Windows 8</p></li>
<li><p>64-разрядная версия Windows 7</p></li>
</ul></td>
</tr>
</tbody>
</table>


**Примечание.**  
В этой статье термин "пакет приложения Office 2013 App-V" относится к лицензированию подписок и корпоративному лицензированию.


### Создание пакетов Office 2013 App-V с помощью средства развертывания Office

Пакеты App-V для Office 2013 создаются с помощью средства развертывания Office. Ниже описано, как создать пакет Office 2013 App-V с корпоративным лицензированием или лицензией на подписку.

Создавайте пакеты App-V для Office 2013 на компьютерах с 64-разрядной версией Windows. После создания пакет App-V для Office 2013 будет работать на компьютерах с Windows 7 и Windows 8, поддерживающих версию 32 и 64.

### Скачать средство развертывания Office

Пакеты App-V для Office 2013 создаются с помощью средства развертывания Office, которое создает пакет App-V для Office 2013. Пакет нельзя создать или изменить с помощью секвенсора App-V. Чтобы начать создание пакета, выполните указанные ниже действия.

1.  Скачайте [средство развертывания Office для приложения "нажми и работай](https://www.microsoft.com/download/details.aspx?id=36778)".

2.  Запустите exe исполняемый файл и извлеките его компоненты в нужное место. Чтобы упростить этот процесс, вы можете создать общую сетевую папку, в которой будут сохраняться функции.

    Пример: \\\\Server\\Office2013

3.  Убедитесь в том, что в указанном расположении есть setup.exe и configuration.xml файл.

### Загрузка приложений Office 2013

После того как вы загрузили средство развертывания Office, вы можете использовать его для получения последних приложений Office 2013. После того как вы получите приложения Office, вы создадите пакет Office 2013 App-V.

XML-файл, который входит в состав средства развертывания Office, определяет сведения о продукте, например языки и приложения Office.

1. **Настройте образец XML-файла конфигурации.** Чтобы настроить приложения Office, используйте образец XML-файла конфигурации, который вы загрузили с помощью средства развертывания Office.

   1. Откройте образец XML-файла в блокноте или в любом любимом текстовом редакторе.

   2. После открытия файла примера configuration.xml и его подготовки к редактированию вы можете указать продукты, языки и путь, по которому нужно сохранить приложения Office 2013. Ниже приведен простой пример файла configuration.xml.

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      **Примечание.**  
      XML-файл конфигурации — это пример XML-файла. Файл содержит строки, которые снабжены комментариями. Вы можете "снять комментарий", чтобы настроить дополнительные параметры файла.

      Вышеприведенный XML-файл конфигурации указывает на то, что версия Office 2013 ProPlus 32-bit Edition, включая Visio профессиональный плюс, будет загружена на английском языке в \\\\server\\Office 2013 (это расположение, в которое будут сохранены приложения Office). Обратите внимание, что код продукта приложения не влияет на финальное лицензирование Office. Пакеты App-V для Office 2013 с различными лицензированиями можно создавать из одних и тех же приложений, выдавая лицензирование на более поздней стадии. В таблице ниже перечислены настраиваемые атрибуты и элементы XML-файла.

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left">Ввод</th>
      <th align="left">Описание</th>
      <th align="left">Пример.</th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p>Добавить элемент</p></td>
      <td align="left"><p>Указывает продукты и языки, которые нужно включить в пакет.</p></td>
      <td align="left"><p>Н/Д</p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>OfficeClientEdition (атрибут элемента Add)</p></td>
      <td align="left"><p>Указывает выпуск Office 2013, который будет использоваться: с 32 или 64-bit. Операция завершается сбоем, если <strong> </strong> для OfficeClientEdition не задано допустимое значение.</p></td>
      <td align="left"><p><strong>OfficeClientEdition </strong> = &quot; 32&quot;</p>
      <p><strong>OfficeClientEdition </strong> = &quot; 64&quot;</p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Элемент Product</p></td>
      <td align="left"><p>Указывает приложение. Проект 2013 и Visio 2013 должны быть указаны в качестве добавленного продукта для включения в приложения.</p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
      <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
      <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Элемент Language</p></td>
      <td align="left"><p>Указывает язык, поддерживаемый в приложениях.</p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Версия (атрибут элемента Add)</p></td>
      <td align="left"><p>Необязательно. Задает сборку, используемую для пакета.</p>
      <p>По умолчанию — это новейшая объявленная сборка (определенная в v32.CAB на источнике Office).</p></td>
      <td align="left"><p><code>15.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Источник (атрибут элемента Add)</p></td>
      <td align="left"><p>Указывает расположение, в которое будут сохраняться приложения.</p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2013”</code></p></td>
      </tr>
      </tbody>
      </table>

      После редактирования файла configuration.xml, чтобы указать необходимый продукт, язык и расположение, в котором будут сохраняться приложения Office 2013, вы можете сохранить файл конфигурации, например Customconfig.xml.

2. **Скачайте приложения в указанное расположение:** Используйте командную команду с повышенными привилегиями и 64-разрядную операционную систему, чтобы скачать приложения Office 2013, которые позже будут преобразованы в пакет App-V. Ниже приведен пример команды с описанием сведений.

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   В примере:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2013</strong></p></td>
   <td align="left"><p>— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>— Это средство развертывания Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/Download</strong></p></td>
   <td align="left"><p>загружает приложения Office 2013, указанные в customConfig.xml файле. Эти биты можно позже преобразовать в пакет App-V для Office 2013 с корпоративным лицензированием.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2013\Customconfig.xml</strong></p></td>
   <td align="left"><p>передает XML-файл конфигурации, необходимый для завершения процесса загрузки, в этом примере customconfig.xml. После использования команды скачать приложения Office нужно найти в расположении, указанном в XML-файле конфигурации, в этом примере \Server\Office2013.</p></td>
   </tr>
   </tbody>
   </table>



### Преобразование приложений Office в пакет App-V

После загрузки приложений Office 2013 с помощью средства развертывания Office с помощью средства развертывания Office можно преобразовать их в пакет приложения Office 2013. Выполните действия, соответствующие вашей модели лицензирования.

**Общие сведения о том, что вам нужно сделать:**

-   Создавайте пакеты App-V для Office 2013 на компьютерах с 64-разрядной версией Windows. Однако пакет будет работать на компьютерах с операционной системой Windows 7 и Windows 8 (32-64 разрядная версия).

-   Создайте пакет Office App-V для лицензирования подписки или корпоративного лицензирования с помощью средства развертывания Office, а затем измените файл конфигурации CustomConfig.xml.

    В следующей таблице приведены значения, которые необходимо ввести в файл CustomConfig.xml для модели лицензирования, которую вы используете. В разделах, которые следуют за таблицей, указаны точные записи, которые необходимо выполнить.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Код продукта</th>
<th align="left">Корпоративное лицензирование</th>
<th align="left">Лицензирование подписки</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Office 2013</strong></p></td>
<td align="left"><p>ProPlusVolume</p></td>
<td align="left"><p>O365ProPlusRetail</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Office 2013 с Visio 2013</strong></p></td>
<td align="left"><p>ProPlusVolume</p>
<p>VisioProVolume</p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Office 2013 с Visio 2013 и Project 2013</strong></p></td>
<td align="left"><p>ProPlusVolume</p>
<p>VisioProVolume</p>
<p>ProjectProVolume</p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p>
<p>ProjectProRetail</p></td>
</tr>
</tbody>
</table>



**Преобразование приложений Office в пакет App-V**

1. В блокноте снова откройте файл CustomConfig.xml и внесите в него указанные ниже изменения.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Параметр</th>
   <th align="left">Что нужно сделать, чтобы изменить значение на</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Источник</p></td>
   <td align="left"><p>Наведите указатель мыши на приложения Office, загруженные ранее.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ProductID</p></td>
   <td align="left"><p>Укажите тип лицензирования, как показано в следующих примерах:</p>
   <ul>
   <li><p>Лицензирование подписки</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p>В этом примере были сделаны следующие изменения для создания пакета с лицензией на подписку.</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Источник</strong></p></td>
   <td align="left"><p>— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Код продукта</strong></p></td>
   <td align="left"><p>для Office изменено на <code>O365ProPlusRetail</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Код продукта</strong></p></td>
   <td align="left"><p>для Visio изменено на <code>VisioProRetail</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p>Корпоративное лицензирование</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p>В этом примере были сделаны следующие изменения для создания пакета с помощью программы корпоративного лицензирования.</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Источник</strong></p></td>
   <td align="left"><p>— путь, который был изменен, чтобы указывал на приложения Office, загруженные ранее.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Код продукта</strong></p></td>
   <td align="left"><p>для Office изменено на <code>ProPlusVolume</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Код продукта</strong></p></td>
   <td align="left"><p>для Visio изменено на <code>VisioProVolume</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ExcludeApp (необязательно)</p></td>
   <td align="left"><p>Позволяет указать программы Office, которые не нужно включать в пакет App-V, создаваемый средством развертывания Office. Например, вы можете исключить Access и InfoPath.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>PACKAGEGUID (необязательно)</p></td>
   <td align="left"><p>По умолчанию все пакеты App-V, созданные с помощью средства развертывания Office, имеют один и тот же идентификатор пакета App-V. Вы можете использовать PACKAGEGUID, чтобы указать другой идентификатор пакета для каждого пакета, который позволяет публиковать несколько пакетов App-V, созданных средством развертывания Office, и управлять ими с помощью сервера App-V.</p>
   <p>Например, если вы хотите использовать этот параметр, если вы создаете разные пакеты для разных пользователей. Например, вы можете создать пакет с помощью Office 2013 для некоторых пользователей и создать еще один пакет с Office 2013 и Visio 2013 для другого набора пользователей.</p>
   <div class="alert">
   <strong>Примечание.</strong><br/><p>Даже если вы используете уникальные идентификаторы пакетов, вы по-прежнему можете развернуть только один пакет App-V на одном устройстве.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. С помощью команды/packager можно преобразовать приложения Office в пакет Office 2013 App-V.

   Пример

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   В примере:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2013</strong></p></td>
   <td align="left"><p>— Это расположение общей сетевой папки, содержащей средство развертывания Office и файл настраиваемого Configuration.xml, Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>— Это средство развертывания Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/packager</strong></p></td>
   <td align="left"><p>создает пакет App-V Office 2013 с корпоративным лицензированием, как указано в файле customConfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2013\Customconfig.xml</strong></p></td>
   <td align="left"><p>передает XML-файл конфигурации (в данном случае customConfig), подготовленный для этапа упаковки.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>\server\share\Office 2013AppV</strong></p></td>
   <td align="left"><p>Указывает расположение только что созданного пакета Office App-V.</p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. Убедитесь в том, что пакет App-V для Office 2013 правильно работает:

   1.  Опубликуйте пакет App-V Office 2013, созданный глобально, на тестовом компьютере, и убедитесь, что появились ярлыки Office 2013.

   2.  Запустите несколько приложений Office 2013, например Excel или Word, чтобы убедиться, что пакет работает должным образом.

## <a href="" id="bkmk-pub-pkg-office"></a>Публикация пакета Office для App-V 5,0


Используйте указанные ниже сведения, чтобы опубликовать пакет Office.

### Методы публикации пакетов приложения Office App-V

Развертывание пакета App-V для Office 2013 с помощью тех же способов, которые вы используете для любого другого пакета:

-   System Center Configuration Manager

-   Сервер App-V

-   Самостоятельная работа с помощью команд PowerShell

### Необходимые условия и требования к публикации

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Необходимые условия и требования</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Включение сценариев PowerShell для клиентов App-V</p></td>
<td align="left"><p>Чтобы опубликовать пакеты Office 2013, необходимо выполнить сценарий.</p>
<p>Сценарии пакетов по умолчанию отключены для клиентов App-V. Чтобы включить сценарии, выполните следующую команду PowerShell:</p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p>Публикация пакета Office 2013 в глобальном масштабе</p></td>
<td align="left"><p>Точки расширения в пакете Office App-V требуют установки на уровне компьютера.</p>
<p>При публикации на уровне компьютера не требуется выполнять необходимые действия или распространяемые компоненты, а пакет Office 2013 глобально позволяет приложениям работать как в исходном установленном Office, устраняя необходимость настраивать пакеты для администраторов.</p></td>
</tr>
</tbody>
</table>



### Публикация пакета Office

Выполните следующую команду, чтобы опубликовать пакет Office глобально.

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   С консоли управления Веба на сервере App-V можно добавлять разрешения для группы компьютеров, а не для группы пользователей, чтобы пакеты могли публиковаться на компьютерах в соответствующей группе.

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a>Настройка пакетов приложений Office App-V и управление ими


Для управления пакетами Office App-V используйте те же действия, что и для любого другого пакета, но есть несколько исключений, как описано в следующих разделах.

-   [Включение подключаемых модулей Office с помощью групп подключений](#bkmk-enable-office-plugins)

-   [Отключение приложений Office 2013](#bkmk-disable-office-apps)

-   [Отключение сочетаний клавиш в Office 2013](#bkmk-disable-shortcuts)

-   [Управление обновлениями пакетов Office 2013](#bkmk-manage-office-pkg-upgrd)

-   [Управление обновлениями лицензирования Office 2013](#bkmk-manage-office-lic-upgrd)

-   [Развертывание Visio 2013 и Project 2013 с Office](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a>Включение подключаемых модулей Office с помощью групп подключений

Выполните действия, описанные в этом разделе, чтобы включить подключаемые модули Office для пакета Office. Чтобы использовать подключаемые модули Office, необходимо использовать секвенсор App-V для создания отдельного пакета, содержащего только подключаемые модули. Вы не можете использовать средство развертывания Office для создания пакета подключаемых модулей. Затем создайте группу подключения, которая включает пакет Office и пакет подключаемых модулей, как описано ниже.

**Чтобы включить подключаемые модули для пакетов Office App-V**

1.  Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.

2.  Поочередные подключаемые модули с помощью секвенсора App-V 5,0. Убедитесь, что на компьютере, используемом для последовательного подключения к сети, установлен Office 2013. При последовательности подключаемых модулей Office 2013 рекомендуется использовать приложения Microsoft 365 для предприятий (невиртуальные) на компьютере с виртуализацией.

3.  Создайте пакет App-V 5,0, который содержит нужные подключаемые модули.

4.  Добавьте группу подключений с помощью сервера App-V, System Center Configuration Manager или командлета PowerShell.

5.  Добавьте пакет приложений Office 2013 App-V и подключаемый комплект, который вы последовательно расдобавили в группу подключений, которую вы создали.

    **Важно.**  
    Порядок пакетов в группе подключения определяет порядок, в котором будет объединено содержимое пакета. В файле-дескрипторе группы подключения сначала добавьте пакет Office 2013 App-V, а затем добавьте пакет App-V для плагина.



6.  Убедитесь, что оба пакета опубликованы на целевом компьютере, и что пакет Plug-in опубликован глобально, чтобы они соответствовали глобальным параметрам опубликованного пакета Office 2013 App-V.

7.  Убедитесь в том, что в файле конфигурации развертывания для пакета Plug-in установлены те же параметры, что и в пакете приложения Office 2013 App-V.

    Так как пакет Office 2013 App-V интегрируется с операционной системой, параметры комплекта для подключения должны совпадать. Вы можете выполнить поиск по файлу конфигурации развертывания в режиме COM и убедиться, что для пакета подключаемых модулей установлено значение "Интеграция", и что "InProcessEnabled" и "OutOfProcessEnabled" соответствуют параметрам пакета Office 2013 App-V, который вы опубликовали.

8.  Откройте файл конфигурации развертывания и задайте для параметра значения для **объектов** значение **false**.

9.  Если вы внесли изменения в файл конфигурации развертывания после выполнения последовательности, убедитесь в том, что пакет Plug-in опубликован с файлом.

10. Убедитесь, что созданная группа подключения включена на нужном компьютере. Если пакет Office 2013 App-V используется, если группа подключений включена, возможно, созданная группа подключения будет "отложить". В этом случае вам потребуется перезагрузить компьютер, чтобы успешно включить группу соединений.

11. После успешной публикации обоих пакетов и включения группы подключения запустите целевое приложение Office 2013 и убедитесь, что подключенный и добавленный в группу подключения внешний сервер работает должным образом.

### <a href="" id="bkmk-disable-office-apps"></a>Отключение приложений Office 2013

Вам может потребоваться отключить определенные приложения в пакете Office App-V. Например, вы можете отключить Access, но оставить все остальные доступные приложения Office в главном приложении. При отключении приложения конечный пользователь больше не увидит ярлык для этого приложения. Переупорядочение приложения не требуется. При изменении файла конфигурации развертывания после публикации пакета Office 2013 App-V необходимо сохранить изменения, добавить пакет приложения Office 2013 и затем повторно опубликовать его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2013 App-V.

**Примечание.**  
Чтобы исключить определенные приложения Office (например, Access и InfoPath) при создании пакета App-V с помощью средства развертывания Office, используйте параметр **ExcludeApp** . Дополнительные сведения можно найти в разделе [ссылки на файл "нажми и работай configuration.xml"](https://technet.microsoft.com/library/jj219426.aspx).



**Отключение приложения Office 2013**

1.  Откройте файл конфигурации развертывания в текстовом редакторе, например в **блокноте** , и выполните поиск по слову "приложения".

2.  Найдите приложение Office, которое вы хотите отключить, например Access 2013.

3.  Измените значение "включено" с "истина" на "ложь".

4.  Сохраните файл конфигурации развертывания.

5.  Добавьте пакет App-V Office 2013 с новым файлом конфигурации развертывания.

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  Повторно добавьте пакет Office 2013 App-V, а затем снова опубликуйте его с помощью нового файла конфигурации развертывания, чтобы применить новые параметры к пакетным приложениям Office 2013 App-V.

### <a href="" id="bkmk-disable-shortcuts"></a>Отключение сочетаний клавиш в Office 2013

Вместо отмены публикации или удаления пакета вы можете отключить сочетания клавиш для некоторых приложений Office. В следующем примере показано, как отключить сочетания клавиш для Microsoft Access.

**Отключение сочетаний клавиш для приложений Office 2013**

1.  Откройте файл конфигурации развертывания в блокноте и выполните поиск по запросу "ярлыки".

2.  Чтобы отключить определенные сочетания клавиш, удалите или закомментируйте конкретные сочетания клавиш, которые вам не нужны. Подсистема должна быть доступна и включена. Например, в приведенном ниже примере удалите сочетания клавиш Microsoft Access, сохранив при этом ярлыки/shortcut не &lt; &gt; &lt; &gt; смогут отключить ярлык Microsoft Access.

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  Сохраните файл конфигурации развертывания.

4.  Повторно опубликуйте пакет Office 2013 App-V с новым файлом конфигурации развертывания.

Многие дополнительные параметры можно изменить, изменив конфигурацию развертывания для пакетов App-V, например сопоставления типов файлов, виртуальной файловой системы и т. д. Дополнительные сведения об использовании файлов конфигурации развертывания для изменения параметров пакета App-V можно найти в разделе Дополнительные ресурсы в конце документа.

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a>Управление обновлениями пакетов Office 2013

Чтобы обновить пакет Office 2013, используйте средство развертывания Office. Чтобы обновить ранее развернутый пакет Office 2013, выполните указанные ниже действия.

**Как обновить ранее развернутый пакет Office 2013**

1.  Создайте новый пакет Office 2013 с помощью средства развертывания Office, которое использует самую последнюю версию приложения Office 2013. Последние биты Office 2013 всегда можно получить на этапе загрузки пакета App-V приложения Office 2013. Недавно созданный пакет Office 2013 содержит самые последние обновления и новый идентификатор версии. Все пакеты, созданные с помощью средства развертывания Office, имеют одинаковый журнал обращений.

    **Примечание.**  
    У пакетов Office App-V есть два идентификатора версии:

    -   Идентификатор версии пакета App-V для Office 2013, уникальный для всех пакетов, созданных с помощью средства развертывания Office.

    -   Второй идентификатор версии пакета App-V, x. x. x. x, например, в манифесте AppX, который будет изменен только в том случае, если у вас есть новая версия Office. Например, если выпущена новая версия Office 2013 с обновлениями, а пакет создан с помощью средства развертывания Office для включения этих обновлений, номер версии X. X. x. X изменится, чтобы показать, что сама версия Office изменилась. Сервер App-V использует номер версии X. X. X. X, чтобы отличать этот пакет и распознать, что он будет содержать новые обновления для ранее опубликованного пакета, и в результате его можно опубликовать как обновление для существующего пакета Office 2013.



2.  Глобально опубликуйте созданные пакеты Office 2013 App-V на компьютерах, на которых вы хотите применить новые обновления. Так как новый пакет имеет тот же журнал обращений к устаревшему пакету Office 2013 App-V, при публикации нового пакета с обновлениями будут применены только новые изменения старого пакета, поэтому они будут быстрее.

3.  Обновления будут применены таким же образом для глобальных опубликованных пакетов App-V. Так как приложения, скорее всего, будут использоваться, обновления могут быть отложены до тех пор, пока компьютер не будет перезагружен.

### <a href="" id="bkmk-manage-office-lic-upgrd"></a>Управление обновлениями лицензирования Office 2013

Если у нового пакета Office 2013 App-V есть лицензия, отличная от уже развернутого пакета App-V для Office 2013. Например, развернутый пакет Office 2013 является подпиской на основе подписки на Office 2013, а новый пакет Office 2013 — на основе корпоративного лицензирования, поэтому для обеспечения беспрепятственного лицензирования необходимо следовать приведенным ниже инструкциям.

**Как обновить лицензию на Office 2013**

1.  Отменить публикацию уже развернутого пакета приложения лицензированных подписок на Office 2013.

2.  Удалите неопубликованный пакет приложения для лицензирования подписки на Office 2013.

3.  Перезагрузите компьютер.

4.  Добавьте новый пакет корпоративного лицензирования Office 2013 App-V.

5.  Опубликуйте добавленный пакет App-V Office 2013 с помощью программы корпоративного лицензирования.

Пакет Office 2013 App-V с выбранным лицензированием будет успешно развернут.

### <a href="" id="bkmk-deploy-visio-project"></a>Развертывание Visio 2013 и Project 2013 с Office

В таблице ниже описаны требования и параметры для развертывания Visio 2013 и Project 2013 с Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Задача</th>
<th align="left">Сведения</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Как упаковать и опубликовать Visio 2013 и Project 2013 с Office?</p></td>
<td align="left"><p>Вы должны включить Visio 2013 и Project 2013 в один и тот же пакет для Office.</p>
<p>Если вы не развертываете Office, вы можете создать пакет, содержащий Visio и/или Project, при условии, что вы подпишитесь на <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> развертывание Microsoft Office 2010 с помощью App-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Как развернуть Visio 2013 и Project 2013 для определенных пользователей?</p></td>
<td align="left"><p>Воспользуйтесь одним из указанных ниже способов.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Если вы хотите...</th>
<th align="left">... затем используйте этот метод</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Создание двух разных пакетов и развертывание каждого из них в другой группе пользователей</p></td>
<td align="left"><p>Создание и развертывание следующих пакетов:</p>
<ul>
<li><p>Пакет, содержащий только Office — развертывание на компьютерах, пользователям которых требуется только Office.</p></li>
<li><p>Пакет, содержащий Office, Visio и Project-deploy, на компьютеры, для пользователей которых нужны все три приложения.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Если вам нужен только один пакет для всей организации или если у вас есть пользователи, которым предоставлен доступ к компьютерам:</p></td>
<td align="left"><p>Выполните указанные ниже действия.</p>
<ol>
<li><p>Создание пакета, содержащего Office, Visio и Project.</p></li>
<li><p>Развертывание пакета для всех пользователей.</p></li>
<li><p>Используйте <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> , чтобы запретить определенным пользователям использовать Visio и Project.</p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## Дополнительные ресурсы


**Пакеты Office 2013 App-V 5,0 5,0 дополнительные ресурсы**

[Средство развертывания Office для "нажми и работай"](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[Поддерживаемые сценарии для развертывания Microsoft Office в последовательном пакете App-V](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Пакеты Office 2010 App-V 5,0**

[Комплект виртуализации Microsoft Office 2010 для Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Известные проблемы, возникающие при создании или использовании пакета Office 2010 для App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Последовательность последовательностей Microsoft Office 2010 в Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Группы подключения**

[Развертывание групп подключений в Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Управление связывающими группами](managing-connection-groups.md)

**Динамическая настройка**

[Сведения о динамической конфигурации App-V 5.0](about-app-v-50-dynamic-configuration.md)














