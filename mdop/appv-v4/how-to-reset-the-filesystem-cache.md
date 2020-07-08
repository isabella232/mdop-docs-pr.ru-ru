---
title: Сброс параметров кэша файловой системы
description: Сброс параметров кэша файловой системы
author: dansimp
ms.assetid: 7777259d-8c21-4c06-9384-9599b69f9828
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 680634d98f8aac048af605c62029a0ee6b20af03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816712"
---
# Сброс параметров кэша файловой системы


Сброс кэша файловой системы не так, как обычно требуется. Тем не менее, если вам нужно полностью сбросить кэш файловой системы, например для устранения неполадок, вы можете использовать описанную ниже процедуру. Для выполнения этого действия требуются права администратора.

**Сброс кэша файловой системы**

1.  Задайте для следующего значения реестра значение 0 (ноль):

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS\\State

2.  Перезагрузите компьютер.

## Статьи по теме


[Настройка параметров реестра клиента App-V с помощью командной строки](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





