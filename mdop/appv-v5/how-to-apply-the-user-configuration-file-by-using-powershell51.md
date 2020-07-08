---
title: Применение файла конфигурации пользователя с помощью PowerShell
description: Применение файла конфигурации пользователя с помощью PowerShell
author: dansimp
ms.assetid: 986e638c-4a0c-4a7e-be73-f4615e8b8000
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97b3db253993d6d855384ee5d9771a7f9ff5b64d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814429"
---
# Применение файла конфигурации пользователя с помощью PowerShell


Файл динамической конфигурации применяется, когда пакет публикуется для определенного пользователя, и определяет, как будет выполняться пакет.

Чтобы задать файл конфигурации для определенного пользователя, выполните указанные ниже действия. Ниже описана процедура, основанная на примере.

**c:\\Packages\\Contoso\\MyApp.appv**

**Применение файла конфигурации пользователя**

1.  Чтобы добавить пакет на компьютер с помощью консоли PowerShell, введите следующую команду:

    **Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.

2.  Используйте следующую команду, чтобы опубликовать пакет для пользователя, и укажите обновленный файл динамической конфигурации.

    **Publish (AppVClientPackage $pkg — DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

 

 





