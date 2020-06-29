---
title: Уничтожение объекта групповой политики
description: Уничтожение объекта групповой политики
author: dansimp
ms.assetid: bfabd71a-47f3-462e-b86f-5f15762b9e28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 842a546c4db9cc6048908521baa05c6cc1a1a8a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818682"
---
# Уничтожение объекта групповой политики


Утверждающие могут уничтожить объект групповой политики (GPO), удалив его из корзины и окончательно удаляя, чтобы его нельзя было восстановить.

Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями. Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".

**Окончательное удаление объекта групповой политики, чтобы его нельзя было восстановить**

1.  В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.

2.  На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные объекты групповой политики.

3.  Щелкните правой кнопкой мыши объект групповой политики, который нужно удалить, и выберите команду **уничтожить**.

4.  Нажмите кнопку **Да** , чтобы подтвердить, что вы хотите окончательно удалить выбранный объект групповой политики и все резервные копии из архива.

5.  После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**. Объект групповой политики удаляется из **корзины** на вкладке "Корзина" и окончательно удаляется.

### Дополнительные рекомендации

-   По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ). В частности, необходимо иметь **содержимое списка** и **удалить разрешения GPO** для объекта групповой политики.

### Дополнительные ссылки

-   [Удаление, восстановление и уничтожение объекта групповой политики](deleting-restoring-or-destroying-a-gpo-agpm30ops.md)

 

 




