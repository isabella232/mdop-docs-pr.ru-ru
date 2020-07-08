---
title: Изменение размера кэша файловой системы
description: Изменение размера кэша файловой системы
author: dansimp
ms.assetid: 6ed17ba3-293b-4482-b3fa-31e5f606dad6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63c98d53ccb31e8eb64bc70d3d79b2198c506e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818002"
---
# Изменение размера кэша файловой системы


Вы можете изменить размер кэша файловой системы, используя командную строку. Это действие требует полного сброса кэша и требует наличия прав администратора.

**Изменение размера кэша файловой системы**

1.  Задайте для следующего значения реестра значение 0 (ноль):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Задайте для следующего значения реестра максимальный размер кэша (в МЕГАБАЙТах), необходимый для удержания пакетов (например, 8192 МБ).

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\FileSize

3.  Перезагрузите компьютер.

## Статьи по теме


[Настройка параметров реестра клиента App-V с помощью командной строки](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





