---
title: Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)
description: Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813325"
---
# Заметки о выпуске для App-V 5.0 с пакетом обновления 3 (SP3)


Ниже описаны известные проблемы, возникающие в Microsoft Application Virtualization (App-V) 5,0 с пакетом обновления 3 (SP3).

## После установки нового сервера App-V 5,0 SP3 на сервер файлы сервера не удаляются


Если вы удалите сервер App-V 5,0 SP1, а затем установите приложение App-V 5,0 SP3, установка завершится сбоем и на нем будет установлена неправильная версия сервера управления. На экране появятся указанные ниже ошибки.

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

Проблема возникает из-за того, что файлы сервера не удаляются при удалении App-V 5,0 с пакетом обновления 1 (SP1), поэтому при установке App-V 5,0 SP3 вместо новой установки происходит обновление.

**Временное решение**: перед установкой App-V 5,0 SP3 удалите следующий раздел реестра:

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## Запросы доменных служб Active Directory могут привести к неправильной работе некоторых приложений


При получении обновленных пакетов с помощью запроса доменных служб Active Directory для обновленных членств в группах может возникнуть ошибка, так как некоторые приложения будут работать неправильно, если приложения зависят от маркера доступа пользователя. Кроме того, частые запросы на членство в группах могут привести к перегрузке контроллера домена. Дополнительные сведения о маркерах доступа пользователей можно найти в разделе [маркеры доступа](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).

**Временное решение**: дождитесь, пока пользователь не выйдет из системы, а затем снова войдите в систему, прежде чем запрашивать обновленные сведения о группах. Не используйте раздел реестра, описанный в [пакете исправлений 2 для Microsoft Application Virtualization 5,0 с пакетом обновления 1](https://support.microsoft.com/kb/2897087)(SP1), для запроса обновленных сведений о членстве в группах.






## Статьи по теме


[Сведения об App-V 5.0 с пакетом обновления 3 (SP3)](about-app-v-50-sp3.md)

 

 





