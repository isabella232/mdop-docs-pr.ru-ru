---
title: Изменение конфигурации клиента с помощью PowerShell
description: Изменение конфигурации клиента с помощью PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813813"
---
# Изменение конфигурации клиента с помощью PowerShell


Чтобы настроить конфигурацию клиента App-V 5,1, выполните указанные ниже действия.

**Изменение конфигурации клиента App-V 5,1 с помощью PowerShell**

1.  Чтобы настроить параметры клиента с помощью PowerShell, используйте командлет **Set-AppvClientConfiguration** . Дополнительные сведения об установке PowerShell и список командлетов можно найти в разделе [как загрузить командлеты PowerShell и получить справку по командлету](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).

2.  Чтобы изменить конфигурацию клиента, откройте командную строка PowerShell и запустите следующий командлет **Set-AppvClientConfiguration** с необходимыми параметрами. Пример

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **У вас есть предложение App-V**? Здесь вы можете добавить предложения и проголосовать [здесь](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **У вас возникла ошибка App-V?** Используйте [Форум TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Статьи по теме


[Операции, связанные с администрированием и использованием App-V 5.1](operations-for-app-v-51.md)

 

 





