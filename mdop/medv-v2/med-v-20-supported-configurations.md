---
title: Поддерживаемые конфигурации MED-V 2.0
description: Поддерживаемые конфигурации MED-V 2.0
author: dansimp
ms.assetid: 88f1d232-aa01-45ab-8da7-d086269250b5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0fed090ec04cf67a32b13533f4003c01ae167493
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825219"
---
# Поддерживаемые конфигурации MED-V 2.0


Ваша среда может уже соответствовать требованиям к конфигурации, указанным здесь, чтобы можно было установить и запустить виртуализацию классической версии Microsoft Enterprise (MED-V) 2,0. Мы включили требования, включая операционную систему узла, место на диске и требования к рабочей области MED-V.

## Требования к ведущему компьютеру для MED-V 2.0


### Требования к операционной системе для узла MED-V 2,0

В таблице ниже перечислены операционные системы, которые поддерживаются установкой MED-V 2,0 на главном компьютере.

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
<td align="left"><p>Windows7</p></td>
<td align="left"><p>Профессиональная, Корпоративная или максимальная</p></td>
<td align="left"><p>Нет или пакет обновления 1 (SP1)</p></td>
<td align="left"><p>x86 или x64</p></td>
</tr>
</tbody>
</table>

 

В таблице ниже приведен минимальный объем ОЗУ, необходимый для каждой операционной системы, поддерживаемой в MED-V 2,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Операционная система</th>
<th align="left">Минимальный требуемый объем ОЗУ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7 x86</p></td>
<td align="left"><p>ПРЕВЫШАТЬ</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7 x64</p></td>
<td align="left"><p>ПРЕВЫШАТЬ</p></td>
</tr>
</tbody>
</table>

 

### Минимальный рекомендуемый объем дискового пространства

Мы рекомендуем использовать не менее 10 ГБ свободного места на устройстве. Тем не менее необходимое место на диске сильно зависит от количества приложений, опубликованных в рабочей области MED-V.

### <a href="" id="med-v-2-0-host-configuration-"></a>Конфигурация узла MED-V 2.0

**Версия .NET Framework**

Версия .NET Framework 3.5 с пакетом обновления 1 (SP1) для Microsoft .NET Framework является обязательной для MED-V 2,0. Однако вы можете установить платформу .NET Framework 4 или более поздней версии, если платформа .NET Framework 3,5 уже установлена.

**Модуль виртуализации**

Windows Virtual PCwith. исправление, описанное в статье Microsoft Knowledge Base 977206, поддерживается для MED-V 2,0.

**Интернет-браузер**

Windows Internet Explorer8 и Windows Internet Explorer 9 поддерживаются для MED-V 2,0.

**Среды Microsoft Server**

Агент узла MED-V и диспетчер рабочих областей MED-V не поддерживаются в какой-либо среде сервера.

## Требования к рабочей области для MED-V 2.0


### Требования к операционной системе для рабочей области MED-V 2,0

В таблице ниже перечислены операционные системы, поддерживаемые в рабочих областях для MED-V 2,0.

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
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Профессиональный выпуск</p></td>
<td align="left"><p>ОБНОВЛЕНИЙ</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="med-v-2-0-workspace-configuration-"></a>Настройка рабочей области для MED-V 2.0

**Версия .NET Framework**

Только версия .NET Framework 3.5 SP1 для Microsoft .NET Framework поддерживается для установки в рабочей области MED-V 2,0.

**Интернет-браузер**

Windows Internet Explorer6, Windows Internet Explorer7, Windows Internet Explorer8 и Windows Internet Explorer9 поддерживаются для установки рабочей области MED-V 2,0.

### Создание рабочей области для MED-V 2,0

Виртуальный жесткий диск, который использовался для создания пакета рабочей области для MED-V 2,0, должен быть создан с помощью Virtual PC для Windows.

## Сведения о глобализации для MED-V 2,0


### Сведения об глобализации агента узла MED-V 2,0

Для агента хостов MED-V 2,0 поддерживаются следующие языковые версии операционной системы Windows:

-   Французский

-   Итальянский

-   Немецкий

-   Испанский

-   Корейский

-   Японский

-   Португальский (Бразилия)

-   Русский

-   Китайский (традиционное письмо)

-   Китайский (упрощенное письмо)

-   Нидерландский

-   Шведский

-   Датский

-   Финский

-   Португальский

-   Норвежский

-   Польский

-   Турецкий

-   Венгерский

-   Чешский

-   Греческий

-   Словацкий

-   Словенский

### Сведения об глобализации диспетчера рабочих областей MED-V 2,0

Для диспетчера рабочих областей MED-V 2,0 поддерживаются следующие языковые версии операционной системы Windows:

-   Французский

-   Итальянский

-   Немецкий

-   Испанский

-   Корейский

-   Японский

-   Португальский (Бразилия)

-   Русский

-   Китайский (традиционное письмо)

-   Китайский (упрощенное письмо)

## Статьи по теме


[Развертывание MED-V](deployment-of-med-v.md)

 

 





