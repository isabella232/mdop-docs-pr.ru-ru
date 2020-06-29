---
title: Поддерживаемые конфигурации в App-V 5.0
description: Поддерживаемые конфигурации в App-V 5.0
author: dansimp
ms.assetid: 3787ff63-7ce7-45a8-8f01-81b4b6dced34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 60236743d2a6b418ca7f4705168a7bf064b82156
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814789"
---
# Поддерживаемые конфигурации в App-V 5.0


В этой статье указаны требования, необходимые для установки и запуска Microsoft Application Virtualization (App-V) 5,0 в среде.

**Важно.**  
**Поддерживаемые конфигурации, описанные в этой статье, относятся только к приложению App-V 5,0**. Поддерживаемые конфигурации, которые относятся к пакетам обновления App-V 5,0, можно найти на веб-страницах ниже.

-   [Новые возможности в App-V 5.0 с пакетом обновления 1 (SP1)](whats-new-in-app-v-50-sp1.md)

-   [Сведения об App-V 5.0 с пакетом обновления 2 (SP2)](about-app-v-50-sp2.md)

-   [Поддерживаемые конфигурации App-V 5.0 с пакетом обновления 3 (SP3)](app-v-50-sp3-supported-configurations.md)



## <a href="" id="---------app-v-5-0-server-system-requirements"></a> Требования к серверной системе для App-V 5,0


**Важно.**  
Сервер App-V 5,0 не поддерживает указанные ниже сценарии.



-   Развертывание на компьютере, на котором запущен Microsoft Windows Server Core.

-   Развертывание на компьютере, на котором установлена предыдущая версия App-V 5,0 Server.

    **Примечание.**  
    Вы можете установить App-V 5,0 рядом с сервером App-V 4,5 Lightweight Streaming Server (LWS). Развертывание App-V 5,0 с помощью службы управления виртуализацией приложений App-V 4,5 (HWS) не поддерживается.



-   Развертывание на компьютере, на котором запущен Microsoft SQL Server, Экспресс-выпуск.

-   Удаленное развертывание базы данных сервера управления или базы данных отчетов. Чтобы успешно установить базу данных, необходимо запустить установщик прямо на компьютере с Microsoft SQL.

-   Развертывание на контроллере домена.

-   Короткие пути не поддерживаются. Если вы планируете использовать короткий путь, вы должны создать новый том.

### Требования к операционной системе для сервера управления

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера управления App-V 5,0.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 (стандартный, корпоративный, центр обработки данных или веб-сервер)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"><p>SP1 и более позднюю версию</p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (стандартный центр обработки данных)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (стандартный центр обработки данных)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



**Важно.**  
Развертывание роли сервера управления на компьютере с включенным удаленным доступом к рабочему столу не поддерживается.



### <a href="" id="management-server-hardware-requirements-"></a>Требования к оборудованию сервера управления

-   Процессор (с тактовой частотой 1,4 ГГц или более мощный, 64-разрядный (x64) процессор

-   ОЗУ — 1 ГБ ОЗУ (64-разр.)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске, не включая каталог содержимого.

### Требования к операционной системе сервера публикаций

В таблице ниже перечислены операционные системы, которые поддерживаются в установке сервера публикаций App-V 5,0.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 (стандартный, корпоративный, центр обработки данных или веб-сервер)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (стандартный центр обработки данных)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (стандартный центр обработки данных)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



### <a href="" id="publishing-server-hardware-requirements-"></a>Требования к оборудованию сервера публикаций

-   Процессор – 1,4 ГГц или более мощный. 64-разрядный процессор (x64)

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске. не включает каталог контента

### Требования к операционной системе сервера отчетов

В таблице ниже перечислены операционные системы, которые поддерживаются при установке сервера Reporting Server App-V 5,0.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2008 (стандартный, корпоративный, центр обработки данных или веб-сервер)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"><p></p></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2012 (стандартный центр обработки данных)</p></td>
<td align="left"><p></p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012 (стандартный центр обработки данных)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



### <a href="" id="reporting-server-hardware-requirements-"></a>Требования к оборудованию сервера отчетов

-   Процессор – 1,4 ГГц или более мощный. 64-разрядный процессор (x64)

-   ОЗУ — 2 ГБ ОЗУ (64-разрядная версия)

-   Место на диске — 200 МБАЙТ свободного места на жестком диске

### <a href="" id="sql-server-database-requirements-"></a>Требования к базам данных SQL Server

В следующей таблице перечислены версии SQL Server, которые поддерживаются для базы данных App-V 5,0 и сервера.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Тип сервера App-V 5,0</th>
<th align="left">Версия SQL Server</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Управление и отчетность</p></td>
<td align="left"><p>Microsoft SQL Server 2008</p>
<p>(Standard, предприятие, центр обработки данных или выпуск разработчика с помощью следующего компонента: <strong> Службы ядра СУБД </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Управление и отчетность</p></td>
<td align="left"><p>Microsoft SQL Server 2008 </p>
<p>(Standard, предприятие, центр обработки данных или выпуск разработчика с помощью следующего компонента: <strong> Службы ядра СУБД </strong> .)</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"><p>SP2</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Управление и отчетность</p></td>
<td align="left"><p>Microsoft SQL Server 2012</p>
<p>(Standard, предприятие, центр обработки данных или выпуск разработчика с помощью следующего компонента: <strong> Службы ядра СУБД </strong> .)</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-client-supp-cfgs"></a> Требования к системе клиента App-V 5,0


В таблице ниже перечислены операционные системы, которые поддерживаются при установке клиента App-V 5,0.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Важно.</strong><br/><p>Windows 8,1 поддерживается только приложением App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
</tbody>
</table>



Следующие сценарии установки клиента App-V не поддерживаются, за исключением случаев, указанных ниже.

-   Компьютеры под управлением Windows Server

-   Компьютеры под управлением App-V 4,6 SP1 или более ранних версий

-   Клиент служб удаленных рабочих столов App-V 5,0 поддерживается только для серверов с поддержкой служб удаленных рабочих столов.

### <a href="" id="client-hardware-requirements-"></a>Требования к оборудованию клиента

В списке ниже показана конфигурация оборудования, поддерживаемая установкой клиента App-V 5,0.

-   Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)

-   ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)

