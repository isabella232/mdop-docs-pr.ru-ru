---
title: Класс WMI приложения App-V
description: Класс WMI приложения App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822322"
---
# Класс WMI приложения App-V


В клиенте Application Virtualization (App-V) класс **Application** является классом инструментария управления Windows (WMI), который представляет все виртуальные приложения на клиенте.

Следующий синтаксис упрощен из кода MOF (Managed Object Format). Код включает все унаследованные свойства.

## Синтаксис


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## Требования


## Свойства


<a href="" id="name"></a>**Имя**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: Key

Отображаемое имя виртуального приложения.

<a href="" id="version"></a>**Версия**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: Key

Версия виртуального приложения.

<a href="" id="packageguid"></a>**PackageGUID**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Идентификатор GUID пакета, с которым связано виртуальное приложение.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
Тип данных: **Дата и время**

Тип доступа "только для чтения"

Квалификаторы: None

Дата и время последнего запуска виртуального приложения.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
Тип данных: **UInt32**

Тип доступа "только для чтения"

Квалификаторы: None

Количество работающих экземпляров виртуального приложения, которые были запущены напрямую.

<a href="" id="loading"></a>**Загрузка**  
Тип данных: **логический**

Тип доступа "только для чтения"

Квалификаторы: None

**значение true** , если виртуальное приложение запускается; в противном случае — **значение false**.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Исходный путь файла OSD, зарегистрированного в клиенте App-V.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
Тип данных: **строка**

Тип доступа "только для чтения"

Квалификаторы: None

Путь к файлу OSD, если клиент App-V кэширует файл OSD локально.

 

 





