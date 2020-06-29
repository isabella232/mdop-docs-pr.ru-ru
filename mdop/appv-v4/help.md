---
title: HELP (СПРАВКА)
description: HELP (СПРАВКА)
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821462"
---
# HELP (СПРАВКА)


Отображает сведения о различных командах SFTMIME, которые можно использовать в Application Virtualization (App-V).

## HELP (СПРАВКА)


`SFTMIME [/? | /HELP [VERB:<verb>]]`

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
<td align="left"><p>/?,/HELP</p></td>
<td align="left"><p>Выводит сведения об использовании.</p></td>
</tr>
<tr class="even">
<td align="left"><p>соответствующ</p></td>
<td align="left"><p>Команда, которую необходимо выполнить, например "Добавить", "Обновить", "Справка" или "Удалить".</p></td>
</tr>
<tr class="odd">
<td align="left"><p>объект</p></td>
<td align="left"><p>Назначение команды (например, &quot; приложение Application: по умолчанию).&quot;</p></td>
</tr>
<tr class="even">
<td align="left"><p>параметры</p></td>
<td align="left"><p>Необязательные параметры для заданных команды и объекта.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LOG</p></td>
<td align="left"><p>Вывод журнала на указанный путь.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CONSOLE</p></td>
<td align="left"><p>Выводит результаты в активном окне консоли (по умолчанию).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/GUI</p></td>
<td align="left"><p>Выводит ошибки в диалоговом окне (недопустимый для запросов).</p></td>
</tr>
</tbody>
</table>

 

Для версии 4.6 добавлен следующий параметр.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>/LOGU</p></td>
<td align="left"><p>Если задано значение, выводится имя указанного пути в формате Юникод.</p></td>
</tr>
</tbody>
</table>

 

Поддерживаются команды, описанные в приведенной ниже таблице.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>ADD</p></td>
<td align="left"><p>Добавляет новое приложение, пакет, сопоставление типов файлов или сервер публикаций в клиент App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>СТРОИЛ</p></td>
<td align="left"><p>Изменение конфигурации приложения, пакета, сопоставления типа файла или сервера публикаций.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DELETE</p></td>
<td align="left"><p>Удаляет приложения, пакеты, сопоставления типов файлов или серверы.</p></td>
</tr>
<tr class="even">
<td align="left"><p>ЗАГРУЗИТЬ</p></td>
<td align="left"><p>Загружает пакет в кэш файловой системы.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ЧИНИТ</p></td>
<td align="left"><p>Сброс личных параметров для приложения.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Обновлен</p></td>
<td align="left"><p>Запускает обновление сервера публикаций.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ПУБЛИКОВАТЬ</p></td>
<td align="left"><p>Публикует ярлык приложения в меню "Пуск", рабочем столе или другом указанном месте, а также может использоваться для публикации контента всего пакета.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Отмена публикации</p></td>
<td align="left"><p>Удаление ярлыков и типов файлов для всего пакета.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ЗАПРОСА</p></td>
<td align="left"><p>Получает текущий список приложений, пакетов, сопоставлений типов файлов или серверов публикаций.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Сброс</p></td>
<td align="left"><p>Удаление личных настроек и настольных конфигураций для одного или нескольких приложений.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ГРУЖАТЬ</p></td>
<td align="left"><p>Выгрузка пакета из кэша файловой системы.</p></td>
</tr>
<tr class="even">
<td align="left"><p>БЛОКИРОВКИ</p></td>
<td align="left"><p>Блокирует приложение, указанное в кэше файловой системы.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Креп</p></td>
<td align="left"><p>Разблокирует приложение, указанное в кэше файловой системы.</p></td>
</tr>
</tbody>
</table>

 

Для получения дополнительных сведений об описанных выше действиях используйте следующую команду:

`SFTMIME /HELP VERB:verb`

Например, следующая команда выведет сведения о команде ADD:

`SFTMIME /HELP VERB:ADD`

## Статьи по теме


[Справочник по командам SFTMIME](sftmime--command-reference.md)

 

 





