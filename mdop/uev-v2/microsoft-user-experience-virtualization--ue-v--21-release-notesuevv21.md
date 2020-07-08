---
title: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1
description: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1
author: dansimp
ms.assetid: 79a36c77-fa0c-4651-8028-4a79763a2fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0677dda93f2c2dc60ec627ae0c3f4bd8c199db6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825279"
---
# Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.1


Чтобы выполнить поиск в заметках о выпуске Microsoft User Experience Virtualization (UE-V) 2,0, нажмите клавиши CTRL + F.

Перед установкой UE-V вы должны внимательно прочитать эти заметки о выпуске. Заметки о выпуске содержат сведения, необходимые для успешной установки виртуализации взаимодействия с пользователем, и содержат дополнительные сведения, недоступные в документации по продукту. Если между этими заметками о выпуске и другой документацией UE-V есть различия, Последнее изменение должно считаться полномочным. Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.

## Предоставление отзыва


Расскажите нам, что вы думаете о нашей документации для MDOP, предоставив нам свой отзыв и комментарии. Отправьте отзыв о документации в [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Известные проблемы UE-V


В этом разделе содержатся заметки о выпуске для виртуализации взаимодействия с пользователем.

### Шаблоны расположения параметров UE-V для Skype приводят к сбою в работе Skype

Если пользователь создает допустимый шаблон расположения параметров для классического приложения Skype, регистрирует его, а затем запускает классическое приложение Skype, и Skype завершает работу со сбоем. ACCESS \ _VIOLATION записывается в журнал событий приложений.

ВРЕМЕННОе решение: удаление и Отмена регистрации шаблона Skype для обеспечения повторной работы Skype.

### Возможны ошибки в существующих сценариях для автоматической установки UE-V

Два изменения, внесенные в установщик UE-V, могут привести к сбою в сценариях установки UE-v, которые приводят к неудачной установке сценариев, которые работали с более ранними версиями UE-v 2,1. Первый является новым требованием, согласно которому пользователи должны принять условия лицензионного соглашения и принять или отклонить участие в программе улучшения качества программного обеспечения (CEIP), даже при автоматической установке. Использование параметра/q больше не подходит для указания принятия условий лицензии и соглашения для участия в программе улучшения качества программного обеспечения.

Во-вторых, установщик теперь принудительно перезапускает компьютер после установки UE-V Agent. Это может привести к сбою сценария установки, если он не ожидается перезапуском (например, он сначала устанавливает агент UE-V Agent, а затем немедленно устанавливает генератор).

ВРЕМЕННОе решение: в установщике UE-V (MSI) есть два новых параметра командной строки, поддерживающих автоматическое установка.

<table>
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
<td align="left"><p><strong>/ACCEPTLICENSETERMS = true</strong></p></td>
<td align="left"><p>Установите для этого параметра <strong> значение истина </strong> , чтобы автоматически установить UE-V. Добавление этого параметра означает, что пользователь принимает условия лицензии UE-V (по умолчанию):%ProgramFiles%\Microsoft User Experience Virtualization\Agent</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/NORESTART</strong></p></td>
<td align="left"><p>Этот параметр предотвращает обязательную перезагрузку после установки агента UE-V. Код возврата 3010 указывает на то, что требуется перезагрузка перед использованием UE-V.</p></td>
</tr>
</tbody>
</table>

 

### Параметры реестра не синхронизируются между приложением App-V и приложениями машинного кода на одном компьютере

Если на компьютере установлено приложение, установленное как с помощью Application Virtualization (App-V), так и локально с помощью установщика Windows (MSI-файла), параметры, основанные на реестре, не синхронизируются между этими технологиями.

ВРЕМЕННОе решение: чтобы устранить эту проблему, запустите приложение, выбрав одну из двух технологий, но не то, и другое.

### Непредсказуемые результаты с установленными приложениями Office 2010 и Office 2013

Если у пользователя установлен и Office 2010, и Office 2013, все общие параметры, которые поддерживаются двумя версиями Office, перемещаются UE-V. Это может привести к тому, что размер пакета Office 2010 станет довольно большим или привести к непредсказуемым конфликтам с 2013, особенно если используется Office 365.

ВРЕМЕННОе решение: Установите только одну версию Office или ограничьте параметры, синхронизируемые агентом UE-V.

### Удаление и повторная установка приложения для Windows 8 восстанавливает исходное состояние параметров

При использовании синхронизации параметров UE-V для приложения Windows 8, если пользователь удаляет приложение, а затем переустанавливает приложение, параметры приложения возвращаются к значениям по умолчанию.Это происходит из-за того, что при удалении удаляется локальная (кэшированная) копия параметров приложения, но не удаляется локальный пакет параметров UE-V.После повторной установки и запуска приложения UE-V собирает параметры приложения, которые были восстановлены в приложении по умолчанию, а затем загружают параметры по умолчанию в центральное место хранения.Другие компьютеры, на которых запущено приложение, затем скачайте параметры по умолчанию.Такое поведение аналогично поведению классических приложений.

ВРЕМЕННОе решение: нет.

### UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Microsoft Office

Мы рекомендуем установить 32-разрядную версию Microsoft Office для 32-и 64-разрядных операционных систем. Чтобы выбрать нужную вам версию Microsoft Office, щелкните здесь. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V поддерживает перемещаемые параметры между идентичными версиями Office. Например, 32-разрядные параметры Office будут перемещаться между всеми 32-разрядными экземплярами Office. UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Office.

ВРЕМЕННОе решение: нет

### <a href="" id="msi-s-are-not-localized"></a>MSI не локализованы

UE-V 2,0 включает локализованную программу установки для агента UE-V и генератора UE-V. Эти файлы MSI по-прежнему доступны, но пользовательский интерфейс минимизирован и отображается только на английском языке. Несмотря на то, что файл находится на английском языке, во время установки программа установки устанавливает все поддерживаемые языки.

ВРЕМЕННОе решение: нет

### Favicons, связанные с браузером Internet Explorer 9, не перемещаются

Favicons, связанные с браузером Internet Explorer 9, не перемещаются с помощью виртуализации взаимодействия с пользователем и не отображаются при первом появлении этого списка на новом компьютере.

ВРЕМЕННОе решение: при использовании закладки и кэшировании в браузере Internet Explorer 9 появится Favicons с соответствующими избранными.

### Пути к параметрам файла хранятся в реестре

Некоторые параметры приложения хранят пути файлов конфигурации и параметров в виде значений в реестре. Файлы, на которые указывают ссылки в реестре, должны быть синхронизированы при перемещении параметров между компьютерами.

ВРЕМЕННОе решение: используйте перенаправление папок или другие технологии, чтобы убедиться в том, что файлы, на которые указывают ссылки, находятся в том же расположении на всех компьютерах, где параметры перемещаются.

### Путь к хранилищу с длинными параметрами может вызвать ошибку

Храните пути к хранилищу параметров как можно короче. Длинные пути могут не допускать разрешения и синхронизацию. UE-V использует путь к хранилищу параметров как часть расчетного пути для хранения параметров. Этот путь вычисляется следующим образом: параметры путь к хранилищу и "settingspackages" + Dir (ИД шаблона) + имя пакета (идентификатор шаблона) +. pkgx. Если размер вычисляемого пути превышает 260 символов, в журнале событий UE-V память пакета завершается сбоем и генерируется следующее сообщение об ошибке:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Для проверки событий журнала в журнале откройте средство просмотра событий и перейдите в раздел Журналы приложений и служб/Microsoft/пользовательский интерфейс, виртуализация и ведение журнала.

ВРЕМЕННОе решение: нет.

### Некоторые параметры операционной системы перемещаются только в том случае, если они есть в версиях операционной системы

Параметры операционной системы для символов экранного диктора и денежных единиц, относящихся к национальной настройке (например, язык и региональные стандарты), будут перемещаться только в версиях операционной системы Windows. Например, символы денежных единиц не будут перемещаться между Windows 7 и Windows 8.

ВРЕМЕННОе решение: нет

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>Агент UE-V 1 вызывает ошибки при запуске шаблонов UE-V 2

Если шаблон расположений параметров UE-V 2 распространяется на компьютер, установленный с агентом UE-V 1, некоторые параметры не синхронизируются между компьютерами, и агент сообщает об ошибках в журнале событий.

РЕШЕНИЕ: при переходе с UE-V 1 на UE-V 2 и, возможно, у вас есть компьютеры, на которых работает Предыдущая версия агента, создайте отдельный каталог UE-V 2,0 для поддержки агента и шаблонов UE-v 2,0.

## Исправления и статьи базы знаний для UE-V 2,1


В этом разделе содержатся исправления и статьи базы знаний для UE-V 2,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Статья базы знаний</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Ссылка</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>3018608</p></td>
<td align="left"><p>UE-V 2,1-TemplateConsole.exe завершает работу со сбоем, если отсутствуют классы WMI UE-V.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)">support.microsoft.com/kb/3018608/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2903501</p></td>
<td align="left"><p>UE-V: совместимость с интерфейсом пользователя (UE-V) Compatibility с профилями пользователей</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)">support.microsoft.com/kb/2903501/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2770042</p></td>
<td align="left"><p>Параметры реестра UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)">support.microsoft.com/kb/2770042/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2847017</p></td>
<td align="left"><p>Параметры UE-V реплицированы с помощью Internet Explorer</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)">support.microsoft.com/kb/2847017/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Восстановление поврежденной установки UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850989</p></td>
<td align="left"><p>Миграция профилей MAPI с помощью Microsoft UE-V не поддерживается</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V перемещение пустых папок и разделов реестра</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Как включить ведение журнала отладки в Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V не обновляет тему в сеансах RDS и VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850582</p></td>
<td align="left"><p>Использование виртуализации взаимодействия с пользователем Microsoft в приложениях App-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)">support.microsoft.com/kb/2850582/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3041879</p></td>
<td align="left"><p>Текущие версии файлов для Microsoft User Experience Virtualization</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)">support.microsoft.com/kb/3041879/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2843592</p></td>
<td align="left"><p>Сведения о виртуализации взаимодействия с пользователем и о высокой доступности</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)">support.microsoft.com/kb/2843592/EN-US</a></p></td>
</tr>
</tbody>
</table>

 






 

 





