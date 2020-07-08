---
title: Применение файла конфигурации развертывания с помощью PowerShell
description: Применение файла конфигурации развертывания с помощью PowerShell
author: dansimp
ms.assetid: 5df5d5bc-6c72-4087-8b93-d6d4b502a1f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6764f07dfe8cff1fb30c354937a405202468428
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814445"
---
# Применение файла конфигурации развертывания с помощью PowerShell


Файл динамической конфигурации развертывания применяется при добавлении пакета или задан на компьютере, на котором запущен клиент App-V 5,0 перед публикацией пакета. Файл настраивает параметры по умолчанию для пакета для всех пользователей на компьютере, на котором запущен клиент App-V 5,0. В этом разделе описаны действия, которые необходимо выполнить для использования файла конфигурации развертывания. Процедура основывается на следующем примере и предполагает, что на компьютере существуют следующие файлы пакета и конфигурации.

**c:\\Packages\\Contoso\\MyApp.appv**

**c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

**Применение файла конфигурации развертывания с помощью PowerShell**

-   Чтобы указать новый набор конфигураций по умолчанию для всех пользователей, которые будут запускать пакет на определенном компьютере, используйте следующую консоль:

    **Add-AppVClientPackage — path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

    **Примечание.**  
    Эта команда перехватывает полученный объект в $pkg. Если пакет уже присутствует на компьютере, можно использовать командлет **Set-AppVclientPackage** , чтобы применить документ конфигурации развертывания.

    **Set-AppVClientPackage-Name MyApp — путь c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)









