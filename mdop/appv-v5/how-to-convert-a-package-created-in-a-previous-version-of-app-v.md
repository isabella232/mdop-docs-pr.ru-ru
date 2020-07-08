---
title: Преобразование пакета, созданного в предыдущей версии App-V
description: Преобразование пакета, созданного в предыдущей версии App-V
author: dansimp
ms.assetid: b092a5f8-cc5f-4df8-a5a2-0a68fd7bd5b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bd0d5db7cb406a5a7fe67c69ff77461cce2b0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814360"
---
# Преобразование пакета, созданного в предыдущей версии App-V


С помощью служебной программы преобразователя пакетов можно обновлять пакеты виртуальных приложений, созданные в предыдущих версиях приложения App-V.

**Примечание.**  
Если на компьютере установлена архитектура 64-bit, необходимо использовать версию x86 оболочки PowerShell.



Конвертер пакетов может напрямую преобразовывать пакеты, созданные с помощью секвенсора App-V 4,5 или последующих версий. Пакеты, созданные с помощью более ранней версии App-V 4,5, должны быть обновлены до формата App-V 4,5 или App-V 4,6 перед преобразованием.

Ниже приведены сведения о том, как преобразовать существующие пакеты виртуальных приложений.

**Важно.**  
Необходимо настроить преобразователь пакетов, чтобы всегда сохранять файл ингредиентов пакета в безопасном месте и каталоге. Безопасное расположение доступно только администратору. Кроме того, при развертывании пакета необходимо сохранить пакет в безопасном расположении или убедиться в том, что во время преобразования никто из пользователей не может войти в систему.



**Начало работы**

1.  Установите секвенсор App-V на компьютер в среде. Сведения о том, как установить секвенсор, приведены в разделе [Установка секвенсора](how-to-install-the-sequencer-beta-gb18030.md).

2. Импорт требуемого модуля PowerShell

```powershell
Import-Module AppVPkgConverter
```

3. Доступны следующие командлеты:

   -   Test-AppvLegacyPackage — этот командлет предназначен для проверки пакетов. Она будет возвращать сведения о сбоях в пакете, таких как отсутствующие **SFT** — файлы, недопустимые ошибки источника, **OSD** или неправильная версия пакета. Этот командлет не будет анализировать **SFT** – файл или выполнять какие – либо проверки глубины. Чтобы получить сведения о параметрах и основных функциональных возможностях для этого командлета, используйте PowerShell cmdline: Type `Test-AppvLegacyPackage -?` .

   -   ConvertFrom-AppvLegacyPackage – чтобы преобразовать существующий пакет, введите `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` . В этой команде — это `c:\contentStore` расположение существующего пакета и `c:\convertedPackages` Каталог вывода, в который будет сохранен конечный файл виртуального приложения App-V 5,0. По умолчанию, если не указать новое имя, для имени файла App-V 5,0 будет использоваться старое имя пакета.

       Кроме того, преобразователь пакетов оптимизирует производительность пакетов в App-V 5,0, настроив пакет на потоковую ошибку пакета App-V.  Это более производительно, чем основной блок функций и полностью загружаемый пакет. Флаг **DownloadFullPackageOnFirstLaunch** позволяет преобразовать пакет и установить его полностью по умолчанию.

       **Примечание.**  
       Перед указанием выходного каталога необходимо создать выходной каталог.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.0 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)









