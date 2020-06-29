---
title: Класс WMI пакета App-V
description: Класс WMI пакета App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819799"
---
# Класс WMI пакета App-V


В клиенте Application Virtualization (App-V) класс **Package** является классом инструментария управления Windows (WMI), который представляет все виртуальные пакеты на клиенте. Виртуальные пакеты могут содержать множество виртуальных приложений.

## Синтаксис


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## Свойства


<a href="" id="name"></a>**Имя**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Понятное имя виртуального пакета.

<a href="" id="version"></a>**Версия**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Версия виртуального пакета.

<a href="" id="packageguid"></a>**PackageGUID**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: Key

Идентификатор GUID конфигурации пакета и исходных файлов.

<a href="" id="sftpath"></a>**SftPath**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Путь к файлу SFT.

<a href="" id="totalsize"></a>**TotalSize**  
Тип данных: **UInt64**

Тип доступа "только для чтения"

Квалификаторы: None

Общий размер виртуального пакета (в килобайтах).

<a href="" id="cachedsize"></a>**CachedSize**  
Тип данных: **UInt64**

Тип доступа "только для чтения"

Квалификаторы: None

Общий размер кэша для виртуального пакета (в килобайтах).

<a href="" id="launchsize"></a>**LaunchSize**  
Тип данных: **UInt64**

Тип доступа "только для чтения"

Квалификаторы: None

Общий размер основного блока компонентов виртуального пакета в килобайтах.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
Тип данных: **UInt64**

Тип доступа "только для чтения"

Квалификаторы: None

Общий размер основного блока функций виртуального пакета, который был кэширован (в килобайтах).

<a href="" id="inuse"></a>**InUse**  
Тип данных: **логический**

Тип доступа "только для чтения"

Квалификаторы: None

**значение true** , если любое виртуальное приложение в виртуальном пакете запущено; в противном случае — **значение false**.

<a href="" id="locked"></a>**Заблокировано**  
Тип данных: **логический**

Тип доступа "только для чтения"

Квалификаторы: None

**значение true** , если виртуальный пакет заблокирован; в противном случае — **значение false**.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
Тип данных: **UInt16**

Тип доступа "только для чтения"

Квалификаторы: None

Процент файлов кэша. В соответствии с приведенной ниже формулой: CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**VersionGUID**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Идентификатор GUID версии пакета.

 

 





