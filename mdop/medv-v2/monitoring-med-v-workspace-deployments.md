---
title: Мониторинг развертывания рабочей области MED-V
description: Мониторинг развертывания рабочей области MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827212"
---
# Мониторинг развертывания рабочей области MED-V


Функция мониторинга в Microsoft Enterprise Virtualization (MED-V) 2,0 позволяет выполнять запросы для отдельных рабочих областей MED-V, чтобы определить, будет ли первоначально выполнена настройка после развертывания рабочих областей MED-V. Наблюдение за успехом первого этапа настройки имеет большое значение, так как MED-V не находится в пригодном для использования состоянии до тех пор, пока не будет выполнена установка первого раза.

В этом разделе содержатся сведения и инструкции, которые помогут вам отслеживать успешность или сбой при первом запуске программы.

## Наблюдение за развертыванием рабочих областей MED-V


Функция мониторинга состоит из отдельного внутрипроцессного поставщика инструментария управления Windows (WMI), который можно запросить с помощью языка запросов WMI, чтобы выяснить состояние первой настройки для всех конечных пользователей в рабочей области MED-V.

Поставщик WMI реализуется с помощью инфраструктуры расширения поставщика WMI из Microsoft .NET Framework 3,5. Поставщик WMI выполняется в контексте локальной службы и сохраняет состояние установки в первый раз в \\ProgramData.

Поставщик WMI реализован в пространстве имен **root\\microsoft\\medv** и реализует класс **FTS \ _Status**, который предоставляет метод **SetFtsState**. MED-V использует **SetFtsState** для установки первого состояния установки.

Класс включает следующие свойства.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Свойство</th>
<th align="left">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Компьютер</strong></p></td>
<td align="left"><p><strong>Свойство только </strong> для чтения, содержащее имя гостевой виртуальной машины, подготовленное при первом запуске программы установки. Этот ключ содержит имя, которое гость имел при первой ошибке установки.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>StatusCode</strong></p></td>
<td align="left"><p><strong>Свойство только </strong> для чтения, которое имеет значение 0, если при первом запуске программы установки была выполнена успешно. Любые другие возвращенные значения равны ИДЕНТИФИКАТОРу события, в котором регистрируется ошибка.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Время</strong></p></td>
<td align="left"><p>Время в формате UTC, когда программа установки завершила свое первое время.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Пользователь</strong></p></td>
<td align="left"><p>Пользователь, для которого при первом запуске программы установки произошла ошибка.</p></td>
</tr>
</tbody>
</table>

 

В следующем коде показан MOF-файл, который определяет класс **FTS \ _Status** .

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

Поскольку основная проблема чаще всего связана с рабочими областями для MED-V, для которых не удалось выполнить начальную настройку, вы можете написать запрос, возвращающий только те из них, которые не выполнялись при первом запуске программы, например:

``` syntax
Select * from FTS_Status where StatusCode != 0
```

В этом случае функция мониторинга возвращает список таких рабочих областей MED-V, для которых не удалось выполнить начальную настройку, с помощью которых можно выполнить необходимые действия для устранения проблемы.

## Статьи по теме


[Мониторинг рабочих областей MED-V](monitor-med-v-workspaces.md)

[Проверка параметров первой установки](how-to-verify-first-time-setup-settings.md)

 

 





