---
title: Планирование использования App-V с Office
description: Планирование использования App-V с Office
author: dansimp
ms.assetid: c4371869-4bfc-4d13-9198-ef19f99fc192
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff523c8f8827e295c8fb9a2d9fd0e02d5b019aa8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813424"
---
# Планирование использования App-V с Office


Используйте следующие сведения, чтобы спланировать развертывание Office с помощью App-V. В этой статье рассматриваются следующие статьи:

-   [Поддержка языковых пакетов для App-V](#bkmk-lang-pack)

-   [Поддерживаемые версии Microsoft Office](#bkmk-office-vers-supp-appv)

-   [Планирование использования App-V с помощью косуществующих версий Office](#bkmk-plan-coexisting)

-   [Интеграция Office с Windows при развертывании Office с помощью App-V](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>Поддержка языковых пакетов для App-V


С помощью секвенсора App-V 5,0 вы можете создавать пакеты для языков, языковых интерфейсов, средств проверки правописания и языков всплывающих подсказок. Затем вы можете включить пакеты плагинов в группу соединения вместе с пакетом Office 2013, созданным с помощью набора средств развертывания Office. Приложения Office и языковые пакеты с поддержкой плагинов легко взаимодействуют в одной группе, так же как и любые другие пакеты, сгруппированные вместе в группу подключений.

**Примечание**  Microsoft Visio и Microsoft Project не предоставляют поддержку для языкового пакета на тайском языке.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>Поддерживаемые версии Microsoft Office


В следующей таблице перечислены версии Microsoft Office, которые поддерживаются приложением App-V, методы создания пакетов Office, поддерживаемые лицензированные и поддерживаемые развертывания.

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
<th align="left">Поддерживаемая версия Office</th>
<th align="left">Поддерживаемые версии App-V</th>
<th align="left">Создание пакета</th>
<th align="left">Поддерживаемое лицензирование</th>
<th align="left">Поддерживаемые развертывания</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Приложения Microsoft 365 для предприятий</p>
<p>Также поддерживаются следующие возможности:</p>
<ul>
<li><p>Visio Pro для Office 365</p></li>
<li><p>Project Pro для Office 365</p></li>
</ul></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
<td align="left"><p>Средство развертывания Office</p></td>
<td align="left"><p>Подписка</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>Персональный VDI</p></li>
<li><p>VDI из пула</p></li>
<li><p>СЛУЖБ</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Office профессиональный плюс 2013</p>
<p>Также поддерживаются следующие возможности:</p>
<ul>
<li><p>Visio профессиональный 2013</p></li>
<li><p>Project профессиональный 2013</p></li>
</ul></td>
<td align="left"><ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
</ul></td>
<td align="left"><p>Средство развертывания Office</p></td>
<td align="left"><p>Корпоративное лицензирование</p></td>
<td align="left"><ul>
<li><p>Desktop</p></li>
<li><p>Персональный VDI</p></li>
<li><p>VDI из пула</p></li>
<li><p>СЛУЖБ</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-plan-coexisting"></a>Планирование использования App-V с помощью косуществующих версий Office


Вы можете установить более одной версии Microsoft Office на одном компьютере, используя "Microsoft Office сосуществование". Вы можете реализовать сосуществование Office со всеми основными версиями Office и методами установки, как это применимо с помощью установщика Windows (MSi), технологии "нажми и работай" и App-V 5,0 SP2. Тем не менее использование сосуществования Office не рекомендуется корпорацией Майкрософт.

Рекомендуется не допустить проблем с совместимостью, но корпорация Майкрософт рекомендует избегать сосуществования Office полностью. Однако при переходе на более новую версию Office иногда возникают проблемы, которые не удается устранить немедленно, поэтому вы можете временно реализовать сосуществование, чтобы упростить миграцию в последнюю версию продукта. Использование сосуществования Office на долгосрочной основе не рекомендуется, и ваша организация должна иметь план на полную смену в будущем.

### Перед реализацией сосуществования Office

Перед реализацией сосуществования Office ознакомьтесь со следующей документацией по Office. Выберите статью, соответствующую последней версии Office, для которой вы планируете реализовать сосуществование.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Версия Office</th>
<th align="left">Ссылка на руководство</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">Сведения об использовании наборов и программ Office 2013 (развертывание MSI) на компьютере, на котором работает другая версия Office</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">Сведения об использовании наборов и программ Office 2010 на компьютере под управлением другой версии Office</a></p></td>
</tr>
</tbody>
</table>

 

Документация по Office содержит обширные рекомендации по сосуществованию установщика Windows (MSi) и установке Office нажми и работай. Этот раздел App-V в сосуществовании дополняет Руководство по Office информацией, более специфичной для развертывания App-V.

### Поддерживаемые сценарии сосуществования Office

В приведенных ниже таблицах перечислены поддерживаемые сценарии сосуществования. Они организованы в соответствии с версией и развертыванием, с которым вы работаете, и версией и методом развертывания, на которые вы мигрируют. Обязательно протестируйте все решения сосуществования перед развертыванием их в рабочую аудиторию.

**Примечание**  Корпорация Microsoft не поддерживает использование нескольких версий Office в средах Windows Server, в которых включена служба роли узла сеансов удаленных рабочих столов. Для запуска сценариев сосуществования Office необходимо отключить эту службу роли.

 

### Интеграция с Windows & сосуществования Office

Средства установки Office, созданные с помощью установщика Windows, интегрируются с определенными точками базовой операционной системы Windows. При использовании сосуществования распространенная интеграция операционной системы между двумя версиями Office может привести к конфликтам, которые приводят к возникновению проблем с совместимостью и взаимодействии с пользователем. С помощью App-V вы можете поочередно использовать определенные версии Office для исключения интеграции, тем самым "изолировать" их от операционной системы.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Режим, в котором App-V может поочередно последовательностей в этой версии Office</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>Всегда не интегрированы. Приложение App-V не предлагает интеграции операционной системы с виртуализированной версией Office 2007.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>Интегрированный и не интегрированный режим.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>Всегда интегрируются. Интеграция с операционной системой Windows не может быть отключена.</p></td>
</tr>
</tbody>
</table>

 

Корпорация Microsoft рекомендует развертывать сосуществование Office только с помощью одного из встроенных экземпляров Office. Например, если вы используете App-V для развертывания Office 2010 и Office 2013, вы должны поочередно использовать Office 2010 в неинтегрированном режиме. Дополнительные сведения о том, как последовательное использование Office в режиме без интеграции (изолированном), описаны в разделе [как пошаговые инструкции для Microsoft Office 2010 в Microsoft Application Virtualization 5,0](https://support.microsoft.com/kb/2830069).

### Известные ограничения сценариев сосуществования Office

В следующих разделах описаны некоторые проблемы, которые могут возникнуть при использовании App-V для реализации сосуществования с помощью Office.

### Ограничения, характерные для сценариев совместного существования с помощью установщика Windows, а затем — для выполнения и App-V.

При установке следующих версий Office на одном компьютере могут возникать указанные ниже ограничения.

-   Office 2010 с помощью установщика Windows

-   Office 2013 с помощью App-V

После публикации Office 2013 с помощью приложения-V рядом с более ранней версией 2010 Office, основанной на установщике Windows, может также быть запуск установщика Windows. Это происходит из-за того, что версия Office 2010, основанная на установщиках Windows или "нажми и работай", пытается автоматически зарегистрироваться на компьютере.

Чтобы отключить автоматическую регистрацию для приложения Word 2010, выполните указанные ниже действия.

1.  Закройте приложение Word 2010.

2.  Запустите редактор реестра, выполнив указанные ниже действия.

    -   В Windows 7: нажмите кнопку **Пуск**, введите **regedit** в поле начать поиск и нажмите клавишу ВВОД.

    -   В Windows 8 введите **regedit** нажмите клавишу ВВОД на начальной странице и нажмите клавишу ВВОД.

    Если вам будет предложено ввести пароль администратора или подтверждение, введите пароль или нажмите кнопку **продолжить**.

3.  Найдите и выделите следующий подраздел реестра:

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  В меню **Правка** выберите пункт **создать**, а затем — параметр **DWORD**.

5.  Введите **NoReReg**и нажмите клавишу ВВОД.

6.  Щелкните правой кнопкой мыши **NoReReg** и выберите команду **изменить**.

7.  В поле **Valuedata** введите **1**и нажмите кнопку **ОК**.

8.  В меню Файл выберите команду **выход** , чтобы закрыть редактор реестра.

## <a href="" id="bkmk-office-integration-win"></a>Интеграция Office с Windows с помощью App-V для развертывания Office


При развертывании Office 2013 с помощью App-V Office полностью интегрируется с операционной системой, которая обеспечивает конечным пользователям те же функции и функциональность, что и в Office, если он развернут без App-V.

Пакет App-V для Office 2013 поддерживает следующие точки интеграции с операционной системой Windows:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Точка расширения</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Плагин присоединения к собранию Lync для Firefox и Chrome</p></td>
<td align="left"><p>Пользователь может присоединиться к собраниям Lync из Firefox и Chrome</p></td>
</tr>
<tr class="even">
<td align="left"><p>Отправлено в драйвер печати OneNote</p></td>
<td align="left"><p>Пользователь может печатать в OneNote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Связанные заметки OneNote</p></td>
<td align="left"><p>Связанные заметки OneNote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Надстройка "отправить в OneNote" в Internet Explorer</p></td>
<td align="left"><p>Пользователь может отправлять сообщения в OneNote из браузера Internet Explorer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Исключение брандмауэра для Lync и Outlook</p></td>
<td align="left"><p>Исключение брандмауэра для Lync и Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Клиент MAPI</p></td>
<td align="left"><p>Встроенные приложения и надстройки могут взаимодействовать с виртуальным приложением Outlook через MAPI</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Надстройка SharePoint для Firefox</p></td>
<td align="left"><p>Пользователь может использовать возможности SharePoint в Firefox</p></td>
</tr>
<tr class="even">
<td align="left"><p>Приложение панели управления "почта"</p></td>
<td align="left"><p>Пользователь получает панель управления "почта" в Outlook</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Основные сборки взаимодействия</p></td>
<td align="left"><p>Поддержка управляемых надстроек</p></td>
</tr>
<tr class="even">
<td align="left"><p>Обработчик кэша документов Office</p></td>
<td align="left"><p>Разрешение кэша документов для приложений Office</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Обработчик поиска протоколов Outlook</p></td>
<td align="left"><p>Пользователь может выполнять поиск в Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Элементы управления ActiveX:</p></td>
<td align="left"><p>Дополнительные сведения об элементах ActiveX можно найти в <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> справочнике API элементов ActiveX </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocument</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. активатор</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Name. NameCtrl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Элемент управления ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Вспомогательное приложение браузера OneDrive Pro</p></td>
<td align="left"><p>Элемент управления ActiveX]</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Наложения значков OneDrive Pro</p></td>
<td align="left"><p>Перекрытие значков оболочки в проводнике Windows при просмотре папок в папках OneDrive Pro</p></td>
</tr>
<tr class="even">
<td align="left"><p>Расширения оболочки</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Горячие</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Search</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





