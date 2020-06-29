---
title: Уничтожение объекта групповой политики
description: Уничтожение объекта групповой политики
author: dansimp
ms.assetid: d74941a3-beef-46cd-a4ca-80a324dcfadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5545918c417fce16bfc2369ebc6fc2199390adc6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818649"
---
# Уничтожение объекта групповой политики


Расширенное управление групповыми политиками позволяет утверждающим уничтожить объект групповой политики (GPO), удалить его из корзины и окончательно удалить его, чтобы его нельзя было восстановить.

Для выполнения этой процедуры требуется учетная запись пользователя с ролью администратора (полного доступа) утверждающего или расширенного управления групповыми политиками или необходимыми разрешениями. Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".

**Окончательное удаление объекта групповой политики, чтобы его нельзя было восстановить**

1.  В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.

2.  На вкладке " **содержимое** " щелкните вкладку " **Корзина** ", чтобы отобразить удаленные объекты групповой политики.

3.  Щелкните правой кнопкой мыши объект групповой политики, который нужно удалить, и выберите команду **уничтожить**.

4.  Нажмите кнопку **Да** , чтобы подтвердить, что вы хотите окончательно удалить выбранный объект групповой политики и все резервные копии из архива.

5.  После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**. Объект групповой политики удаляется из **корзины** на вкладке "Корзина" и окончательно удаляется.

### Дополнительные рекомендации

-   По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ). В частности, необходимо иметь **содержимое списка** и **удалить разрешения GPO** для объекта групповой политики.

### Дополнительные ссылки

-   [Удаление, восстановление и уничтожение объекта групповой политики](deleting-restoring-or-destroying-a-gpo.md)

 

 




