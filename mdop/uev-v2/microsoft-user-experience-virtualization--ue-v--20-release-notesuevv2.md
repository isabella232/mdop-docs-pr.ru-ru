---
title: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0
description: Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825282"
---
# Заметки о выпуске для Microsoft User Experience Virtualization (UE-V) 2.0


Чтобы выполнить поиск в заметках о выпуске Microsoft User Experience Virtualization (UE-V) 2,0, нажмите клавиши CTRL + F.

Перед установкой UE-V вы должны внимательно прочитать эти заметки о выпуске. Заметки о выпуске содержат сведения, необходимые для успешной установки виртуализации взаимодействия с пользователем, и содержат дополнительные сведения, недоступные в документации по продукту. Если между этими заметками о выпуске и другой документацией UE-V есть различия, Последнее изменение должно считаться полномочным. Эти заметки о выпуске заменяют содержимое, которое входит в состав этого продукта.

## Предоставление отзыва


Расскажите нам, что вы думаете о нашей документации для MDOP, предоставив нам свой отзыв и комментарии. Отправьте отзыв о документации в [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Известные проблемы UE-V


В этом разделе содержатся заметки о выпуске для виртуализации взаимодействия с пользователем.

### Параметры реестра не синхронизируются между приложением App-V и приложениями машинного кода на одном компьютере

Если на компьютере установлено приложение, установленное как с помощью Application Virtualization (App-V), так и локально с помощью установщика Windows (MSI-файла), параметры, основанные на реестре, не синхронизируются между этими технологиями.

**Временное решение:** Чтобы устранить эту проблему, запустите приложение, выбрав одну из двух технологий, но не то, и другое.

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a>Параметры не синхронизируются, если сетевая доля выходит за пределы домена пользователя

Если Windows® 8 попытается синхронизировать параметры операционной системы, синхронизация завершается сбоем со следующим сообщением об ошибке: **"Boost:: FileSystem:: EXISTS": неверное имя пользователя или пароль**. Эта ошибка может указывать на то, что сетевой общий доступ находится за пределами домена пользователя или домена с отношением доверия с этим доменом. Чтобы проверить работоспособность журнала событий, откройте **средство просмотра событий** и перейдите в раздел " **приложения и службы**", которые регистрируются в журнале  /  **Microsoft**  /  **виртуализации Microsoft User Experience**  /  **Logging**  /  **Operational**. Общие сетевые ресурсы, используемые для расположений хранилищ параметров UE-V, должны располагаться в том же домене Active Directory, что и пользователь, либо доверенный домен домена пользователя.

**Временное решение:** Используйте общие сетевые ресурсы из того же домена Active Directory, что и пользователь.

### Непредсказуемые результаты с установленными приложениями Office 2010 и Office 2013

Если у пользователя установлен и Office 2010, и Office 2013, все общие параметры, которые поддерживаются двумя версиями Office, перемещаются UE-V. Это может привести к тому, что размер пакета Office 2010 станет довольно большим или привести к непредсказуемым конфликтам с 2013, особенно если используется Office 365.

**Временное решение:** Установка только одной версии Office или ограничение параметров синхронизации UE-V.

### Удаление и повторная установка приложения для Windows 8 восстанавливает исходное состояние параметров

При использовании синхронизации параметров UE-V для приложения Windows 8, если пользователь удаляет приложение, а затем переустанавливает приложение, параметры приложения возвращаются к значениям по умолчанию.Это происходит из-за того, что при удалении удаляется локальная (кэшированная) копия параметров приложения, но не удаляется локальный пакет параметров UE-V.После повторной установки и запуска приложения UE-V собирает параметры приложения, которые были восстановлены в приложении по умолчанию, а затем загружают параметры по умолчанию в центральное место хранения.Другие компьютеры, на которых запущено приложение, затем скачайте параметры по умолчанию.Такое поведение аналогично поведению классических приложений.

**Временное решение:** Ничего.

### Перемещение подписей электронной почты в Outlook 2010

UE-V перемещает файлы подписей Outlook 2010 между устройствами. Однако параметры подписи по умолчанию для новых сообщений, ответов и пересылаемых писем не синхронизируются. Эти два параметра хранятся в профиле Outlook, который UE-V не перемещается.

**Временное решение:** Ничего.

### UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Microsoft Office

Рекомендуем установить 64-разрядную версию Microsoft Office для современных компьютеров. Чтобы узнать, какая версия вам нужна, [щелкните здесь](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions). UE-V поддерживает перемещаемые параметры между идентичными версиями Office. Например, 32-разрядные параметры Office будут перемещаться между всеми 32-разрядными экземплярами Office. UE-V не поддерживает перемещаемые параметры между 32-битным и 64-разрядными версиями Office.

**Временное решение:** Ничего

### <a href="" id="msi-s-are-not-localized"></a>MSI не локализованы

UE-V 2,0 включает локализованную программу установки для агента UE-V и генератора UE-V. Эти файлы MSI по-прежнему доступны, но пользовательский интерфейс минимизирован и отображается только на английском языке. Несмотря на то, что файл находится на английском языке, во время установки программа установки устанавливает все поддерживаемые языки.

**Временное решение:** Ничего

### Favicons, связанные с браузером Internet Explorer 9, не перемещаются

Favicons, связанные с браузером Internet Explorer 9, не перемещаются с помощью виртуализации взаимодействия с пользователем и не отображаются при первом появлении этого списка на новом компьютере.

**Временное решение:** После использования закладки и кэширования в браузере Internet Explorer 9 будет выводиться Favicons с соответствующими избранными.

### Пути к параметрам файла хранятся в реестре

Некоторые параметры приложения хранят пути файлов конфигурации и параметров в виде значений в реестре. Файлы, на которые указывают ссылки в реестре, должны быть синхронизированы при перемещении параметров между компьютерами.

**Временное решение:** С помощью перенаправления папок или других технологий убедитесь, что файлы, на которые указывают ссылки, указаны в одном и том же месте на всех компьютерах, где параметры перемещаются.

### Путь к хранилищу с длинными параметрами может вызвать ошибку

Храните пути к хранилищу параметров как можно короче. Длинные пути могут не допускать разрешения и синхронизацию. UE-V использует путь к хранилищу параметров как часть расчетного пути для хранения параметров. Этот путь вычисляется следующим образом: параметры путь к хранилищу и "settingspackages" + Dir (ИД шаблона) + имя пакета (идентификатор шаблона) +. pkgx. Если размер вычисляемого пути превышает 260 символов, в журнале событий UE-V память пакета завершается сбоем и генерируется следующее сообщение об ошибке:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Для проверки событий журнала в журнале откройте средство просмотра событий и перейдите в раздел Журналы приложений и служб/Microsoft/пользовательский интерфейс, виртуализация и ведение журнала.

**Временное решение:** Ничего.

### Некоторые параметры операционной системы перемещаются только в том случае, если они есть в версиях операционной системы

Параметры операционной системы для символов экранного диктора и денежных единиц, относящихся к национальной настройке (например, язык и региональные стандарты), будут перемещаться только в версиях операционной системы Windows. Например, символы денежных единиц не будут перемещаться между Windows 7 и Windows 8.

**Временное решение:** Ничего

### Приложения для Windows 8 не синхронизируют параметры после того, как приложение перезапускается после неожиданного закрытия

Если приложение Windows 8 неожиданно закрывается после запуска, параметры приложения могут быть не синхронизированы при перезапуске приложения.

**Временное решение:** Закройте приложение для Windows 8, закройте и перезапустите приложение UevAppMonitor.exe (может использовать TaskManager), а затем перезапустите приложение Windows 8.

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>Агент UE-V 1 вызывает ошибки при запуске шаблонов UE-V 2

Если шаблон расположений параметров UE-V 2 распространяется на компьютер, установленный с агентом UE-V 1, некоторые параметры не синхронизируются между компьютерами, и агент сообщает об ошибках в журнале событий.

**Временное решение:** При переходе с UE-V 1 на UE-V 2 и, возможно, у вас есть компьютеры, на которых работает Предыдущая версия агента, создайте отдельный каталог UE-V 2,0 для поддержки агента и шаблонов UE-v 2,0.

## Исправления и статьи базы знаний для UE-V 2,0


В этом разделе содержатся исправления и статьи базы знаний для UE-V 2,0.

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
<td align="left"><p>2927019</p></td>
<td align="left"><p>Пакет исправлений 1 для Microsoft User Experience Virtualization 2,0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)">support.microsoft.com/kb/2927019</a></p></td>
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
<td align="left"><p>2930271</p></td>
<td align="left"><p>Общие сведения об ограничениях для перемещаемых подписей Outlook в Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)">support.microsoft.com/kb/2930271/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Восстановление поврежденной установки UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2850989</p></td>
<td align="left"><p>Миграция профилей MAPI с помощью Microsoft UE-V не поддерживается</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V перемещение пустых папок и разделов реестра</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Как включить ведение журнала отладки в Microsoft User Experience Virtualization (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V не обновляет тему в сеансах RDS и VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2901856</p></td>
<td align="left"><p>Параметры приложения не синхронизируются после принудительной перезагрузки на компьютере с поддержкой UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)">support.microsoft.com/kb/2901856/EN-US</a></p></td>
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

 

 

 





