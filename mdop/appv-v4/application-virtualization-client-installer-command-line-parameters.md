---
title: Параметры командной строки установщика клиента Application Virtualization
description: Параметры командной строки установщика клиента Application Virtualization
author: dansimp
ms.assetid: 508fa404-52a5-4919-8788-2a3dfb00639b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 911d333c80060c1881c96430c1d2d0516b6a4855
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819719"
---
# Параметры командной строки установщика клиента Application Virtualization


В следующей таблице перечислены все доступные параметры командной строки установщика клиента Microsoft Application Virtualization, их значения и краткое описание каждого параметра. Параметры чувствительны к регистру и должны вводиться как прописные буквы. Все значения параметров должны быть заключены в двойные кавычки.

**Примечание.**  
-   Для App-V версии 4,6 параметры командной строки нельзя использовать во время обновления клиента.

-   Параметры *SWICACHESIZE* и *MINFREESPACEMB* нельзя сочетать в командной строке. Если используются оба аргумента, параметр *SWICACHESIZE* будет игнорироваться.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Параметр</th>
<th align="left">Данные</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>ALLOWINDEPENDENTFILESTREAMING</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Указывает, будет ли включена потоковая передача из файла независимо от того, как был настроен клиент с <em> помощью </em> параметра APPLICATIONSOURCEROOT. Если задано значение FALSE, транспорт не включит потоковую передачу из файлов даже в том случае, если в качестве <em> параметра APPLICATIONSOURCEROOT в OSD </em> есть путь к файлу.</p>
<p>Возможные значения:</p>
<ul>
<li><p>TRUE — приложение, развернутое вручную, может быть загружено с диска.</p></li>
<li><p>FALSE — все приложения должны поступать из исходного потокового сервера.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>APPLICATIONSOURCEROOT</em></p></td>
<td align="left"><p><em>URL-адрес RTSP:// </em> (для доставки динамического пакета)</p>
<p><em>URL-адрес file:// </em> или <em> UNC </em> (для загрузки из файла с пакетом доставки)</p></td>
<td align="left"><p>Чтобы включить администратора или электронную систему распространения программного обеспечения, чтобы обеспечить выполнение загрузки приложения в соответствии с схемой управления топологией, можно переопределить базу кода OSD для элемента HREF приложения (исходное расположение). Если значение равно "", то есть значение по умолчанию, используются существующие параметры OSD файла.</p>
<p>URL-адрес состоит из нескольких частей.</p>
<p>&lt;протокол &gt; :// &lt; сервер &gt; : &lt; &gt; / &lt; путь к порту &gt; / &lt; ? &gt; &lt; #fragment запросов&gt;</p>
<p>Путь в формате UNC состоит из трех частей:</p>
<p>&amp;lt; имя_компьютера &gt; &amp; lt; общий доступ к папке &gt; &amp; lt; ресурс&gt;</p>
<p>Если <em> параметр APPLICATIONSOURCEROOT </em> указан на клиентском компьютере, клиент будет прерывать URL-адрес или путь UNC из файла OSD в составные части и заменять разделы OSD соответствующими <em> </em> разделами APPLICATIONSOURCEROOT.</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Убедитесь, что при использовании file://с путями в формате UNC используется правильный формат. Правильный формат: file:// &amp; lt; сервер &gt; &amp; lt; общий доступ &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>ICONSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> -адрес http:// </em> или <em> url-адрес https://</em></p></td>
<td align="left"><p>Позволяет администратору указать исходное расположение для получения значка для серийного пакета приложения во время публикации. Корни источника значков поддерживают пути в формате UNC и URL-адреса (HTTP или HTTPS). Если значение равно "", то есть значение по умолчанию, используются существующие параметры OSD файла.</p>
<p>URL-адрес состоит из нескольких частей.</p>
<p>&lt;протокол &gt; :// &lt; сервер &gt; : &lt; &gt; / &lt; путь к порту &gt; / &lt; ? &gt; &lt; #fragment запросов&gt;</p>
<p>Путь в формате UNC состоит из трех частей:</p>
<p>&amp;lt; имя_компьютера &gt; &amp; lt; общий доступ к папке &gt; &amp; lt; ресурс&gt;</p>
<div class="alert">
<strong>Важно.</strong><br/><p>При использовании UNC-пути следует использовать правильный формат. Допустимые форматы: &amp; lt; сервер &gt; &amp; lt; общий доступ &gt; или &lt; буква диска &gt; : &amp; lt; папка &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>OSDSOURCEROOT</em></p></td>
<td align="left"><p><em>UNC</em></p>
<p>URL <em> -адрес http:// </em> или <em> url-адрес https://</em></p></td>
<td align="left"><p>Позволяет администратору указать расположение источника для получения файла OSD для пакета приложения во время публикации. Корни источника OSD поддерживают пути UNC и URL-адреса (HTTP или HTTPS). Если значение равно "", то есть значение по умолчанию, используются существующие параметры OSD файла.</p>
<p>URL-адрес состоит из нескольких частей.</p>
<p>&lt;протокол &gt; :// &lt; сервер &gt; : &lt; &gt; / &lt; путь к порту &gt; / &lt; ? &gt; &lt; #fragment запросов&gt;</p>
<p>Путь в формате UNC состоит из трех частей:</p>
<p>&amp;lt; имя_компьютера &gt; &amp; lt; общий доступ к папке &gt; &amp; lt; ресурс&gt;</p>
<div class="alert">
<strong>Важно.</strong><br/><p>При использовании UNC-пути следует использовать правильный формат. Допустимые форматы: &amp; lt; сервер &gt; &amp; lt; общий доступ &gt; или &lt; буква диска &gt; : &amp; lt; папка &gt; .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>AUTOLOADONLOGIN</em></p>
<p><em>AUTOLOADONLAUNCH</em></p>
<p><em>AUTOLOADONREFRESH</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Триггеры AutoLoad, определяющие события, инициирующие автоматическую загрузку приложений. AutoLoad неявно использует фоновую потоковую передачу для обеспечения полной загрузки приложения в кэш.</p>
<p>Основной блок функций будет загружаться как можно быстрее. Оставшиеся блоки функций будут загружены в фоновом режиме, чтобы обеспечить приоритетные операции, такие как взаимодействие пользователей с приложениями, и обеспечить оптимальную производительность.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p><em>Параметр AUTOLOADTARGET </em> определяет, какие приложения загружаются автоматически. По умолчанию используемые пакеты загружаются автоматически, если <em> </em> не задано значение AUTOLOADTARGET.</p>
</div>
<div>