-   Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.

## <a href="" id="---------app-v-5-0-remote-desktop-client-system-requirements"></a> Требования к клиентской системе для удаленных рабочих столов для App-V 5,0


В приведенной ниже таблице перечислены операционные системы, которые поддерживаются при установке клиента для удаленного рабочего стола App-V 5,0.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



Выпуск операционной системы, пакет обновления Microsoft Windows Server 2008

ОС

SP1

Microsoft Windows Server 2012

**Важно.**  
Windows Server 2012 R2 поддерживается только приложением App-V 5,0 SP2



Microsoft Windows Server 2012 (стандартный центр обработки данных)

ОС

64-разрядная



### <a href="" id="remote-desktop-client-hardware-requirements-"></a>Требования к оборудованию клиента удаленных рабочих столов

В списке ниже показана конфигурация оборудования, поддерживаемая установкой клиента App-V 5,0.

-   Процессор — процессор с тактовой частотой 1,4 ГГц или более 32 мощный (x86) или 64-bit (x64)

-   ОЗУ — 1 ГБ (32-разрядная версия) или 2 ГБ (64-разр.)

-   Диск — 100 МБАЙТ для установки, не включая пространство на диске, используемое виртуализированными приложениями.

## <a href="" id="---------app-v-5-0-sequencer-system-requirements"></a> Требования к системе Sequencer для App-V 5,0


В следующей таблице перечислены операционные системы, которые поддерживаются при установке App-V 5,0 Sequencer.

**Примечание.**  
Корпорация Майкрософт предоставляет поддержку для текущего пакета обновления и, в некоторых случаях, непосредственно предыдущего пакета обновления. Чтобы найти временные шкалы поддержки вашего продукта, обратитесь к разделу [Поддерживаемые пакеты обновления для жизненного цикла](https://go.microsoft.com/fwlink/p/?LinkId=31975). Дополнительные сведения о политике поддержки жизненного цикла продуктов Майкрософт можно найти в разделе [вопросы и ответы о поддержке в течение жизненного](https://go.microsoft.com/fwlink/p/?LinkId=31976)цикла поддержки Майкрософт.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Выпуск</th>
<th align="left">Пакет обновления</th>
<th align="left">Системная архитектура</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Windows 7</p></td>
<td align="left"></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows 8</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><div class="alert">
<strong>Важно.</strong><br/><p>Windows 8,1 поддерживается только приложением App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Windows 8.1</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Windows Server 2008</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Windows Server 2012</p></td>
<td align="left"></td>
<td align="left"><p></p></td>
<td align="left"><p>32- и 64-разрядная</p></td>
</tr>
<tr class="even">
<td align="left"><div class="alert">
<strong>Важно.</strong><br/><p>Windows Server 2012 R2 поддерживается только приложением App-V 5,0 SP2</p>
</div>
<div>

</div>
<p>Microsoft Windows Server 2012</p></td>
<td align="left"><p>ОС</p></td>
<td align="left"></td>
<td align="left"><p>64-разрядная</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-supp-ver-sccm"></a>Поддерживаемые версии System Center Configuration Manager


Вы можете использовать Microsoft System Center 2012 Configuration Manager или System Center 2012 R2 Configuration Manager для управления виртуальными приложениями App-V, отчетами и другими функциями. В следующей таблице перечислены поддерживаемые версии Configuration Manager для каждой применимой версии App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Поддерживаемая версия Configuration Manager</th>
<th align="left">Версия App-V</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft System Center 2012 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>System Center 2012 R2 Configuration Manager</p></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
</tr>
</tbody>
</table>



Дополнительные сведения о том, как Configuration Manager интегрируется с App-V, можно найти в разделе [Планирование интеграции App-v с Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx).






## Статьи по теме


[Планирование развертывания App-V](planning-to-deploy-app-v.md)

[Предварительные требования App-V 5.0](app-v-50-prerequisites.md)









