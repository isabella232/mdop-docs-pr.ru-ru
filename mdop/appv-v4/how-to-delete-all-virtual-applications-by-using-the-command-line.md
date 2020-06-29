---
title: Удаление всех виртуальных приложений с помощью командной строки
description: Удаление всех виртуальных приложений с помощью командной строки
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817539"
---
# Удаление всех виртуальных приложений с помощью командной строки


Вы можете удалить все виртуальные приложения с определенного компьютера с помощью описанной ниже процедуры.

**Примечание**  Когда все приложения удаляются из пакета, клиент Application Virtualization (App-V) также удаляет пакет.

 

**Удаление всех приложений**

-   Чтобы удалить все приложения для учетной записи пользователя, для которой выполняется команда, выполните следующую команду: Если вы выполняете команду с дополнительным параметром/GLOBAL, используя учетную запись с правами администратора, все приложения удаляются для всех пользователей.

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    **Примечание**  Когда все приложения удаляются из пакета, клиент Application Virtualization (App-V) также удаляет пакет.

     

## Статьи по теме


[Добавление пакета с помощью командной строки](how-to-add-a-package-by-using-the-command-line.md)

[Удаление пакета с помощью командной строки](how-to-remove-a-package-by-using-the-command-line.md)

 

 