</div>
<p>Каждый параметр влияет на поведение при загрузке, как описано ниже.</p>
<ul>
<li><p><em>AUTOLOADONLOGIN </em> — Загрузка начинается, когда пользователь входит в систему.</p></li>
<li><p><em>AUTOLOADONLAUNCH </em> — Загрузка начинается, когда пользователь запускает приложение.</p></li>
<li><p><em>AUTOLOADONREFRESH </em> — Загрузка начинается, когда выполняется обновление публикации.</p></li>
</ul>
<p>Три значения могут быть объединены. В следующем примере триггеры AutoLoad включены как при входе пользователя, так и при обновлении публикации.</p>
<p><em>AUTOLOADONLOGIN AUTOLOADONREFRESH</em></p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Если клиент настроил эти значения при первой установке, autoload не будет срабатывать до следующего выхода из системы и повторного входа пользователя в систему.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><em>AUTOLOADTARGET</em></p></td>
<td align="left"><p>НИЧЕГО</p>
<p>ВЕСЬ</p>
<p>PREVUSED</p></td>
<td align="left"><p>Указывает, что будет автоматически загружаться при возникновении любого определенного триггера AutoLoad.</p>
<p>Возможные значения:</p>
<ul>
<li><p>NONE — без автоматической загрузки, независимо от того, какие триггеры могут быть заданы.</p></li>
<li><p>ALL (если включен какой-либо триггер AutoLoad, все пакеты загружаются автоматически, независимо от того, были ли они запущены.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Этот параметр настраивается для отдельных пакетов с помощью <strong> команд "добавить пакет" </strong> и "Настройка пакета" SFTMIME <strong> </strong> . Дополнительные сведения об этих командах можно найти в разделе <a href="sftmime--command-reference.md" data-raw-source="[SFTMIME Command Reference](sftmime--command-reference.md)"> Справочник по командам SFTMIME </a> .</p>
</div>
<div>

</div></li>
<li><p>PREVUSED — если включен какой-либо триггер AutoLoad, загрузите только те пакеты, в которых ранее использовалось хотя бы одно приложение в пакете (то есть, запущены или предварительно кэшированы).</p></li>
</ul>
<div class="alert">
<strong>Примечание.</strong><br/><p>При установке клиента App-V для использования кэша, доступного только для чтения (например, в качестве реализации сервера VDI), необходимо установить <em> </em> для параметра AUTOLOADTARGET значение None, чтобы клиент не мог обновить приложения в кэше только для чтения.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><em>DOTIMEOUTMINUTES</em></p></td>
<td align="left"><p>29600 (по умолчанию)</p>
<p>1 – 1439998560 минут (диапазон)</p></td>
<td align="left"><p>Показывает, сколько минут приложение может использоваться в отключенной операции.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>INSTALLDIR</em></p></td>
<td align="left"><p>&lt;аппарат&gt;</p></td>
<td align="left"><p>Указывает каталог установки клиента App-V.</p>
<p>Пример: INSTALLDIR = &quot; C:\Program Files\Microsoft Application Virtualization Client&quot;</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>РЕЖИМ</em></p></td>
<td align="left"><p>ЗАДАН</p>
<p>“”</p></td>
<td align="left"><p>Клиентские компоненты Microsoft Application Virtualization будут обновляться с помощью центра обновления Майкрософт, когда они доступны для общего доступа. Для агента Центра обновления Майкрософт, установленного в операционных системах Windows, требуется явное согласие пользователя на использование службы. Этот отказ требуется только один раз для всех приложений на устройстве. Если вы уже выбрали вариант "Microsoft Update", компоненты Microsoft Application Virtualization на устройстве будут автоматически использовать преимущества службы.</p>
<p>Для установки с помощью командной строки по умолчанию используется Microsoft Update (если только предыдущее приложение не включило на него) в соответствии с требованием, которое можно вручную внести в Microsoft Update. Таким образом, ожидание в установках должна быть явной для установки из командной строки. Установка для параметра "OptIn" <em> значения </em> true приводит к принудительному включению центра обновления Майкрософт.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>REQUIREAUTHORIZATIONIFCACHED</em></p></td>
<td align="left"><p>TRUE</p>
<p>FALSE</p></td>
<td align="left"><p>Указывает, требуется ли всегда проверка подлинности, независимо от того, какое приложение уже находится в кэше.</p>
<p>Возможные значения:</p>
<ul>
<li><p>TRUE — приложение всегда должно быть авторизовано при запуске. Для потоковых приложений RTSP маркер авторизации пользователя отправляется на сервер для проверки подлинности. Для файловых приложений списки ACL для файлов определяют, может ли пользователь получить доступ к приложению.</p></li>
<li><p>FALSE — всегда пытайтесь подключиться к серверу. Если не удается установить соединение с сервером, клиент по-прежнему позволяет пользователю запустить приложение, которое ранее было загружено в кэш.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWICACHESIZE</em></p></td>
<td align="left"><p>Размер кэша в МЕГАБАЙТах</p></td>
<td align="left"><p>Задает размер (в мегабайтах) кэша клиента. Размер по умолчанию составляет 4096 МБ и максимальный размер составляет 1 048 576 МБ (1 ТБ). Система проверяет наличие доступного места во время установки, но не резервирует пространство.</p>
<p>Пример: <strong> SWICACHESIZE = &quot; 1024&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRDISPLAY</em></p></td>
<td align="left"><p>Отображаемое имя</p></td>
<td align="left"><p>Указывает отображаемое имя сервера публикаций; требуется при <em> </em> использовании SWIPUBSVRHOST.</p>
<p>Пример: <strong> SWIPUBSVRDISPLAY = &quot; производственная среда&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRTYPE</em></p></td>
<td align="left"><p>[HTTP | Протокол</p></td>
<td align="left"><p>Указывает тип сервера публикаций. Тип сервера по умолчанию — сервер Application Virtualization Server. <strong>Параметр/Secure </strong> не учитывает регистр.</p>
<ul>
<li><p>HTTP (стандартный HTTP-сервер)</p></li>
<li><p>HTTP- <strong> /Secure </strong> — Улучшенная безопасность HTTP-сервер</p></li>
<li><p>RTSP (сервер Application Virtualization Server)</p></li>
<li><p>Протокол RTSP <strong> /Secure </strong> — сервер виртуализации приложений повышенной безопасности</p></li>
</ul>
<p>Пример: <strong> SWIPUBSVRTYPE = &quot; http/Secure&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRHOST</em></p></td>
<td align="left"><p>IP-адрес | имя узла</p></td>
<td align="left"><p>Указывает IP-адрес сервера виртуализации приложений или имени узла сервера, который разрешается в IP-адрес сервера&#39;s; требуется при <em> </em> использовании SWIPUBSVRDISPLAY.</p>
<p>Пример: <strong> SWIPUBSVRHOST = &quot; Server01&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRPORT</em></p></td>
<td align="left"><p>Номер порта</p></td>
<td align="left"><p>Задает логический порт, используемый этим сервером Application Virtualization для прослушивания запросов от клиента (по умолчанию = 554).</p>
<ul>
<li><p>Стандартный HTTP-сервер — по умолчанию = 80.</p></li>
<li><p>Сервер HTTP с улучшенной защитой: по умолчанию = 443.</p></li>
<li><p>Сервер Application Virtualization — значение по умолчанию = 554.</p></li>
<li><p>Сервер виртуализации приложений повышенной безопасности — по умолчанию = 322.</p></li>
</ul>
<p>Пример: <strong> SWIPUBSVRPORT = &quot; 443&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIPUBSVRPATH</em></p></td>
<td align="left"><p>Имя пути</p></td>
<td align="left"><p>Задает расположение на сервере публикации файла, в котором определяются сопоставления типов файлов (по умолчанию =/); требуется, если <em> </em> значение параметра SWIPUBSVRTYPE — HTTP.</p>
<p>Пример: <strong> SWIPUBSVRPATH = &quot; /AppVirt/appsntypes.xml&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIPUBSVRREFRESH</em></p></td>
<td align="left"><p>[Вкл. | ВЫЙТИ</p></td>
<td align="left"><p>Указывает, будет ли клиент автоматически запрашивает сервер публикаций для сопоставлений типов файлов и приложений, когда пользователь входит на клиент (по умолчанию используется значение ON).</p>
<p>Пример: <strong> SWIPUBSVRREFRESH = &quot; Off&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIGLOBALDATA</em></p></td>
<td align="left"><p>Глобальный каталог данных</p></td>
<td align="left"><p>Указывает каталог, в котором будут храниться данные, не относящиеся к конкретным пользователям (по умолчанию — C:\Documents and Settings\All Users\Documents).</p>
<p>Пример: <strong> SWIGLOBALDATA = &quot; D:\Microsoft Application Virtualization Client\Global&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SWIUSERDATA</em></p></td>
<td align="left"><p>Каталог данных пользователя</p></td>
<td align="left"><p>Указывает каталог, в котором будут храниться данные, специфичные для конкретных пользователей (по умолчанию =% APPDATA%).</p>
<p>Пример: <strong> SWIUSERDATA = &quot; H:\Windows\Microsoft Application Virtualization (клиент)&quot;</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><em>SWIFSDRIVE</em></p></td>
<td align="left"><p>Предпочтительная буква диска</p></td>
<td align="left"><p>Соответствует букве диска, выбранной для виртуального диска.</p>
<p>Пример: <strong> SWIFSDRIVE = &quot; S&quot;</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>SYSTEMEVENTLOGLEVEL</em></p></td>
<td align="left"><p>0 – 4</p></td>
<td align="left"><p>Уровень ведения журнала, на котором сообщения журнала записываются в журнал событий NT. Это значение указывает порог, который заносится в журнал, то есть все, что равно или меньше этого значения, заносится в журнал. Например, значение 0x3 (предупреждение) указывает на то, что в журнал записываются предупреждения (0x3), ошибки (0x2) и критические ошибки (0x1).</p>
<p>Возможные значения:</p>
<ul>
<li><p>0 = = нет</p></li>
<li><p>1 = = критическая</p></li>
<li><p>2 = = ошибка</p></li>
<li><p>3 = = предупреждение</p></li>
<li><p>4 = = информация</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><em>MINFREESPACEMB</em></p></td>
<td align="left"><p>В МЕГАБАЙТах</p></td>
<td align="left"><p>Задает объем свободного места (в мегабайтах), которое должно быть доступно на узле, прежде чем можно будет увеличивать размер кэша. В следующем примере в клиенте настраивается наличие не менее 5 ГБ свободного места на диске, прежде чем можно будет увеличивать размер кэша. По умолчанию используется 5000 МБАЙТ свободного места на диске во время установки.</p>
<p>Пример: <strong> MINFREESPACEMB = &quot; 5000 &quot; (5 ГБ)</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>KEEPCURRENTSETTINGS</em></p></td>
<td align="left"><p>[0 | 1]</p></td>
<td align="left"><p>Используется при применении параметров реестра перед развертыванием клиента (например, с помощью групповой политики). При развертывании клиента установите для этого параметра значение 1, чтобы не перезаписывать параметры реестра.</p>
<div class="alert">
<strong>Важно.</strong><br/><p>Если задано значение 1, игнорируются следующие параметры командной строки установщика клиента:</p>
<p><strong>SWICACHESIZE </strong> , <strong> MINFREESPACEMB </strong> , <strong> ALLOWINDEPENDENTFILESTREAMING </strong> , <strong> APPLICATIONSOURCEROOT </strong> , ICONSOURCEROOT, OSDSOURCEROOT, <strong> </strong> <strong> </strong> <strong> SYSTEMEVENTLOGLEVEL </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> <strong> </strong> , SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE и AUTOLOADTARGET.</p>
<p>Дополнительные сведения об установке этих значений после установки можно найти в разделе "Настройка параметров реестра клиента App-V с помощью командной строки" в руководстве по операциям Application Virtualization (App-V) ( <a href="https://go.microsoft.com/fwlink/?LinkId=122939" data-raw-source="[https://go.microsoft.com/fwlink/?LinkId=122939](https://go.microsoft.com/fwlink/?LinkId=122939)"> https://go.microsoft.com/fwlink/?LinkId=122939 </a> ).</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Статьи по теме


[Установка клиента Application Virtualization Client вручную](how-to-manually-install-the-application-virtualization-client.md)

[Обновление клиента Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Справочник по командам SFTMIME](sftmime--command-reference.md)









