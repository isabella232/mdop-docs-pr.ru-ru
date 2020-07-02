---
title: Управление неконтролируемым объектом групповой политики
description: Управление неконтролируемым объектом групповой политики
author: dansimp
ms.assetid: dc81545c-8da5-4b6f-b266-f01a82e27c6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 418e2a4100e1d824198b7d05034443948ec8a44c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818902"
---
# Управление неконтролируемым объектом групповой политики


Чтобы предоставить управление изменениями для объекта групповой политики (GPO), необходимо сначала управлять этим объектом.

Для выполнения этой процедуры необходимо использовать учетную запись пользователя с ролью "полный доступ" и "Администратор расширенного управления групповыми политиками (для опытных пользователей)" или необходимыми разрешениями. Ознакомьтесь с подробными сведениями в разделе "Дополнительные сведения".

**Управление неподдерживаемым объектом групповой политики**

1.  В дереве **консоли управления групповыми политиками** нажмите кнопку **изменить элемент управления** в лесу и домене, в котором вы хотите управлять объектами групповой политики.

2.  На вкладке **содержание** в области сведений щелкните вкладку **неконтрольные** значения, чтобы отобразить неконтрольные объекты групповой политики.

3.  Щелкните правой кнопкой мыши объект групповой политики, для которого нужно настроить управление групповыми политиками, и выберите пункт **элемент управления**.

4.  Введите Примечание, которое будет отображаться в журнале объекта групповой политики, и нажмите кнопку **ОК**.

5.  После того как окно **прогресса** показывает, что весь ход выполнения завершен, нажмите кнопку **Закрыть**. Объект групповой политики удаляется из списка на вкладке " **неуправляемый** " и добавляется на вкладку " **управляемые** ".

### Дополнительные рекомендации

-   По умолчанию для выполнения этой процедуры необходимо быть утверждающим или администратором расширенного управления групповыми политиками (полный доступ). В частности, необходимо иметь **содержимое списка** и **создать разрешения GPO** для домена.

### Дополнительные ссылки

-   [Создание и администрирование объекта групповой политики](creating-or-controlling-a-gpo-agpm40-app.md)

 

 




