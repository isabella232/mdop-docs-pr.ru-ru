---
title: Настройка разрешений для пользователей
description: Настройка разрешений для пользователей
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817732"
---
# Настройка разрешений для пользователей


Вы можете включить и отключить некоторые действия для пользователей, не обладающих правами администратора, изменив значения ключа в разделе " **разрешения** " (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions). Этот раздел главным образом предназначен для предотвращения ошибок пользователей, а не для обеспечения какой-либо особой защиты, так как пользователи с правами администратора могут изменять любые из этих значений ключа. Ниже приведены инструкции по изменению значений клавиш. Дополнительные сведения о ключах и значениях реестра клиента Application Virtualization (App-V) можно найти в разделе <https://go.microsoft.com/fwlink/?LinkId=121528> .

**Изменение разрешений пользователей**

1.  Чтобы разрешить пользователям запускать клиент в автономном режиме, задайте для параметра реестра значение 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode

2.  Чтобы разрешить пользователям просматривать все приложения с помощью пользовательского интерфейса, задайте для параметра значение 1. Если задать для этого параметра значение 0 (ноль), пользователи смогут видеть только те приложения, которые доступны для них.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications

## Статьи по теме


[Настройка параметров реестра клиента App-V с помощью командной строки](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Разрешения на доступ пользователей в клиенте Application Virtualization](user-access-permissions-in-application-virtualization-client.md)

 

 





