---
title: Microsoft User Experience Virtualization (UE-V) 2. x
description: Microsoft User Experience Virtualization (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795968"
---
# Microsoft User Experience Virtualization (UE-V) 2. x

>[!NOTE]
>Эта документация является версией UE-V, которая входит в состав пакета оптимизации рабочего стола (MDOP) (Майкрософт). Сведения о последней версии UE-V, которая входит в состав Windows 10 Enterprise, приведены в разделе [Начало работы с UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Соблюдайте и разработайте параметры приложения и ОС Windows, выполнив виртуализацию Microsoft User Experience (UE-V) 2,0 или 2,1. Затем примените эти параметры к устройствам, которые пользователи получают доступ к вашим организациям, таким как настольные компьютеры, Ноутбуки и сеансы инфраструктуры виртуальных рабочих столов (VDI).

**С UE-V вы можете...**

-   Укажите, какие параметры приложения и рабочего стола следует синхронизировать

-   доставлять параметры в любое время, где бы на территории организации не работал пользователь;

-   создавать пользовательские шаблоны для сторонних приложений или бизнес-приложений;

-   Восстановление параметров после замены оборудования или обновления или после reimaging виртуальной машины в исходное состояние

## Компоненты UE-V 2. x


На этой схеме показано, как совместно развернутые компоненты UE-V работают вместе для синхронизации параметров.

![Архитектурная схема uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Компонент</th>
<th align="left">Функция</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Агент UE-V</strong></p></td>
<td align="left"><p>Установлен на всех компьютерах, которые должны синхронизировать параметры, <strong> Агент UE-V Agent </strong> отслеживает зарегистрированные приложения и операционную систему на предмет изменений параметров, а затем синхронизирует эти параметры между компьютерами.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Пакеты параметров</strong></p></td>
<td align="left"><p>Параметры приложения и параметры Windows хранятся в <strong> пакетах параметров, </strong> созданных агентом UE-V Agent. Параметры пакетов формируются, сохраняются локально и копируются в место хранения параметров.</p>
<ul>
<li><p>Значения параметров для <strong> классических приложений </strong> сохраняются, когда пользователь закрывает приложение.</p></li>
<li><p>Значения <strong> параметров Windows </strong> сохраняются при выходе пользователя из системы, при блокировке компьютера или при удаленном отключении от компьютера.</p></li>
</ul>
<p>Поставщик синхронизации определяет, когда параметры приложения или операционной системы считываются из <strong> пакетов параметров </strong> и синхронизируются.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Место хранения параметров</strong></p></td>
<td align="left"><p>Это стандартная сетевая демонстрация, к которой пользователи могут получить доступ. Агент UE-V проверяет расположение и создает скрытую системную папку, в которой хранятся и извлекаются параметры пользователей.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Шаблоны расположений параметров</strong></p></td>
<td align="left"><p>UE-V использует XML-файлы в качестве шаблонов расположения параметров для отслеживания и синхронизации параметров классических приложений и рабочего стола Windows между компьютерами пользователя. По умолчанию некоторые шаблоны расположений параметров включены в UE-V. Вы также можете создавать, изменять и проверять шаблоны расположений настраиваемых параметров, <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> управляя синхронизацией параметров для настраиваемых приложений </a> .</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Шаблоны расположений параметров не требуются для приложений для Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Список приложений для Windows</strong></p></td>
<td align="left"><p>Параметры приложений для Windows записываются и применяются динамически. Разработчик приложений определяет параметры, которые синхронизируются для каждого приложения. UE-V определяет, какие приложения для Windows включены для синхронизации параметров с помощью управляемого списка приложений. По умолчанию этот список содержит большинство приложений для Windows.</p>
<p>Вы можете добавлять и удалять приложения в списке приложений для Windows, выполнив указанные <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> ниже действия </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>Управление синхронизацией параметров для настраиваемых приложений

Используйте эти компоненты UE-V для создания и управления пользовательскими шаблонами для бизнес-приложений сторонних разработчиков.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Генератор UE-V</strong></p></td>
<td align="left"><p>Используйте <strong> генератор UE-V </strong> для создания настраиваемых шаблонов расположений параметров, которые затем можно распространять на компьютеры пользователей. Генератор UE-V также позволяет редактировать существующий шаблон или проверять шаблон, созданный с помощью другого редактора XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Каталог шаблонов параметров</strong></p></td>
<td align="left"><p><strong>Каталог шаблонов параметров </strong> — это путь к папке на компьютерах UE-V или сетевая папка SMB, в которой хранятся пользовательские шаблоны расположения параметров. Агент UE-V проверяет это расположение один раз в день, извлекает новые или обновленные шаблоны и обновляет поведение синхронизации.</p>
<p>Если используются только шаблоны расположений параметров по умолчанию UE-V, каталог шаблонов параметров не нужен. Дополнительные сведения о каталогах развертывания параметров можно найти <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> в разделе Настройка каталога шаблонов параметров ue-V </a> .</p></td>
</tr>
</tbody>
</table>



![процесс генератора UE-v](images/ue-vgeneratorprocess.gif)

## Параметры, синхронизированные по умолчанию


UE-V синхронизирует параметры для этих приложений по умолчанию. Полный список и более подробные сведения можно найти в разделе [Параметры, которые автоматически синхронизируются в развертывании UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Приложения Microsoft Office 2013 (UE-V 2,1 SP1 и 2,1)

Приложения Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 и 2,0)

Приложения Microsoft Office 2007 (только для UE-V 2,0)

Internet Explorer 8, 9 и 10

Internet Explorer 11 в UE-V 2,1 с пакетом обновления 1 (SP1) и 2,1

Многие приложения для Windows, например Xbox

Многие приложения для Windows для настольных систем, например Блокнот

Многие параметры Windows, например фоновый рисунок рабочего стола или фоновый рисунок

**Примечание.**  
Вы также можете [настроить UE-V для синхронизации параметров](https://technet.microsoft.com/library/dn458942.aspx) для других приложений, кроме тех, которые синхронизированы по умолчанию.



## Сравнение UE-V с другими продуктами Майкрософт


Используйте эту таблицу для сравнения UE-V и синхронизации профилей в Windows 7, синхронизации профилей в Windows 8 и компонента "Синхронизация параметров компьютера" учетной записи Майкрософт.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Функция</th>
<th align="left">Синхронизация профилей с помощью Windows 7</th>
<th align="left">Синхронизация профилей в Windows 8</th>
<th align="left">Синхронизация профилей с помощью Windows 10</th>
<th align="left">Учетная запись Майкрософт</th>
<th align="left">UE-V 2,0</th>
<th align="left">UE-V 2,1 и 2,1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Синхронизация параметров на нескольких компьютерах</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Синхронизация параметров между физическими и виртуальными приложениями</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Синхронизация параметров приложения для Windows</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Управление через WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Регулярно синхронизировать изменения параметров</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Минимальная конфигурация для настройки</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Поддерживается на компьютерах, не подключенных к домену</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Поддержка атрибута основного компьютера (Active Directory)</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Синхронизация параметров между инфраструктурой виртуальных рабочих столов (VDI)/Remote Desktop Services (RDS) и богатыми рабочими столами</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Неограниченный объем хранилища</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Выбор параметров приложения для синхронизации</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Резервное копирование и восстановление для ИТ-специалистов</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Частично</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## Заметки о выпуске UE-V 2. x


Дополнительные сведения и последние новости, которые не были внесены в документацию, приведены в статье

-   [Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1 с пакетом обновления 1 (SP1)](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## Другие ресурсы для этого продукта


-   [Начало работы с UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Подготовка к развертыванию UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Администрирование UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Устранение неполадок UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Технический справочник по UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### Дополнительные сведения

<a href="" id="mdop-techcenter-page"></a>[Страница TechCenter для MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Узнайте о последних сведениях и ресурсах для MDOP.

<a href="" id="mdop-information-experience"></a>[Информационные функции для MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Ознакомьтесь с документацией, видеороликами и прочими материалами, посвященными технологиям MDOP. Вы также можете [отправить нам отзыв](mailto:MDOPDocs@microsoft.com) и узнать об обновлениях, перейдя в [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) или [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).














