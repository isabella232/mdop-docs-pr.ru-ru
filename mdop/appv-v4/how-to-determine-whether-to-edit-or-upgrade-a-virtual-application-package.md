---
title: Определение необходимости изменения или обновления пакета виртуального приложения
description: Определение необходимости изменения или обновления пакета виртуального приложения
author: dansimp
ms.assetid: 33dd5332-6802-46e0-9748-43fcc8f80aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b256a4927231613b6f2e688b5951adf57c9cb89a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817502"
---
# Определение необходимости изменения или обновления пакета виртуального приложения


Используйте следующую таблицу, чтобы определить, можно ли открыть виртуальный пакет приложения для редактирования, нужно ли создавать новую версию пакета, или один из доступных вариантов — с помощью секвенсора App-V.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Действие</th>
<th align="left">Открыть для редактирования</th>
<th align="left">Открыть для обновления</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Просмотр свойств пакета.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Просмотр журнала изменений в пакете.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Просмотр связанных файлов пакетов.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Редактирование параметров реестра.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ознакомьтесь с дополнительными параметрами пакета (кроме свойств файла операционной системы).</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Создание связанного установщика Windows (MSI).</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Изменить OSD файл.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Сжатие и распаковка пакета.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Добавление сопоставлений типов файлов.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Переименование сочетаний клавиш.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Задает состояние виртуальной клавиши в реестре (переопределение/слияние).</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Настройте состояние виртуализированной папки.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Изменение сопоставлений виртуальной файловой системы.</p></td>
<td align="left"><p>Да</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ознакомьтесь со всеми свойствами файлов операционной системы, связанными с пакетом.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Добавление дополнительных служб.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Добавление дополнительных файлов.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Соберите и настройте соответствующие дескрипторы безопасности.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Примените обновления для системы безопасности или обновите ее до новой версии.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Добавьте дополнительное приложение.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="even">
<td align="left"><p>Примените обновления, для которых требуется открыть приложение.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Примените обновления, требующие перезагрузки компьютера.</p></td>
<td align="left"><p>Нет</p></td>
<td align="left"><p>Да</p></td>
</tr>
</tbody>
</table>

 

## Связанные разделы


[Изменение существующего виртуального приложения](how-to-edit-an-existing-virtual-application.md)

[Обновление существующего виртуального приложения](how-to-upgrade-an-existing-virtual-application.md)

 

 





