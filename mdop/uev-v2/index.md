---
title: Виртуализация средств взаимодействия с пользователем (Майкрософт) (UE-V) 2.x
description: Виртуализация средств взаимодействия с пользователем (Майкрософт) (UE-V) 2.x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 79748e04ae1a59afdc8f9dae3c5dc77c50e3c253
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910544"
---
# <a name="microsoft-user-experience-virtualization-ue-v-2x"></a>Виртуализация средств взаимодействия с пользователем (Майкрософт) (UE-V) 2.x

>[!NOTE]
>Эта документация является версией UE-V, которая была включена в пакет оптимизации рабочего стола Майкрософт (MDOP). Сведения о последней версии UE-V, которая включена в Windows 10 Корпоративная, см. Начало работы [с UE-V](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Захват и централизация параметров приложений и Windows оси путем реализации Виртуализация средств взаимодействия с пользователем (Майкрософт) (UE-V) 2.0 или 2.1. Затем примените эти параметры к устройствам, к доступу пользователей на предприятии, например к настольным компьютерам, ноутбукам или сеансам виртуальной инфраструктуры настольных компьютеров (VDI).

**С UE-V вы можете ...**

-   Укажите, какие параметры приложений и настольных компьютеров синхронизируются

-   доставлять параметры в любое время, где бы на территории организации не работал пользователь;

-   создавать пользовательские шаблоны для сторонних приложений или бизнес-приложений;

-   Восстановление параметров после замены оборудования или обновления или после повторного обновления виртуальной машины в исходное состояние.

## <a name="components-of-ue-v-2x"></a>Компоненты UE-V 2.x


На этой схеме показано, как развернутые UE-V компоненты работают вместе для синхронизации параметров.

![архитектурная схема uev2.](images/uev2archdiagram.gif)

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
<td align="left"><p><strong>UE-V Агент</strong></p></td>
<td align="left"><p>Установленный на каждом компьютере, который должен синхронизировать параметры, агент UE-V отслеживает зарегистрированные приложения и операционную систему для любых изменений параметров, а затем синхронизирует эти параметры между <strong> </strong> компьютерами.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Параметры пакеты</strong></p></td>
<td align="left"><p>Параметры приложений и Windows хранятся в пакетах параметров, созданных <strong> </strong> агентом UE-V агентом. Параметры пакетов формируются, сохраняются локально и копируются в место хранения параметров.</p>
<ul>
<li><p>Значения параметров для настольных приложений сохраняются при закрытии <strong> </strong> приложения пользователем.</p></li>
<li><p>Значения для Windows сохраняются при отключении пользователя, при блокировке компьютера или удаленном отключении пользователя <strong> </strong> от компьютера.</p></li>
</ul>
<p>Поставщик синхронизации определяет, когда параметры приложения или операционной системы читают из Параметры <strong> пакетов </strong> и синхронизируются.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Параметры хранилища</strong></p></td>
<td align="left"><p>Это стандартная сеть, к которую пользователи могут получить доступ. Агент UE-V проверяет расположение и создает скрытую папку системы, в которой можно хранить и извлекать параметры пользователя.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Параметры расположения</strong></p></td>
<td align="left"><p>UE-V XML-файлы используются в качестве шаблонов параметров расположения для мониторинга и синхронизации параметров настольных приложений и Windows параметров рабочего стола между пользовательскими компьютерами. По умолчанию некоторые шаблоны расположения параметров включены в UE-V. Вы также можете создавать, изменять или проверять настраиваемые шаблоны расположения параметров, управляя синхронизацией параметров <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> для пользовательских </a> приложений.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Параметры шаблоны расположения не требуются для Windows приложений.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Windows приложения</strong></p></td>
<td align="left"><p>Параметры для Windows приложения захватываются и применяются динамически. Разработчик приложения указывает параметры, синхронизированные для каждого приложения. UE-V определяет, какие Windows приложения включены для синхронизации параметров с помощью управляемого списка приложений. По умолчанию этот список включает большинство Windows приложений.</p>
<p>Вы можете добавить или удалить приложения в списке Windows, следуя процедурам, показанным <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> </a> здесь.</p></td>
</tr>
</tbody>
</table>



### <a name="managing-settings-synchronization-for-custom-applications"></a><a href="" id="customapps"></a>Управление синхронизацией Параметры пользовательских приложений

Используйте эти UE-V для создания и управления пользовательскими шаблонами для сторонних или бизнес-приложений.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Генератор</strong></p></td>
<td align="left"><p>Используйте генератор UE-V для создания настраиваемых шаблонов расположения параметров, которые можно затем распространить <strong> </strong> на компьютеры пользователей. Генератор UE-V также позволяет изменить существующий шаблон или проверить шаблон, созданный с помощью другого редактора XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Параметры шаблона</strong></p></td>
<td align="left"><p>Каталог шаблонов параметров — это путь папки на UE-V или сетевой блок сообщений сервера, который хранит настраиваемые шаблоны расположения <strong> </strong> параметров. Агент UE-V проверяет это расположение один раз в день, извлекает новые или обновленные шаблоны и обновляет свое поведение синхронизации.</p>
<p>Если вы используете только шаблоны UE-V параметров расположения по умолчанию, каталог шаблонов параметров не является ненужным. Дополнительные сведения о каталогах развертывания параметров см. в каталоге <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> шаблонов UE-V </a> параметров.</p></td>
</tr>
</tbody>
</table>



![процесс генератора ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-synchronized-by-default"></a>Параметры Синхронизация по умолчанию


UE-V по умолчанию синхронизирует параметры для этих приложений. Полный список и более подробные сведения см. в Параметры, которые автоматически синхронизируются в [UE-V развертывания.](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings)

Microsoft Office 2013 г. (UE-V 2.1 SP1 и 2.1)

Microsoft Office 2010 приложений (UE-V 2.1 SP1, 2.1 и 2.0)

Microsoft Office 2007 приложений (только UE-V 2.0)

Internet Explorer 8, 9 и 10

Internet Explorer 11 в UE-V 2.1 SP1 и 2.1

Многие Windows, такие как Xbox

Многие Windows настольные приложения, например Блокнот

Многие Windows параметров, таких как фон рабочего стола или обои

**Примечание.**  
Вы также можете настроить [UE-V](https://technet.microsoft.com/library/dn458942.aspx) для синхронизации параметров для приложений, не синхронизированных по умолчанию.



## <a name="compare-ue-v-to-other-microsoft-products"></a>Сравнение UE-V с другими продуктами Майкрософт


С помощью этой таблицы UE-V синхронизировать профили в Windows 7, синхронизировать профили в Windows 8 и функцию sync PC Параметры учетной записи Майкрософт.

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
<th align="left">Синхронизация профилей с Windows 7</th>
<th align="left">Синхронизация профилей с помощью Windows 8</th>
<th align="left">Синхронизация профилей с Windows 10</th>
<th align="left">Учетная запись Майкрософт</th>
<th align="left">UE-V 2.0</th>
<th align="left">UE-V 2.1 и 2.1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Синхронизация параметров между несколькими компьютерами</p></td>
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
<td align="left"><p>Синхронизация Windows параметров приложения</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Управление с помощью WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Синхронизация изменений параметров на регулярной основе</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Минимальная конфигурация для установки</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Поддерживается на компьютерах, не вступив в домен,</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Поддерживает атрибут Primary Computer Active Directory</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Синхронизация параметров между виртуальной инфраструктурой настольных компьютеров (VDI)/Remote Desktop Services (RDS) и богатыми настольными компьютерами</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Неограниченное пространство для хранения параметров</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Выбор синхронизации параметров приложения</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Резервное копирование и восстановление для ИТ-Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Частично</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## <a name="ue-v-2x-release-notes"></a>UE-V 2.x Заметки о выпуске


Дополнительные сведения и последние новости, не ворвавшись в документацию, см. в

-   [Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1 с пакетом обновления 1 (SP1)](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## <a name="other-resources-for-this-product"></a>Другие ресурсы для этого продукта


-   [Начало работы с UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Подготовка UE-V развертывания 2.x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Администрирование UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Устранение неполадок UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Технический справочник по UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### <a name="more-information"></a>Дополнительные сведения

<a href="" id="mdop-techcenter-page"></a>[Страница TechCenter MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Сведения о последних сведениях и ресурсах MDOP.

<a href="" id="mdop-information-experience"></a>[Опыт работы с сведениями MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Найдите документацию, видео и другие ресурсы для технологий MDOP. Вы также можете [отправить нам отзывы](mailto:MDOPDocs@microsoft.com) или узнать об обновлениях, следуя за нами на [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) или [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).














