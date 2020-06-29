---
title: Настройка дополнительных параметров с помощью Windows PowerShell
description: Настройка дополнительных параметров с помощью Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827392"
---
# Настройка дополнительных параметров с помощью Windows PowerShell


Созданный пакет рабочей области для MED-V включает в себя файл сценария Windows PowerShell (PS1), который можно изменить перед тестированием и развертыванием пакета для рабочей области MED-V. В этом разделе приведены сведения и рекомендации по управлению параметрами конфигурации для MED-V с помощью Windows PowerShell перед развертыванием рабочих областей MED-V.

## Использование командлетов Windows PowerShell в MED-V


Следующие командлеты Windows PowerShell доступны в Microsoft Enterprise Virtualization (MED-V) 2,0:

**New-MedvConfiguration**

**Export-MedvConfiguration**

**New-MedvWorkspace**

**Export-MedvWorkspace**

Чтобы получить доступ к командлетам Windows PowerShell для MED-V, откройте Windows PowerShell и введите следующую команду для импорта модулей MED-V.

``` syntax
Import-Module microsoft.medv
```

После импорта модулей вы можете получить доступ к встроенной справке по командлетам с помощью стандартных команд справки Windows PowerShell, **Man** или **Get-Help**. Например, для доступа к описанию командлета **New-MedvConfiguration** , в том числе полного списка доступных параметров, введите следующую команду:

``` syntax
get-help New-MedvConfiguration
```

Вы также можете просмотреть справку по определенным параметрам. Например, чтобы просмотреть справку по параметру VmMemory, введите следующую команду:

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

Чтобы просмотреть список всех параметров конфигурации для MED-V и их значений по умолчанию, введите следующую команду:

``` syntax
New-MedvConfiguration -ForceDefaults
```

Чтобы просмотреть список всех параметров конфигурации для MED-V и их текущих значений, введите указанную ниже команду.

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## Создание рабочей области для MED-V с пользовательскими параметрами


После успешного создания пакета рабочей области MED-V с помощью диспетчера рабочих областей MED-V в папке, указанной для сохранения файлов упаковщика, создается сценарий Windows PowerShell. Содержимое этого сценария показывает некоторые доступные параметры конфигурации для MED-V, которые можно изменять.

Следуя этим инструкциям, вы можете настроить сценарий, а затем запустить его в Windows PowerShell, чтобы создать рабочую область MED-V с новыми параметрами.

**Важно!**  Запустите Windows PowerShell с учетными данными администратора и убедитесь, что политика выполнения Windows PowerShell разрешает выполнение сценариев.

1.  Измените сценарий Windows PowerShell, созданный диспетчером рабочих областей MED-V, или создайте новый сценарий с нужными параметрами конфигурации.

2.  Запустите Windows PowerShell с учетными данными администратора и в командной строке введите указанную ниже команду.

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    Эта команда запускает сценарий Windows PowerShell и запускает командлет **New-MedvWorkspace** для создания нового пакета рабочей области для MED-V. Новые файлы упаковщика сохраняются в папке, которая была первоначально указана для хранения файлов диспетчера рабочих областей для MED-V. Дополнительные сведения об этом командлете можно найти в справке Windows PowerShell.

 

## Экспорт конфигурации MED-V в файл реестра


После установки рабочей области для MED-V вы можете обновить параметры конфигурации MED-V. С помощью командлета **New-MedvConfiguration** можно указать параметры, которые нужно изменить. Например, чтобы создать файл реестра, который изменяет параметр памяти виртуальной машины, введите указанные ниже команды.

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

Чтобы применить новые параметры конфигурации, вы можете импортировать полученный файл реестра из главного компьютера в рабочую область MED-V.

## Статьи по теме


[Управление параметрами конфигурации рабочей области MED-V](managing-med-v-workspace-configuration-settings.md)

[Тестирование и развертывание пакета рабочих областей MED-V](test-and-deploy-the-med-v-workspace-package.md)

 

 





