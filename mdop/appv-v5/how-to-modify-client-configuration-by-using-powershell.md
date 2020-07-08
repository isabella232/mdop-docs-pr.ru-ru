---
title: Изменение конфигурации клиента с помощью PowerShell
description: Изменение конфигурации клиента с помощью PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813829"
---
# Изменение конфигурации клиента с помощью PowerShell


Чтобы настроить конфигурацию клиента App-V 5,0, выполните указанные ниже действия.

**Изменение конфигурации клиента App-V 5,0 с помощью PowerShell**

1.  Чтобы настроить параметры клиента с помощью PowerShell, используйте командлет **Set-AppvClientConfiguration** .

2.  Чтобы изменить конфигурацию клиента, откройте командную строка PowerShell и запустите следующий командлет **Set-AppvClientConfiguration** с необходимыми параметрами. Пример

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.0](operations-for-app-v-50.md)

 

 





