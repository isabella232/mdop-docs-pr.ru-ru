---
title: Подготовка UE-V развертывания 2.x
description: Подготовка UE-V развертывания 2.x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 3e4d4b69975deda473372345733d8e8593a4775d
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910534"
---
# <a name="prepare-a-ue-v-2x-deployment"></a>Подготовка UE-V развертывания 2.x


Перед развертыванием Виртуализация средств взаимодействия с пользователем (Майкрософт) (UE-V) 2.0 или 2.1 в качестве решения для синхронизации параметров между устройствами, к которые пользователи имеют доступ в вашем предприятии, необходимо подготовиться. В этом разделе вы можете определить, какой тип развертывания вы будете делать и какую подготовку вы можете сделать заранее, чтобы ваше развертывание было успешным.

Сначала рассмотрим задачи, которые вы будете выполнять для развертывания UE-V:

-   Планирование развертывания UE-V

    Прежде чем развернуть что-либо, сначала необходимо немного спланить, чтобы можно было определить, какие UE-V будут развернуты. Поэтому, если вы оставите эту страницу, убедитесь, что вы возвращались и читали сведения о планировании ниже.

-   [Развертывание необходимых компонентов для UE-v 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Каждое UE-V развертывание требует этих действий:

    -   [Определение расположения хранилища параметров](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Решение о развертывании агента UE-V и управлении UE-V конфигурациями](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Установка агента UE-V на](https://technet.microsoft.com/library/dn458891.aspx#agent) каждом компьютере пользователя, который нуждается в синхронизированной синхронизации параметров

-   Дополнительно можно развернуть UE-V [2.x для настраиваемых приложений](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    Планирование поможет вам выяснить, хотите ли вы UE-V для поддержки синхронизации параметров настраиваемого приложения (сторонних или бизнес-приложений), для чего требуются UE-V функции:

    -   [Установите генератор UEV,](https://technet.microsoft.com/library/dn458942.aspx#uevgen) чтобы можно было создавать, изменять и проверять настраиваемые шаблоны расположения параметров, необходимых для синхронизации настраиваемых параметров приложения.

    -   [Создание пользовательских шаблонов расположения](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) параметров с помощью UE-V Generator

    -   [Развертывание UE-V шаблонов параметров,](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) которые используются для хранения шаблонов расположения настраиваемой настройки

Эта схема рабочего процесса обеспечивает четкое представление о развертывании UE-V и решениях, которые определяют, как UE-V развертывание в вашем предприятии.

![развертывание.](images/deploymentworkflow.png)

**Планирование развертывания UE-V:** Сначала необходимо немного спланить, чтобы определить, какие UE-V будут развертываться. Планирование развертывания UE-V включает в себя такие вещи:

-   [Решение о синхронизации параметров настраиваемой программы](#deciding)

    Это определяет, будет ли устанавливаться генератор UE-V во время развертывания, что позволяет создавать настраиваемые шаблоны расположения параметров. Он включает в себя следующие:

    Просмотрите [параметры,](#autosyncsettings)которые синхронизируются автоматически в UE-V развертывания.

    [Определите, нужно ли синхронизировать параметры для других приложений.](#determinesettingssync)

-   Просмотрите [другие аспекты](#considerations)развертывания UE-V, такие как высокая доступность и планирование емкости.

-   [Подтверждение необходимых условий и поддерживаемых конфигураций для UE-V](#prereqs)

## <a name="decide-whether-to-synchronize-settings-for-custom-applications"></a><a href="" id="deciding"></a>Решение о синхронизации Параметры пользовательских приложений


В развертывании UE-V многие параметры автоматически синхронизируются. Но вы также можете настроить UE-V для синхронизации параметров для других приложений, таких как бизнес-приложения и сторонние приложения.

Решение о том, UE-V ли вы хотите синхронизировать параметры настраиваемого приложения, вероятно, является наиболее важной частью планирования UE-V развертывания. Темы в этом разделе помогут вам принять это решение.

### <a name="settings-that-are-automatically-synchronized-in-a-ue-v-deployment"></a><a href="" id="autosyncsettings"></a>Параметры, которые автоматически синхронизируются в UE-V развертывании

В этом разделе приводится информация о параметрах, синхронизированных по умолчанию в UE-V, включая следующие:

Настольные приложения, параметры которых синхронизируются по умолчанию

Windows параметров рабочего стола, синхронизированных по умолчанию

Заявление о поддержке синхронизации Windows настройки приложения

Чтобы скачать полный список параметров Microsoft Office 2013, Microsoft Office 2010 и 200 UE-V 7 Microsoft Office 2007 г., синхронизированных Microsoft Office, см. в UE-V [Microsoft Office.](https://www.microsoft.com/download/details.aspx?id=46367)

### <a name="desktop-applications-synchronized-by-default-in-ue-v-21-and-ue-v-21-sp1"></a>Настольные приложения, синхронизированные по умолчанию в UE-V 2.1 и UE-V 2.1 SP1

При установке агента UE-V 2.1 или 2.1 SP1 он регистрирует группу шаблонов расположения параметров по умолчанию, которые захватывают значения параметров для этих распространенных приложений Майкрософт.

**Совет**  
**Microsoft Office 2007 Параметры** — в UE-V 2.1 и 2.1 SP1 шаблон расположения параметров больше не включен по умолчанию для приложений 2007 Office 2007 г. Тем не менее, вы все еще можете использовать Office 2007 шаблонов из UE-V 2.0 или ранее и можете получить шаблоны из галереи [UE-V шаблонов](https://go.microsoft.com/fwlink/p/?LinkID=246589).



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Категория приложений</strong></th>
<th align="left"><strong>Описание</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office 2010 г.</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</p></td>
<td align="left"><p>Microsoft Word 2010, русская версия</p>
<p>Microsoft Excel 2010, русская версия</p>
<p>Microsoft Outlook 2010, русская версия</p>
<p>Microsoft Access 2010, русская версия</p>
<p>Microsoft Project 2010 г.</p>
<p>Microsoft® PowerPoint® 2010, русская версия</p>
<p>Microsoft® Publisher 2010, русская версия</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010, русская версия</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010, русская версия</p>
<p>Microsoft SharePoint Конструктор 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2013 г.</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013 г.</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint designer 2013</p>
<p>Microsoft Office 2013 Upload Центр</p>
<p>Microsoft OneDrive для бизнеса 2013</p>
<p>Шаблоны UE-V 2.1 и 2.1 SP1 Microsoft Office 2013 г. включают улучшенную поддержку Outlook подписи. Добавлена синхронизация параметров подписи по умолчанию для новых, ответных и отправленных сообщений электронной почты.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Необходимо создать Outlook для любого устройства, на котором пользователь хочет синхронизировать Outlook подписи. Если профиль еще не создан, пользователь может создать его, а затем Outlook на этом устройстве, чтобы включить синхронизацию подписи.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Параметры браузера: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 и Internet Explorer 11</p></td>
<td align="left"><p>Избранное, домашняя страница, вкладки и панели инструментов.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>UE-V не перемещает параметры cookie-файлов Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows аксессуары</p></td>
<td align="left"><p>Калькулятор (Майкрософт), Блокнот, WordPad.</p></td>
</tr>
</tbody>
</table>



**Примечание.**  
UE-V 2.1 SP1 не синхронизирует параметры между Калькулятор (Майкрософт) в Windows 10 и Калькулятор (Майкрософт) в предыдущих операционных системах.



### <a name="desktop-applications-synchronized-by-default-in-ue-v-20"></a>Настольные приложения, синхронизированные по умолчанию UE-V 2.0

При установке UE-V 2.0 Agent он регистрирует группу шаблонов расположения параметров по умолчанию, которые захватывают значения параметров для этих распространенных приложений Майкрософт.

**Совет**  
**Microsoft Office 2013 Параметры** Синхронизация — в UE-V 2.0 шаблон расположения параметров не включен по умолчанию для приложений Office 2013 г., но доступен для скачивания из [галереи шаблонов UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589). [Синхронизация Office 2013](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) г. с UE-V 2.0 содержит сведения о поддерживаемых шаблонах, синхронизируются Office 2013 г.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Категория приложений</strong></th>
<th align="left"><strong>Описание</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Office 2007 г.</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007 г.</p>
<p>Microsoft Excel 2007 г.</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007 г.</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007 г.</p>
<p>Microsoft Publisher 2007 г.</p>
<p>Microsoft SharePoint designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007 г.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Microsoft Office 2010 г.</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Скачайте список всех синхронизированных параметров </a> )</p></td>
<td align="left"><p>Microsoft Word 2010, русская версия</p>
<p>Microsoft Excel 2010, русская версия</p>
<p>Microsoft Outlook 2010, русская версия</p>
<p>Microsoft Access 2010, русская версия</p>
<p>Microsoft Project 2010 г.</p>
<p>Microsoft® PowerPoint® 2010, русская версия</p>
<p>Microsoft® Publisher 2010, русская версия</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010, русская версия</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010, русская версия</p>
<p>Microsoft SharePoint Конструктор 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Параметры браузера: Internet Explorer 8, Internet Explorer 9 и Internet Explorer 10</p></td>
<td align="left"><p>Избранное, домашняя страница, вкладки и панели инструментов.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>UE-V не перемещает параметры cookie-файлов Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Windows аксессуары</p></td>
<td align="left"><p>Калькулятор (Майкрософт), Блокнот, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a name="windows-settings-synchronized-by-default"></a><a href="" id="autosyncsettings2"></a>Windows параметров, синхронизированных по умолчанию

UE-V настроек шаблонов расположения, которые захватывают значения параметров для этих Windows параметров.

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
<th align="left">Параметры Windows</th>
<th align="left">Описание</th>
<th align="left">Применить на</th>
<th align="left">Экспорт на</th>
<th align="left">Состояние по умолчанию</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Фон рабочего стола</p></td>
<td align="left"><p>В настоящее время активный фон рабочего стола или обои.</p></td>
<td align="left"><p>Logon, unlock, remote connect, Scheduled Task events.</p></td>
<td align="left"><p>Logoff, lock, remote disconnect, user clicking <strong> Sync Now in Company Параметры </strong> Center, or scheduled task interval</p></td>
<td align="left"><p>Включено</p></td>
</tr>
<tr class="even">
<td align="left"><p>Специальные возможности</p></td>
<td align="left"><p>Параметры доступности и ввода, Microsoft Magnifier, Narrator и экранная клавиатура.</p></td>
<td align="left"><p>Только logon.</p></td>
<td align="left"><p>Logoff, щелкнуть синхронизацию пользователя в центре <strong> </strong> Параметры или интервале запланированных задач</p></td>
<td align="left"><p>Включено</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Параметры рабочего стола</p></td>
<td align="left"><p>меню и панели задач, параметры папок, значки настольных компьютеров по умолчанию, дополнительные часы и параметры Region и Language.</p></td>
<td align="left"><p>Только logon.</p></td>
<td align="left"><p>Logoff, щелкнув синхронизацию пользователя в центре <strong> </strong> Параметры компании или запланированной задачи</p></td>
<td align="left"><p>Включено</p></td>
</tr>
</tbody>
</table>



**Примечание.**  
Начиная с Windows 8, UE-V не перемещает параметры, связанные с экраном Начните, например элементы и расположения. Кроме того, UE-V не поддерживает синхронизацию закрепленных элементов панели задач или Windows ярлыков файлов.



**Важно.**  
UE-V 2.1 SP1 перемещает параметры панели задач между Windows 10 устройствами. Однако UE-V не синхронизирует параметры панели задач между Windows 10 устройствами с предыдущими операционными системами.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Группа параметров</th>
<th align="left">Категория</th>
<th align="left">Захват</th>
<th align="left">Подать заявку</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Приложение Параметры</strong></p></td>
<td align="left"><p>Приложения для Windows  </p></td>
<td align="left"><p>Закрыть приложение</p>
<p>Windows события изменения параметров приложения</p></td>
<td align="left"><p>Запуск монитора UE-V при запуске</p>
<p>Открытое приложение</p>
<p>Windows Событие Параметры приложения</p>
<p>Прибытие пакета параметров</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Классические приложения</p></td>
<td align="left"><p>Приложение закрывается</p></td>
<td align="left"><p>Приложение открывается и закрывается</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Параметры рабочего стола</strong></p></td>
<td align="left"><p>Фон рабочего стола</p></td>
<td align="left"><p>Блокировка или вход</p></td>
<td align="left"><p>Logon, unlock, remote connect, notification of new package arrival, user clicks <strong> Sync Now in Company Параметры </strong> Center, or scheduled task runs.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Простота доступа (общие — доступность, рассказчик, увеличение, экранная клавиатура)</p></td>
<td align="left"><p>Блокировка или logoff</p></td>
<td align="left"><p>Logon</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Простота доступа (Shell — аудио, доступность, клавиатура, мышь)</p></td>
<td align="left"><p>Блокировка или вход</p></td>
<td align="left"><p>Logon, unlock, remote connect, notification of new package arrival, user clicks <strong> Sync Now in Company Параметры </strong> Center, or scheduled task runs</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Параметры рабочего стола</p></td>
<td align="left"><p>Блокировка или вход</p></td>
<td align="left"><p>Logon</p></td>
</tr>
</tbody>
</table>



### <a name="ue-v-support-for-windows-apps"></a>UE-V-поддержка Windows Apps

Для Windows приложений разработчик приложения указывает синхронизированные параметры. Можно указать, Windows приложения включены для синхронизации параметров.

Чтобы отобразить список Windows приложений, которые могут синхронизировать параметры на компьютере с их семейным именем пакета, состоянием включенного и включенным источником, в командной Windows PowerShell введите: `Get-UevAppxPackage`

**Примечание.**  
По Windows 8, UE-V не синхронизирует параметры Windows, если пользователь домена связывает свои учетные данные входа со своей учетной записью Microsoft. Эта связь синхронизирует параметры с Microsoft OneDrive UE-V, что отключает синхронизацию параметров Windows приложений.



### <a name="ue-v-support-for-roaming-printers"></a>UE-V поддержки для принтеров в роуминге

UE-V 2.1 SP1 позволяет сетевым принтерам перемещаться между устройствами, чтобы пользователь получил доступ к сетевым принтерам при входе на любое устройство в сети. Это включает в себя роуминг принтера, заданной по умолчанию.

Для роуминга принтера в UE-V требуется один из этих сценариев:

-   Сервер печати может скачать необходимый драйвер при роуминге на новом устройстве.

-   Драйвер для сетевого принтера в роуминге предварительно установлен на любом устройстве, которое должно получить доступ к этому сетевому принтеру.

-   Драйвер принтера можно получить из Windows Update.

**Примечание.**  
Функция UE-V в роуминге принтера не перемещает параметры принтера или параметры, такие как печать в одностороннем окантовку. ****



### <a name="determine-whether-you-need-settings-synchronized-for-other-applications"></a><a href="" id="determinesettingssync"></a>Определите, нужно ли синхронизировать параметры для других приложений

После автоматического просмотра параметров, синхронизируются в развертывании UE-V, необходимо решить, будут ли синхронизироваться параметры для других приложений, так как это определяет, как развертывать UE-V на предприятии.

Как администратор при рассмотрении того, какие настольные приложения включить в решение UE-V, рассмотрите, какие параметры могут быть настроены пользователями, а также как и где приложение хранит свои параметры. Не во всех настольных приложениях есть параметры, которые можно настроить или которые обычно настраиваются пользователями. Кроме того, не все параметры настольных приложений можно безопасно синхронизировать на нескольких компьютерах или средах.

В общем, можно синхронизировать параметры, которые соответствуют следующим критериям:

-   Параметры, которые хранятся в доступных пользователям местах. Например, не синхронизируются параметры, хранимые в System32 или за пределами раздела HKEY\_CURRENT\_USER (HKCU) реестра.

-   Параметры, которые не являются специфическими для конкретного компьютера. Например, исключить конфигурации сети или оборудования.

-   Параметры, которые можно синхронизировать между компьютерами без риска поврежденных данных. Например, не используйте параметры, хранимые в файле базы данных.

### <a name="checklist-for-evaluating-custom-applications"></a><a href="" id="checklistsettingssync"></a>Контрольный список для оценки пользовательских приложений

Если вы решили, что вам нужны параметры, синхронизированные для других приложений, вы можете использовать этот контрольный список, чтобы выяснить, какие приложения вы будете включать.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Содержит ли это приложение параметры, которые пользователь может настроить?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Важно ли для пользователя синхронизировать эти параметры?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Эти параметры пользователей уже управляются управлением приложениями или решением политики параметров? UE-V применяет параметры приложений при запуске приложения и Windows в событиях logon, unlock или remote connect. Если вы используете UE-V с другими решениями для совместного использования параметров, пользователи могут испытывать несоответствие между синхронизированными настройками.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Являются ли параметры приложения специфическими для компьютера? Предпочтения и настройки приложений, связанные с аппаратными или определенными конфигурациями компьютеров, не синхронизируются между сеансами и могут привести к плохому опыту приложения.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Сильны ли параметры магазина приложений в каталоге Program Files или в файловом каталоге, расположенном в сильном каталоге <strong> </strong> LocalLow Для пользователей [имя &lt; &gt; </strong> &lt; &gt; </strong> пользователя]? Данные приложений, хранимые в любом из этих местоположений, обычно не должны синхронизироваться с пользователем, так как эти данные являются специфическими для компьютера или потому, что данные слишком большие, чтобы синхронизироваться.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Сохраняет ли приложение какие-либо параметры в файле, который содержит другие данные приложения, которые не должны синхронизироваться? UE-V синхронизирует файлы как единое целое. Если параметры хранятся в файлах, включающих данные приложений, помимо параметров, то синхронизация этих дополнительных данных может привести к плохому опыту приложения.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Насколько большими являются файлы, содержащие параметры? На производительность синхронизации параметров могут повлиять большие файлы. В том числе большие файлы могут повлиять на производительность синхронизации параметров.</p></td>
</tr>
</tbody>
</table>



## <a name="other-considerations-when-preparing-a-ue-v-deployment"></a><a href="" id="considerations"></a>Другие соображения при подготовке UE-V развертывания


Эти вещи следует также учитывать при подготовке к развертыванию UE-V:

-   [Управление синхронизацией учетных данных](#creds)

-   [Windows синхронизации параметров приложений](#appxsettings)

-   [Настраиваемые UE-V параметров шаблонов расположения](#custom)

-   [Конфигурации параметров непреднамеренности пользователей](#prevent)

-   [Производительность и емкость](#capacity)

-   [Высокая доступность](#high)

-   [Синхронизация часов компьютера](#clocksync)

### <a name="managing-credentials-synchronization-in-ue-v-21-and-ue-v-21-sp1"></a><a href="" id="creds"></a>Управление синхронизацией учетных данных в UE-V 2.1 и UE-V 2.1 SP1

Многие корпоративные приложения, в том числе Microsoft Outlook и Lync, подсказывая пользователям свои учетные данные домена при входе в систему. Пользователи могут сохранять учетные данные на диске, чтобы не вводить их каждый раз, когда они открывают эти приложения. Включение синхронизации учетных данных в роуминге позволяет пользователям сохранять учетные данные на одном компьютере и не вводить их повторно на каждом компьютере, который они используют в своей среде. Пользователи могут синхронизировать некоторые учетные данные домена с UE-V 2.1 и 2.1 SP1.

**Важно.**  
Синхронизация учетных данных отключена по умолчанию. Для реализации этой функции необходимо явно включить синхронизацию учетных данных во время развертывания.



UE-V 2.1 и 2.1 SP1 может синхронизировать учетные данные предприятия, но не перемещать учетные данные, предназначенные только для использования на локальном компьютере.

Учетные данные синхронны, то есть они применяются к вашему профилю при первом входе на компьютер после UE-V синхронизации.

Синхронизация учетных данных управляется собственным шаблоном расположения параметров, который отключен по умолчанию. Этот шаблон можно включить или отключить с помощью тех же методов, которые используются для других шаблонов. Идентификатор шаблона для этой функции — RoamingCredentialSettings.

**Важно.**  
Если в среде используется роуминг учетных данных Active Directory, рекомендуется не включить шаблон UE-V учетных данных.



Используйте один из этих методов для синхронизации учетных данных:

-   Центр Параметры компании

-   PowerShell

-   Групповая политика

**Примечание.**  
Учетные данные шифруются во время синхронизации.



[Центр Параметры](https://technet.microsoft.com/library/dn458903.aspx)**компании:** проверьте Параметры учетных данных Windows Параметры учетных данных. Отключать поле, чтобы отключить его. Этот контрольный ящик отображается в Центре Параметры компании, если учетная запись не настроена для синхронизации параметров с помощью учетной записи Майкрософт.

[PowerShell.](https://technet.microsoft.com/library/dn458937.aspx)**** Этот кодлет PowerShell позволяет синхронизировать учетные данные:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Этот кодлет PowerShell отключает синхронизацию учетных данных:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Групповой](https://technet.microsoft.com/library/dn458893.aspx)**политики.** Необходимо развернуть последний [шаблон MDOP ADMX,](https://go.microsoft.com/fwlink/p/?LinkId=393944) чтобы включить синхронизацию учетных данных с помощью групповой политики. Синхронизация учетных данных управляется с Windows параметров. Чтобы управлять этой функцией с помощью групповой политики, вправляйте Windows параметры.

1.  Откройте редактор групповой политики и перейдите к конфигурации пользователя — административные шаблоны **— Windows компоненты — Виртуализация средств взаимодействия с пользователем (Майкрософт)**.

2.  Дважды щелкните **параметры Windows синхронизации.**

3.  Если эта политика включена, вы можете включить синхронизацию учетных данных, проверив поле **учетных** данных в роуминге или отключив синхронизацию учетных данных путем ее отмены.

4.  Нажмите кнопку **ОК**.

### <a name="credential-locations-synchronized-by-ue-v"></a>Расположения учетных данных, синхронизированные UE-V

Файлы учетных данных, сохраненные приложениями в следующих расположениях, синхронизируются:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

Учетные данные, сохраненные в других расположениях, не синхронизируются UE-V.

### <a name="windows-app-settings-synchronization"></a><a href="" id="appxsettings"></a>Windows синхронизации параметров приложений

UE-V управляет синхронизацией параметров Windows тремя способами:

-   **Синхронизация Windows приложений:** Разрешить или запретить Windows синхронизации приложений

-   **Windows App List:** Синхронизация списка Windows приложений

-   **Не засвеченное поведение синхронизации по умолчанию:** Определите поведение синхронизации Windows приложений, которые не находятся в Windows списке приложений.

Дополнительные сведения см. в [Windows App List.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)

### <a name="custom-ue-v-settings-location-templates"></a><a href="" id="custom"></a>Настраиваемые UE-V параметров шаблонов расположения

Если вы развертываете UE-V для синхронизации параметров для настраиваемых приложений, вы будете использовать генератор UE-V для создания настраиваемых шаблонов расположения параметров для этих настольных приложений. После создания и тестирования настраиваемого шаблона расположения параметров в тестовой среде можно развернуть шаблоны расположения параметров на компьютерах предприятия.

Шаблоны расположения настраиваемых параметров должны быть развернуты с существующей инфраструктурой развертывания, например методом корпоративного распространения программного обеспечения (ESD), например System Center Configuration Manager, с настройками или путем настройки каталога шаблонов UE-V параметров. Шаблоны, развернутые с помощью диспетчера конфигурации или групповой политики, должны быть зарегистрированы с помощью UE-V WMI или Windows PowerShell.

Дополнительные сведения о настраиваемом шаблоне расположения параметров см. в [UE-V 2.x для настраиваемых приложений.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md) Дополнительные сведения об использовании UE-V в Configuration Manager см. в UE-V [2.x с System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)г.

### <a name="prevent-unintentional-user-settings-configuration"></a><a href="" id="prevent"></a>Предотвращение непреднамеренности настройки параметров пользователя

UE-V загружает новые сведения о параметрах пользователя из расположения хранилища параметров и применяет параметры на локальном компьютере в этих экземплярах:

-   Каждый раз, когда начинается приложение с зарегистрированным UE-V шаблоном.

-   При входе пользователя на компьютер.

-   Когда пользователь открывает компьютер.

-   При подключении к удаленному настольному компьютеру, который UE-V установлен.

-   При запуске запланированной задачи контроллера синхронизации.

Если UE-V установлено на компьютере A и компьютере B, а параметры, которые вы хотите для приложения, находятся на компьютере A, то сначала компьютер A должен открыть и закрыть приложение. Если приложение сначала открывается и закрывается на компьютере B, то параметры приложения на компьютере A настраиваются на параметры приложения на компьютере B. Параметры синхронизируются между компьютерами на основе каждого приложения. Со временем параметры становятся совместимыми между компьютерами по мере их открытия и закрытия с предпочтительными настройками.

Этот сценарий также применяется к Windows параметров. Если параметры Windows на компьютере B должны быть одинаковыми с Windows на компьютере A, пользователь должен войти в систему и сначала выйти из компьютера A.

Если нужные пользователю параметры применяются в неправильном порядке, они могут быть восстановлены путем выполнения операции восстановления для конкретного приложения или Windows конфигурации на компьютере, на котором были перезаписаны параметры. Дополнительные сведения см. в руб. Управление административным резервным копированием и [восстановлением в UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a name="performance-and-capacity-planning"></a><a href="" id="capacity"></a>Планирование производительности и емкости

Укажите требования к UE-V с помощью стандартных дисковой емкости и мониторинга сетевого здоровья.

UE-V для хранения пакетов параметров используется серверный блок сообщений (SMB). Размер пакетов параметров зависит от сведений о параметрах для каждого приложения. Хотя большинство пакетов параметров являются небольшими, синхронизация потенциально больших файлов, таких как изображения настольных компьютеров, может привести к низкой производительности, особенно в более медленных сетях.

Чтобы уменьшить проблемы с задержкой в сети, создайте точки хранения параметров в тех же локальных сетях, где находятся компьютеры пользователей. Для расположения хранилища параметров рекомендуется 20 МБ дискового пространства на каждого пользователя.

По умолчанию UE-V синхронизации через 2 секунды, чтобы предотвратить чрезмерное отставание из-за большого пакета параметров. Параметр SyncMethod=SyncProvider можно настроить с помощью [объектов групповой политики.](https://technet.microsoft.com/library/dn458893.aspx)

### <a name="high-availability-for-ue-v"></a><a href="" id="high"></a>Высокая доступность для UE-V

Каталог шаблонов UE-V параметров хранения и параметров шаблона поддерживает хранение данных пользователей на любой писаной совместной основе. Чтобы обеспечить высокую доступность, следуйте следующим критериям:

-   Формат хранилища с помощью файловой системы NTFS.

-   В share можно использовать распределенную файловую систему (DFS), но существуют ограничения.
В частности, поддерживается единая целевая конфигурация распределенной файловой системы (DFS-R) с пространством имен распределенной файловой системы (DFS-N) или без нее.
Кроме того, только одна целевая конфигурация поддерживается с помощью DFS-N.
Подробные сведения см. в заявлении microsoft Support [Around Replicated User Profile Data,](https://go.microsoft.com/fwlink/p/?LinkId=313991) а также сведения о политике поддержки Майкрософт для сценария развертывания [DFS-R и DFS-N.](https://support.microsoft.com/kb/2533009)

    Кроме того, поскольку SYSVOL использует DFS-R для репликации, SYSVOL не может использоваться для репликации UE-V данных.

-   Настройте разрешения на доступ к share и списки управления доступом NTFS (ACLs), указанные в развертывании Параметры служба хранилища [location для UE-V 2.x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Используйте кластеризация файлового сервера вместе с агентом UE-V для предоставления доступа к копиям данных состояния пользователя в случае сбоев связи.

-   Вы можете хранить данные о пути хранения параметров (пользовательские данные) и шаблоны шаблонов шаблонов в кластерных акциях, на акциях DFS-N или на обоих.

### <a name="synchronize-computer-clocks-for-ue-v-settings-synchronization"></a><a href="" id="clocksync"></a>Синхронизация компьютерных часов для синхронизации UE-V параметров

Компьютеры, на UE-V агенты, должны использовать сервер времени для поддержания согласованного использования параметров. UE-V использует штампы времени, чтобы определить, должны ли параметры синхронизироваться с расположением хранилища параметров. Если часы компьютера неточны, более старые параметры могут переписать более новые параметры или новые параметры могут не быть сохранены в расположении хранилища параметров.

## <a name="confirm-prerequisites-and-supported-configurations-for-ue-v"></a><a href="" id="prereqs"></a>Подтверждение необходимых условий и поддерживаемых конфигураций для UE-V


Перед началом работы убедитесь, что среда включает эти требования для UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Операционная система</strong></th>
<th align="left"><strong>Выпуск</strong></th>
<th align="left"><strong>Пакет служб</strong></th>
<th align="left"><strong>Архитектура системы</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7;</p></td>
<td align="left"><p>Ultimate, Enterprise или Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
<td align="left"><p>Windows PowerShell 3.0 или выше</p></td>
<td align="left"><p>платформа .NET Framework 4,5 или выше для UE-V 2.1.</p>
<p>платформа .NET Framework 4 или более для UE-V 2.0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Стандартный, Enterprise, центр обработки данных или веб-сервер</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>Windows PowerShell 3.0 или выше</p></td>
<td align="left"><p>платформа .NET Framework 4,5 или выше для UE-V 2.1.</p>
<p>платформа .NET Framework 4 или более для UE-V 2.0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 и Windows 8.1</p></td>
<td align="left"><p>Enterprise или Pro</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
<td align="left"><p>Windows PowerShell 3.0 или выше</p></td>
<td align="left"><p>платформа .NET Framework 4,5 или выше</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10 версии до 1607 г.</p>
<div class="alert">
<strong>Примечание.</strong><br/><p>Только UE-V 2.1 SP1 поддерживает Windows 10 версии до 1607 г.</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise или Pro</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>32- или 64-разрядная</p></td>
<td align="left"><p>Windows PowerShell 3.0 или выше</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 и Windows Server 2012 R2</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>Windows PowerShell 3.0 или выше</p></td>
<td align="left"><p>платформа .NET Framework 4,5 или выше</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2016</p></td>
<td align="left"><p>Стандартный или центр обработки данных</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>64-разрядная</p></td>
<td align="left"><p>Windows PowerShell 3.0 или выше</p></td>
<td align="left"><p>платформа .NET Framework 4,6 или выше</p></td>
</tr>
</tbody>
</table>



Кроме того, ...

-   **Лицензия MDOP:** Эта технология входит в пакет оптимизации рабочего стола Майкрософт (MDOP). Enterprise клиенты могут получать MDOP с помощью Microsoft Software Assurance. Дополнительные сведения о Microsoft Software Assurance и приобретении MDOP см. в дополнительных сведениях о том, как получить MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Административные учетные данные** для любого компьютера, на котором вы будете устанавливаться

**Примечание.**  

-   Начиная с WIndows 10 версии 1607, UE-V включена в Windows 10 для [Enterprise](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) и больше не входит в пакет оптимизации рабочего стола Майкрософт.

-   Для UE-V Windows PowerShell агента UE-V требуется платформа .NET Framework 4 или более Windows PowerShell 3,0 или выше. Скачать Windows PowerShell 3.0 [здесь](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Установите платформа .NET Framework 4 или платформа .NET Framework 4.5 на компьютеры с Windows 7 или операционной системой Windows Server 2008 R2. Операционные Windows 8, Windows 8.1 и Windows Server 2012 установлены платформа .NET Framework 4.5. Операционная Windows 10 поставляется с установленным платформа .NET Framework 4.6.
-   Политика "Удаление кэша в роуминге" для обязательных профилей не поддерживается UE-V и не должна использоваться.



Не существует специальных требований к памяти случайного доступа (ram) для UE-V.

### <a name="synchronization-of-settings-through-the-sync-provider"></a>Синхронизация Параметры через поставщика синхронизации

Поставщик синхронизации — это параметр по умолчанию для пользователей, который синхронизирует локальный кэш с расположением хранилища параметров в этих экземплярах:

-   Logon/logoff

-   Блокировка/разблокировка

-   Удаленное подключение и отключение рабочего стола

-   Приложение open/close

Запланированная задача управляет этой синхронизацией параметров каждые 30 минут или с помощью определенных событий триггера для определенных приложений. Дополнительные сведения см. в руб. Изменение UE-V [2.x Запланированные задачи.](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

Агент UE-V синхронизирует параметры пользователей для компьютеров, которые не всегда подключены к корпоративной сети (удаленные компьютеры и ноутбуки) и компьютеров, которые всегда подключены к сети (компьютеры, которые работают Windows Server и хост виртуальный интерфейс рабочего стола (VDI).

**Синхронизация для компьютеров с всегда доступными подключениями:** При использовании UE-V на компьютерах, всегда подключенных к сети, необходимо настроить агент UE-V для синхронизации параметров с помощью параметра *SyncMethod=None,* который обрабатывает сервер хранилища параметров в качестве стандартной сетевой доли. В этой конфигурации UE-V агент может быть настроен для уведомления о задержке импорта параметров приложения.

Включить эту конфигурацию с помощью одного из этих методов:

-   Во UE-V установки в командной подсказке или пакетном файле установите параметр AgentSetup.exe *SyncMethod = None*. [Развертывание UE-V 2.x Agent](https://technet.microsoft.com/library/dn458891.aspx#agent) предоставляет дополнительные сведения.

-   После установки UE-V используйте функцию управления Параметры в System Center 2012 или шаблоны MDOP ADMX, чтобы нажать конфигурацию *SyncMethod = None.*

-   Используйте Windows PowerShell или Windows управления (WMI) для настройки *конфигурации SyncMethod = None.*

    **Примечание.**  
    Эти два последних метода не работают для среды виртуальной инфраструктуры настольных компьютеров (VDI).



Необходимо перезапустить компьютер до начала синхронизации параметров.

**Примечание.**  
Если вы *задаете SyncMethod = None,* любые изменения параметров сохраняются непосредственно на сервере. Если сетевое подключение к пути хранения параметров не найдено, изменения параметров кэшируются на устройстве и синхронизируются при следующем запуске поставщика синхронизации. Если путь хранения параметров не найден и профиль пользователя удаляется из пула среды VDI при входе в систему, параметры теряются, и пользователь должен повторно внести изменения при повторном присоединении компьютера к пути хранения параметров.



**Синхронизация для внешних двигателей синхронизации:** Параметр *SyncMethod=External* указывает, что если UE-V параметров записаны в локализованную папку на компьютере пользователя, то любой внешний механизм синхронизации (например, OneDrive для бизнеса, work folders, Sharepoint или Dropbox) может использоваться для применения этих параметров на различных компьютерах, к которые имеют доступ пользователи.

**Поддержка общих сеансов VDI:** UE-V 2.1 и 2.1 SP1 обеспечивают поддержку сеансов VDI, которые разделяются между конечными пользователями. Вы можете зарегистрировать и настроить специальный шаблон VDI, который гарантирует, что UE-V все его функциональные возможности не повреждены для неустанных сеансов VDI.

**Примечание.**  
Если режим VDI не включается для нестационарных сеансов VDI, некоторые функции не работают, например, [back-up/restore и](https://technet.microsoft.com/library/dn878331.aspx)последнее известное хорошее (LKG).



Шаблон VDI предоставляется с UE-V 2.1 и 2.1 SP1 и обычно доступен здесь после установки: C:\\Program Files\\Microsoft User Experience Virtualization\\Templates\\VdiState.xml

### <a name="prerequisites-for-ue-v-generator-support"></a>Необходимые условия для UE-V генератора

Установите генератор UE-V на компьютере, который используется для создания настраиваемых шаблонов расположения параметров. Этот компьютер должен иметь возможность запускать приложения, параметры которых синхронизированы. Вы должны быть членом группы Администраторы на компьютере, который запускает программное обеспечение UE-V Генератор.

Генератор UE-V должен быть установлен на компьютере, использующем файловую систему NTFS. Программное обеспечение UE-V генератора требует платформа .NET Framework 4. Дополнительные сведения см. в [UE-V 2.x для настраиваемых приложений.](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

## <a name="other-resources-for-this-product"></a>Другие ресурсы для этого продукта


-   [Виртуализация средств взаимодействия с пользователем (Майкрософт) (UE-V) 2.x](index.md)

-   [Начало работы с UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Администрирование UE-V 2.x](administering-ue-v-2x-new-uevv2.md)

-   [Устранение неполадок UE-V 2.x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Технический справочник по UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














