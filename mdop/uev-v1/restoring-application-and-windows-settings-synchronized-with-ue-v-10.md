---
title: Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0
description: Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812376"
---
# Восстановление параметров приложений и системы Windows, синхронизированных с UE-V 1.0


Функции WMI и PowerShell в Microsoft User Experience Virtualization (UE-V) предоставляют возможность восстанавливать пакеты параметров. Команды WMI и PowerShell позволяют восстанавливать параметры приложения и Windows в значениях параметров, которые были установлены на компьютере при первом запуске приложения после установки UE-V Agent. Это действие по восстановлению выполняется отдельно для каждого приложения или параметров Windows. Эти параметры восстанавливаются при следующем запуске приложения или при входе пользователя в операционную систему.

**Восстановление параметров приложения и параметров Windows с помощью PowerShell**

1.  Откройте окно Windows PowerShell. Чтобы импортировать модуль PowerShell Microsoft UE-V, введите следующую команду:

    ``` syntax
    Import-module UEV
    ```

2.  Чтобы восстановить параметры приложения и параметры Windows, введите следующий командлет PowerShell.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Командлет PowerShell</strong></th>
    <th align="left"><strong>Описание</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Restore-UevUserSetting</p></td>
    <td align="left"><p>Восстанавливает параметры пользователя для приложения или восстанавливает группу параметров Windows.</p></td>
    </tr>
    </tbody>
    </table>

     

**Восстановление параметров приложения и параметров Windows с помощью WMI**

1.  Откройте окно PowerShell.

2.  Чтобы восстановить параметры приложения и параметры Windows, введите следующую команду WMI.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Команда WMI</strong></th>
    <th align="left"><strong>Описание</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Invoke-WmiMethod-Namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</p></td>
    <td align="left"><p>Восстанавливает параметры пользователя для приложения или восстанавливает группу параметров Windows.</p></td>
    </tr>
    </tbody>
    </table>

     

## Статьи по теме


[Администрирование UE-V 1.0](administering-ue-v-10.md)

[Операции в UE-V 1.0](operations-for-ue-v-10.md)

 

 





